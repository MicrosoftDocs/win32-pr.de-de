---
title: processTokenSidType – einfacher Typ
description: Definiert die möglichen Werte für das ProcessTokenSidType -Element (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- einfacher processTokenSidType-Typ Taskplaner
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 505f8abe340af36c25792ec97a5a465a166eedb74921c800d2a568d10a5cce0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611902"
---
# <a name="processtokensidtype-simple-type"></a>processTokenSidType – einfacher Typ

Definiert die möglichen Werte für das [**ProcessTokenSidType -Element (principalType).**](taskschedulerschema-processtokensidtype-principaltype-element.md)

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

Der einfache **processTokenSidType-Typ** definiert die folgenden Werte.



| Wert        | Beschreibung                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Keine         | Aufgaben werden in einem Prozess ausgeführt, der keine Prozesstoken-SID enthält (an der Liste der Prozesstokengruppen werden keine Änderungen vorgenommen).<br/> |
| Nicht eingeschränkt | Eine Task-SID wird vom vollständigen Aufgabenpfad abgeleitet und der Liste der Prozesstokengruppen hinzugefügt.<br/>                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





