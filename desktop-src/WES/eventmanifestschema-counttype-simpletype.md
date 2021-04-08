---
title: Einfacher Typ von zählype
description: Definiert einen Zähltyp, der verwendet wird, um die Anzahl von Elementen in einem Array anzugeben.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Event Log für den einfachen Typ von "zählype"
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743840"
---
# <a name="counttype-simple-type"></a>Einfacher Typ von zählype

Definiert einen Zähltyp, der verwendet wird, um die Anzahl von Elementen in einem Array anzugeben. Der Wert kann als xs: unsignedshort-Wert oder als Zeichenfolge angegeben werden, die auf den Namen des Datenelement Knotens verweist, der den unbestimmten Kurzwert enthält.

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





