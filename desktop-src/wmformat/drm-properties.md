---
title: DRM-Eigenschaften
description: DRM-Eigenschaften
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows Medienformat-SDK, DRM-Eigenschaften
- Advanced Systems Format (ASF), DRM-Eigenschaften
- ASF (Advanced Systems Format), DRM-Eigenschaften
- Digital Rights Management (DRM), Eigenschaften
- DRM (Digital Rights Management), Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d553d644a6f3ec7130262d0e8567a4aa6ceab53286b24248607b1928991f51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848266"
---
# <a name="drm-properties"></a>DRM-Eigenschaften

In der folgenden Tabelle sind die DRM-Eigenschaften aufgeführt, die Anwendungen beim Schreiben oder Lesen geschützter Dateien erhalten oder festlegen können. Diese Eigenschaften sind keine Dateiattribute. Sie werden nicht in den ASF-Dateiheader geschrieben.



| DRM-Eigenschaft                                                                             | Globaler Bezeichner                               | Datentyp             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**\_DRM-AktionAllowed**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **\_WMT-TYP \_ BOOL**   |
| [**\_DRM-AktionAllowed \_ Backup**](drm-actionallowed-backup.md)                           | g \_ wszWMDRM \_ ActionAllowed \_ Backup              | **\_WMT-TYP \_ BOOL**   |
| [**\_DRM-AktionAllowed \_ CollaborativePlay**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **\_WMT-TYP \_ BOOL**   |
| [**\_DRM-AktionAllowed \_ Copy**](drm-actionallowed-copy.md)                               | g \_ wszWMDRM \_ ActionAllowed \_ Copy                | **\_WMT-TYP \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ CopyToCD**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **\_WMT-TYP \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ CopyToNonSDMIDevice**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **\_WMT-TYP \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ CopyToSDMIDevice**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **\_WMT-TYP \_ BOOL**   |
| [**\_DRM-AktionAllowed \_ Playback**](drm-actionallowed-playback.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ Playback            | **\_WMT-TYP \_ BOOL**   |
| [**\_DRM-AktionAllowed \_ PlaylistPlayList**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed \_ Playlist Aus        | **\_WMT-TYP \_ BOOL**   |
| [**DRM \_ BaseLicenseAcqURL**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **\_WMT-TYPZEICHENFOLGE \_** |
| [**\_DRM-Flags**](drm-flags.md)                                                          | g \_ wszWMDRM-Flags \_                              | **WMT \_ TYPE \_ DWORD**  |
| [**DRM \_ HeaderSignPrivKey**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **\_WMT-TYPZEICHENFOLGE \_** |
| [**DRM \_ IsDRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **\_WMT-TYP \_ BOOL**   |
| [**DRM \_ IsDRMCached**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **\_WMT-TYP \_ BOOL**   |
| [**DRM \_ KeySeed**](drm-keyseed.md)                                                      | g \_ wszWMDRM \_ KeySeed                            | **\_WMT-TYPZEICHENFOLGE \_** |
| [**\_DRM-Ebene**](drm-level.md)                                                          | g \_ wszWMDRM Level \_                              | **WMT \_ TYPE \_ DWORD**  |
| [**\_DRM-Lizenz-ID**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **\_WMT-TYPZEICHENFOLGE \_** |
| [**DRM \_ LicenseState**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **WMT \_ TYPE \_ DWORD**  |
| [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **\_WMT-TYP \_ BINARY** |
| [**DRM \_ LicenseState \_ Copy**](drm-licensestate-copy.md)                                 | g \_ wszWMDRM \_ LicenseState \_ Copy                 | **\_WMT-TYP \_ BINARY** |
| [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **\_WMT-TYP \_ BINARY** |
| [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **\_WMT-TYP \_ BINARY** |
| [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **\_WMT-TYP \_ BINARY** |
| [**DRM \_ \_ LicenseState-Wiedergabe**](drm-licensestate-playback.md)                         | g \_ wszWMDRM \_ LicenseState \_ Playback             | **\_WMT-TYP \_ BINARY** |
| [**DRM \_ LicenseState \_ Playlist Playlist**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM \_ LicenseState \_ Playlist Playlist         | **\_WMT-TYP \_ BINARY** |
| [**\_DRM-Rechte**](drm-rights.md)                                                        | g \_ wszWMDRM-Rechte \_                             | **\_WMT-TYPZEICHENFOLGE \_** |
| [**DRM \_ SAPLEVEL**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **\_WMT-TYPZEICHENFOLGE \_** |
| [**Verwenden \_ von Advanced \_ DRM**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ Advanced \_ DRM                      | **\_WMT-TYP \_ BOOL**   |
| [**Verwenden \_ von DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **\_WMT-TYP \_ BOOL**   |
| [**WMDRMNET-Sperrung \_**](wmdrmnet-revocation.md)                                      | g \_ wszWMDRMNET Revocation \_                      | **\_WMT-TYPZEICHENFOLGE \_** |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Attributliste**](drm-attribute-list.md)
</dt> </dl>

 

 




