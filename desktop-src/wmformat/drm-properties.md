---
title: DRM-Eigenschaften
description: DRM-Eigenschaften
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows Media-Format-SDK, DRM-Eigenschaften
- Advanced Systems Format (ASF), DRM-Eigenschaften
- ASF (Advanced Systems Format), DRM-Eigenschaften
- Digital Rights Management (DRM), Eigenschaften
- DRM (Digital Rights Management), Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8542d360c38ab3f12406462cefc0454e7eae33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037624"
---
# <a name="drm-properties"></a>DRM-Eigenschaften

In der folgenden Tabelle sind die DRM-Eigenschaften aufgeführt, die Anwendungen beim Schreiben oder lesen geschützter Dateien erhalten oder festlegen können. Diese Eigenschaften sind keine Dateiattribute. Sie werden nicht in den ASF-Dateiheader geschrieben.



| DRM-Eigenschaft                                                                             | Globaler Bezeichner                               | Datentyp             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**DRM- \_ Aktions zulässig**](drm-actionallowed.md)                                          | g \_ wszwmdrm- \_ Aktions zulässig                      | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ Aktions zulässige \_ Sicherung**](drm-actionallowed-backup.md)                           | g \_ wszwmdrm- \_ Aktions zulässige \_ Sicherung              | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ Aktions zugelassene \_ kollaborativeplay**](drm-actionallowed-collaborativeplay.md)     | g \_ wszwmdrm- \_ Aktions zulässige \_ kollaborative Zusammenspiel   | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ Aktions zulässige \_ Kopie**](drm-actionallowed-copy.md)                               | g \_ wszwmdrm- \_ Aktions zulässige \_ Kopie                | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ Aktions zulässige \_ CopyTo-CD**](drm-actionallowed-copytocd.md)                       | g \_ wszwmdrm- \_ Aktions zulässige \_ copyper-CD            | **WMT- \_ Typ \_ bool**   |
| [**DRM-Aktions zulässiges \_ \_ copytononsdmidevice**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszwmdrm- \_ Aktions zulässige \_ copytononsdmidevice | **WMT- \_ Typ \_ bool**   |
| [**DRM-Aktions zulässiges \_ \_ copytosdmidevice**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszwmdrm- \_ Aktions zulässige \_ copytosdmidevice    | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ Aktions zulässige \_ Wiedergabe**](drm-actionallowed-playback.md)                       | g \_ wszwmdrm- \_ Wiedergabe, Aktions zulässig \_            | **WMT- \_ Typ \_ bool**   |
| [**DRM \_ Action Allowed \_ playlistburn**](drm-actionallowed-playlistburn.md)               | g \_ wszwmdrm \_ Action Allowed \_ playlistburn        | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ baselicenabacqurl**](drm-baselicenseacqurl.md)                                  | g \_ wszwmdrm \_ baselicensetup-URL                  | **WMT \_ - \_ Typzeichenfolge** |
| [**DRM- \_ Flags**](drm-flags.md)                                                          | g \_ wszwmdrm- \_ Flags                              | **WMT- \_ Typ \_ DWORD**  |
| [**DRM \_ headersignprivkey**](drm-headersignprivkey.md)                                  | g \_ wszwmdrm \_ headersignprivkey                  | **WMT \_ - \_ Typzeichenfolge** |
| [**DRM- \_ isdrm**](drm-isdrm.md)                                                          | g \_ wszisdrm                                     | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ isdrmcme**](drm-isdrmcached.md)                                              | g \_ wszisdrmcme                               | **WMT- \_ Typ \_ bool**   |
| [**DRM- \_ keyseed**](drm-keyseed.md)                                                      | g \_ wszwmdrm- \_ keyseed                            | **WMT \_ - \_ Typzeichenfolge** |
| [**DRM- \_ Ebene**](drm-level.md)                                                          | g \_ wszwmdrm- \_ Ebene                              | **WMT- \_ Typ \_ DWORD**  |
| [**DRM- \_ Lizenz seid**](drm-licenseid.md)                                                  | g \_ wszwmdrm \_ licenseid                          | **WMT \_ - \_ Typzeichenfolge** |
| [**DRM- \_ Lizenzstatus**](drm-licensestate.md)                                            | "g \_ wszwmdrm \_ licenanstate"                       | **WMT- \_ Typ \_ DWORD**  |
| [**DRM \_ licenanstate \_ kollaborativeplay**](drm-licensestate-collaborativeplay.md)       | g \_ wszwmdrm \_ licen\state \_ kollaborativeplay    | **WMT \_ - \_ typbinär Datei** |
| [**DRM- \_ Lizenzstatus \_ Kopie**](drm-licensestate-copy.md)                                 | "g \_ wszwmdrm \_ licenanstate" \_ Kopieren                 | **WMT \_ - \_ typbinär Datei** |
| [**DRM \_ licenanstate \_ copyper CD**](drm-licensestate-copytocd.md)                         | g \_ wszwmdrm \_ licenanstate \_ copyper CD             | **WMT \_ - \_ typbinär Datei** |
| [**DRM \_ licenanstate \_ copytosdmidevice**](drm-licensestate-copytosdmidevice.md)         | g \_ wszwmdrm \_ \_ licentarstate copytosdmidevice     | **WMT \_ - \_ typbinär Datei** |
| [**DRM \_ licenanstate \_ copytononsdmidevice**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszwmdrm \_ licensstate \_ copytononsdmidevice  | **WMT \_ - \_ typbinär Datei** |
| [**DRM- \_ Lizenz Zustands \_ Wiedergabe**](drm-licensestate-playback.md)                         | g \_ wszwmdrm \_ licenanstate- \_ Wiedergabe             | **WMT \_ - \_ typbinär Datei** |
| [**DRM \_ licenanstate \_ playlistburn**](drm-licensestate-playlistburn.md)                 | g \_ wszwmdrm \_ licenanstate \_ playlistburn         | **WMT \_ - \_ typbinär Datei** |
| [**DRM- \_ Rechte**](drm-rights.md)                                                        | g \_ wszwmdrm- \_ Rechte                             | **WMT \_ - \_ Typzeichenfolge** |
| [**DRM- \_ saplevel**](drm-saplevel--deprecated.md)                                        | g \_ wszwmdrm ( \_ saplevel)                           | **WMT \_ - \_ Typzeichenfolge** |
| [**Verwenden von \_ Advanced \_ DRM**](use-advanced-drm.md)                                           | g \_ wszwmuse \_ Advanced \_ DRM                      | **WMT- \_ Typ \_ bool**   |
| [**Verwenden von \_ DRM**](use-drm.md)                                                              | g \_ wszwmuse \_ DRM                                | **WMT- \_ Typ \_ bool**   |
| [**Wmdrmnet \_ -Sperrung**](wmdrmnet-revocation.md)                                      | g \_ wszwmdrmnet-Sperrung \_                      | **WMT \_ - \_ Typzeichenfolge** |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Attribut Liste**](drm-attribute-list.md)
</dt> </dl>

 

 




