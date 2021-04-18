---
title: Einfacher Typ des Längen Typs
description: Definiert einen length-Typ, der verwendet wird, um die Anzahl von Bytes oder Zeichen in einem Datenelement variabler Länge anzugeben, z. b. Binärdaten oder eine ANSI-oder Unicode-Zeichenfolge.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Simple Type-Ereignistyp EventLog
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341207"
---
# <a name="lengthtype-simple-type"></a>Einfacher Typ des Längen Typs

Definiert einen length-Typ, der verwendet wird, um die Anzahl von Bytes oder Zeichen in einem Datenelement variabler Länge anzugeben, z. b. Binärdaten oder eine ANSI-oder Unicode-Zeichenfolge. Der Wert kann als xs: unsignedshort-Wert oder als Zeichenfolge angegeben werden, die auf den Namen des Datenelement Knotens verweist, der den Ganzzahl ohne Vorzeichen Short-Wert enthält.

``` syntax
<xs:simpleType name="LengthType">
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



 

 





