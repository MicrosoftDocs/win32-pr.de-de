---
title: Systemmonitor. Schreib only (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuer Elements ändern kann, oder legt diesen fest.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Schreibgeschützte Eigenschaft (Sysmon)
- Schreibgeschützte Eigenschaft "sysmon", Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", schreibgeschützte Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956427"
---
# <a name="systemmonitorreadonly-property"></a>Systemmonitor. Schreib only (Eigenschaft)

Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuer Elements ändern kann, oder legt diesen fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True, wenn der Benutzer die Eigenschaftswerte des Steuer Elements nicht ändern soll. andernfalls false. Der Standardwert ist false. Dies bedeutet, dass Benutzer die Eigenschaftswerte des Steuer Elements ändern können.

## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft true ist, sind die folgenden Bedingungen wirksam:

-   Der Benutzer kann das Kontextmenü nicht verwenden.
-   Die folgenden Symbolleisten Schaltflächen sind deaktiviert:
    -   Neuen Indikatorensatz
    -   Aktuellen Vorgang anzeigen
    -   Protokolldateidaten anzeigen
    -   Hinzufügen
    -   Löschen
    -   Leistungsindikatorliste einfügen
    -   Eigenschaften

Beachten Sie, dass sich diese Eigenschaft nur auf die Fähigkeit des Benutzers auswirkt, Eigenschaftswerte über die Benutzeroberfläche zu ändern. es hindert Sie nicht daran, Eigenschaftswerte oder-Indikatoren Programm gesteuert zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





