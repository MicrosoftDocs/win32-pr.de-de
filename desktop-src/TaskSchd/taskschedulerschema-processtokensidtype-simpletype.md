---
title: einfacher processtokensidtype-Typ
description: Definiert die möglichen Werte für das processtokensidtype (principaltype)-Element.
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Dateityp "processtokensidtype" Taskplaner
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391760"
---
# <a name="processtokensidtype-simple-type"></a>einfacher processtokensidtype-Typ

Definiert die möglichen Werte für das [**processtokensidtype (principaltype)**](taskschedulerschema-processtokensidtype-principaltype-element.md) -Element.

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache Typ **processtokensidtype** definiert die folgenden Werte.



| Wert        | BESCHREIBUNG                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Keine         | Tasks werden in einem Prozess ausgeführt, der keine Prozess Token-sid enthält (es werden keine Änderungen an der Liste der prozesstokengruppen vorgenommen).<br/> |
| Nicht eingeschränkt | Eine Task-sid wird vom vollständigen Aufgaben Pfad abgeleitet und der Liste der prozesstokengruppen hinzugefügt.<br/>                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





