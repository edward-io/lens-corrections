# Lens corrections

Manufacturer-supplied Adobe lens correction profiles (`.lcp`) for Viltrox and Sigma lenses, with Lensfun XML conversions of the RAW profiles. Each folder covers one lens and mount. The collection contains 33 LCPs and 21 Lensfun XML files.

## Using the profiles

### Lightroom Classic and Adobe Camera Raw

Choose the `.lcp` for your lens, mount, and image type. Use the RAW profile for camera RAW files and the non-RAW profile, where available, for rendered files such as JPEGs and TIFFs. Copy the `.lcp` to your user profile directory and restart the app. [Adobe lens profile guide](https://helpx.adobe.com/x-productkb/multi/lens-profile-support.html) · [Sigma installation guide](https://www.sigma-global.com/en/support/download/LensCorrectionProfileUserManual_for_20200mmF3563DGContemporary.pdf)

- macOS `~/Library/Application Support/Adobe/CameraRaw/LensProfiles/1.0/`
- Windows `%APPDATA%\Adobe\CameraRaw\LensProfiles\1.0\`

Enable profile corrections in **Lens Corrections → Profile**. If the app doesn’t select a profile automatically, choose the lens and profile manually. Sigma’s interim profiles are intended for manual selection. [Lightroom Classic instructions](https://helpx.adobe.com/lightroom-classic/desktop/process-and-develop-photos/retouch-photos.html) · [Sigma profile guide](https://www.sigma-global.com/en/support/download/LensCorrectionProfileUserManual_50_12_a024.pdf)

### Lensfun

Copy the `*-lensfun.xml` files you want into your app’s Lensfun user database directory, usually `~/.local/share/lensfun/` on macOS and Linux. Restart the app and select the lens manually if its metadata doesn’t match automatically. These files require a Lensfun build that supports **database format 2** and the **Adobe Camera Model (`acm`)**. [Lensfun database locations](https://lensfun.github.io/manual/latest/dbsearch.html) · [Database format](https://lensfun.github.io/manual/latest/dbformat.html)

## Lens coverage

### Viltrox

The LCPs came from Viltrox’s global, Taiwan, and Japan download pages. [Viltrox Download Center](https://viltrox.com/pages/download-center-1) · [Taiwan downloads](https://www.viltrox.com.tw/downloads/lens/) · [Japan downloads](https://viltroxjapan.jp/pages/downloads)

| Lens | Mount | Files |
| --- | --- | --- |
| [AF 16mm f/1.8 FE](viltrox/AF-16mm-f1.8-FE/) | Sony E | RAW LCP, Lensfun |
| [MF 20mm f/1.8](viltrox/MF-20mm-f1.8-E/) | Sony E | RAW and non-RAW LCPs, Lensfun |
| [MF 20mm f/1.8](viltrox/MF-20mm-f1.8-Z/) | Nikon Z | RAW and non-RAW LCPs, Lensfun |
| [AF 23mm f/1.4 E](viltrox/AF-23mm-f1.4-E/) | Sony E | Non-RAW LCP |
| [AF 23mm f/1.4 XF](viltrox/AF-23mm-f1.4-XF/) | Fujifilm X | RAW and non-RAW LCPs, Lensfun |
| [AF 24mm f/1.8 FE](viltrox/AF-24mm-f1.8-FE/) | Sony E | RAW and non-RAW LCPs, Lensfun |
| [AF 26mm f/2.8 EVO FE](viltrox/AF-26mm-f2.8-EVO-FE/) | Sony E | RAW and non-RAW LCPs, Lensfun |
| [AF 26mm f/2.8 EVO Z](viltrox/AF-26mm-f2.8-EVO-Z/) | Nikon Z | RAW and non-RAW LCPs, Lensfun |
| [AF 33mm f/1.4 XF](viltrox/AF-33mm-f1.4-XF/) | Fujifilm X | RAW and non-RAW LCPs, Lensfun |
| [AF 56mm f/1.4 XF](viltrox/AF-56mm-f1.4-XF/) | Fujifilm X | RAW and non-RAW LCPs, Lensfun |
| [AF 85mm f/1.8 FE](viltrox/AF-85mm-f1.8-FE/) | Sony E | Non-RAW LCP |
| [AF 85mm f/1.8 XF](viltrox/AF-85mm-f1.8-XF/) | Fujifilm X | Non-RAW LCP |
| [AF 85mm f/1.8 Z](viltrox/AF-85mm-f1.8-Z/) | Nikon Z | Non-RAW LCP |

### Sigma

Each Sigma folder contains a RAW LCP from a Sigma interim download and its Lensfun XML. [Sigma resource catalog](https://www.sigma-global.com/en/support/catalog/lenses/) · [Canon RF profile guide](https://www.sigma-global.com/en/support/download/Lens%20Correction%20Profile%20User%20Manual%20for%2015mm%20F1.4%20DC%20Contemporary%20CANON.pdf)

| Lens | Mount |
| --- | --- |
| [15mm F1.4 DC Contemporary](sigma/15mm-f1.4-dc-contemporary-e/) | Sony E |
| [15mm F1.4 DC Contemporary](sigma/15mm-f1.4-dc-contemporary-rf/) | Canon RF |
| [15mm F1.4 DG DN Diagonal Fisheye Art](sigma/15mm-f1.4-dg-dn-fisheye-art-e/) | Sony E |
| [17–40mm F1.8 DC Art](sigma/17-40mm-f1.8-dc-art-e/) | Sony E |
| [20–60mm F2.8–4 DG Contemporary](sigma/20-60mm-f2.8-4-dg-contemporary-e/) | Sony E |
| [20–200mm F3.5–6.3 DG Contemporary](sigma/20-200mm-f3.5-6.3-dg-contemporary-e/) | Sony E |
| [28–105mm F2.8 DG DN Art](sigma/28-105mm-f2.8-dg-dn-art-e/) | Sony E |
| [35mm F1.2 DG II Art](sigma/35mm-f1.2-dg-ii-art-e/) | Sony E |
| [35mm F1.4 DG II Art](sigma/35mm-f1.4-dg-ii-art-e/) | Sony E |
| [50mm F1.2 DG DN Art](sigma/50mm-f1.2-dg-dn-art-e/) | Sony E |
| [135mm F1.4 DG Art](sigma/135mm-f1.4-dg-art-e/) | Sony E |
| [500mm F5.6 DG DN OS Sports](sigma/500mm-f5.6-dg-dn-os-sports-e/) | Sony E |

## Conversion notes

- The Lensfun XMLs were generated with `lensfun-convert-lcp` from RAW calibration records. Aperture values were converted from APEX to f-numbers using `f = 2^(Av/2)`. Both Viltrox 26mm EVO profiles have a single vignetting sample at f/8. [Lensfun converter](https://github.com/lensfun/lensfun/blob/master/docs/man/lensfun-convert-lcp.1.rst) · [Exif aperture standard](https://www.cipa.jp/std/documents/j/DC-008-2012_J_C.pdf)
- The Viltrox 24mm RAW LCP has a corrected `CameraRawProfile` header (`Ture` → `True`). Its individual non-RAW calibration record was excluded from the Lensfun XML.
- The Viltrox MF 20mm profiles contain distortion and lateral chromatic aberration corrections. The LCPs lack the aperture metadata needed to convert their vignetting data.
- Several vignetting samples produced black corners in Lensfun and were omitted. The affected XMLs have comments identifying the samples. Sigma’s XMLs use the LCP polynomial vignetting curves.
- The XMLs were checked in Lensfun 0.3.99.0 for lens matching and correction behavior on synthetic pixels. Correction quality on real photos hasn’t been verified.

## Licensing

The licensing terms for the Viltrox and Sigma lens profiles are unclear. We haven’t verified what permissions apply to the manufacturer-supplied LCPs or the Lensfun XMLs derived from them.
