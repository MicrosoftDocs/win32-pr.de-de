---
title: SystemMonitor.ReadOnly (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuerelements ändern kann, oder legt diesen fest.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- ReadOnly-Eigenschaft SysMon
- ReadOnly-Eigenschaft SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , ReadOnly-Eigenschaft
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
ms.openlocfilehash: d4baee1e95a6c40e2983e92e914df921b9f91613ec0bebc1da9f74c54404b7f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955035"
---
# <a name="systemmonitorreadonly-property"></a>SystemMonitor.ReadOnly (Eigenschaft)

Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuerelements ändern kann, oder legt diesen fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True, wenn der Benutzer die Eigenschaftswerte des Steuerelements nicht ändern soll. andernfalls FALSE. Der Standardwert ist FALSE. Das bedeutet, dass Benutzer die Eigenschaftswerte des Steuerelements ändern können.

## <a name="remarks"></a>Hinweise

Wenn der Wert dieser Eigenschaft True ist, sind die folgenden Bedingungen wirksam:

-   Der Benutzer kann das Kontextmenü nicht verwenden.
-   Die folgenden Symbolleistenschaltflächen sind deaktiviert:
    -   Neuen Indikatorensatz
    -   Aktuellen Vorgang anzeigen
    -   Protokolldateidaten anzeigen
    -   Add
    -   Löschen
    -   Leistungsindikatorliste einfügen
    -   Eigenschaften

Beachten Sie, dass diese Eigenschaft nur die Fähigkeit des Benutzers beeinflusst, Eigenschaftswerte über die Benutzeroberfläche zu ändern. Sie verhindert nicht, dass Sie Eigenschaftswerte oder Leistungsindikatoren programmgesteuert ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





