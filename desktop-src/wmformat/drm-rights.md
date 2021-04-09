---
title: DRM_Rights
description: Die DRM- \_ Rechte Eigenschaft gibt die Rechte an, die die Anwendung beim nächsten Versuch benötigt, eine geschützte Datei zu öffnen.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038536"
---
# <a name="drm_rights"></a>DRM- \_ Rechte

Die **DRM- \_ Rechte** Eigenschaft gibt die Rechte an, die die Anwendung beim nächsten Versuch benötigt, eine geschützte Datei zu öffnen.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ Rechte

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich um eine Eigenschaft mit Lese-/Schreibzugriff, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) abgerufen und entweder mithilfe von [**iwmdrmreader:: setdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) oder [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt wird.

In der folgenden Tabelle sind die unterstützten Rechte aufgeführt.



| Rechts                                           | Zeichenfolgenliteral      | BESCHREIBUNG                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszwmdrm- \_ Rechte \_ Sicherung                      | „Backup“            | Recht zum Sichern der Lizenz.                                                                                                                                                                                        |
| g \_ wszwmdrm \_ right \_ COLLABORATIVE \_ Play         | "Kollaborativeplay" | Das Recht, die Datei im Rahmen einer Zusammenarbeits Wiedergabe Wiedergabe wiederzugeben.                                                                                                                                                          |
| g \_ wszwmdrm- \_ Rechte \_ Kopie                        | "Kopieren"              | Recht zum Kopieren der Datei auf ein Gerät. Dieses Recht ersetzt die älteren Kopierrechte (g \_ wszwmdrm \_ right \_ Copy \_ to \_ CD, g \_ wszwmdrm \_ right \_ Copy \_ to \_ Non \_ SDMI \_ Device und g \_ wszwmdrm right Copy \_ \_ \_ to \_ SDMI \_ Device). |
| g \_ wszwmdrm \_ - \_ Rechte \_ auf \_ CD kopieren                | "Print. Redbook"     | Rechts zum Kopieren der Datei auf eine CD (rotes Buchformat). In Windows Media DRM 10 wird dieses Recht durch g \_ wszwmdrm \_ right Copy ersetzt \_ .<br/>                                                                             |
| g \_ wszwmdrm- \_ Rechte \_ Kopie \_ auf nicht- \_ \_ SDMI- \_ Gerät kopieren | "Transfer. nonsdmi"  | Recht zum Kopieren der Datei auf ein nicht-SDMI-Gerät. In Windows Media DRM 10 wird dieses Recht durch g \_ wszwmdrm \_ right Copy ersetzt \_ .<br/>                                                                                  |
| g \_ wszwmdrm- \_ Rechte \_ Kopie \_ auf \_ SDMI- \_ Gerät kopieren      | "Transfer. SDMI"     | Recht zum Kopieren der Datei auf ein SDMI-kompatibles Gerät. In Windows Media DRM 10 wird dieses Recht durch g \_ wszwmdrm \_ right Copy ersetzt \_ .<br/>                                                                           |
| g \_ wszwmdrm \_ right- \_ Wiedergabe                    | Theater              | Das Recht, die Mediendatei wiederzugeben.                                                                                                                                                                                        |



 

Diese Eigenschaft enthält eine Zeichenfolge mit breit Zeichen von mindestens einer durch Semikolons getrennten Berechtigung, z. b.: L "Wiedergabe; Skopie Kollaborativeplay ".

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 





