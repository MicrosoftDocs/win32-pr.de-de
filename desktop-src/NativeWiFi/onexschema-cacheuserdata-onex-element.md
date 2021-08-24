---
description: Gibt an, ob die Benutzeranmeldeinformationen für nachfolgende Verbindungen zwischengespeichert werden.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: cacheUserData(OneX)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f4663153fa9aff176180387ebaf0321ab3d48ec2c382e9e84c0f524d6e0ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800870"
---
# <a name="cacheuserdata-onex-element"></a>cacheUserData(OneX)-Element

Das cacheUserData-Element (OneX) gibt an, ob die Benutzeranmeldeinformationen für nachfolgende Verbindungen zwischengespeichert werden. Wenn cacheUserData true ist, werden die Anmeldeinformationen zwischengespeichert. Wenn cacheUserData auf FALSE festgelegt ist, werden die Anmeldeinformationen nicht zwischengespeichert, und der Benutzer wird bei nachfolgenden Verbindungsversuchen möglicherweise zur Eingabe von Anmeldeinformationen aufgefordert.

Dieses Element ist optional. Wenn cacheUserData nicht in einem Profil angegeben ist, werden die Benutzeranmeldeinformationen zwischengespeichert.

**Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

Das **cacheUserData-Element** wird durch das [**OneX-Element**](onexschema-onex-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




