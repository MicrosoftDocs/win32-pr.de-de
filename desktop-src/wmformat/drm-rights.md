---
title: DRM_Rights
description: Die \_ DRM Rights-Eigenschaft gibt die Rechte an, die die Anwendung beim nächsten Versuch zum Öffnen einer geschützten Datei benötigt.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d655ea3f4a0a5dccc8b5e1380296948c9a55dce1d86336f824b30189f6557d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930900"
---
# <a name="drm_rights"></a>\_DRM-Rechte

Die **DRM \_ Rights-Eigenschaft** gibt die Rechte an, die die Anwendung beim nächsten Versuch zum Öffnen einer geschützten Datei benötigt.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM-Rechte \_

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Dies ist eine Lese-/Schreibeigenschaft, die mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) abgerufen und entweder mit [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) oder [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt wird.

In der folgenden Tabelle sind die unterstützten Rechte aufgeführt.



| Right                                           | Zeichenfolgenliteral      | Beschreibung                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ RIGHT \_ BACKUP                      | „Backup“            | Recht zum Sichern der Lizenz.                                                                                                                                                                                        |
| g \_ wszWMDRM \_ RIGHT COLLABORATIVE \_ \_ PLAY         | "CollaborativePlay" | Recht zum Wiedergeben der Datei als Teil einer Gemeinsamen Wiedergabeliste.                                                                                                                                                          |
| g \_ wszWMDRM \_ RIGHT \_ COPY                        | "Kopieren"              | Recht zum Kopieren der Datei auf ein Gerät. Dieses Recht ersetzt die älteren Kopierrechte (g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD, g \_ wszWMDRM \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI DEVICE und g \_ \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE). |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD                | "Print.redbook"     | Recht zum Kopieren der Datei auf eine CD (Red Book-Format). In Windows Media DRM 10 wird dieses Recht durch g \_ wszWMDRM \_ RIGHT \_ COPY ersetzt.<br/>                                                                             |
| g \_ wszWMDRM \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI \_ DEVICE | "Transfer.NONSDMI"  | Recht zum Kopieren der Datei auf ein Nicht-SDMI-Gerät. In Windows Media DRM 10 wird dieses Recht durch g \_ wszWMDRM \_ RIGHT \_ COPY ersetzt.<br/>                                                                                  |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE      | "Transfer.SDMI"     | Recht zum Kopieren der Datei auf ein SDMI-kompatibles Gerät. In Windows Media DRM 10 wird dieses Recht durch g \_ wszWMDRM \_ RIGHT \_ COPY ersetzt.<br/>                                                                           |
| g \_ wszWMDRM \_ RIGHT \_ PLAYBACK                    | "Play"              | Recht zum Wiedergeben der Mediendatei.                                                                                                                                                                                        |



 

Diese Eigenschaft enthält eine Breitzeichenzeichenfolge mit mindestens einem durch Semikolons getrennten Recht, z.B.: L"Playback; Kopieren; CollaborativePlay".

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 





