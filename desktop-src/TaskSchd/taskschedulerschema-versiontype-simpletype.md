---
title: versionType Simple Type
description: Definiert ein Muster, das eine Version einer Aufgabe angibt.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- versionType simple type Taskplaner
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ad30f5ea14a447e2a08151ef2803b0577066e147e29673d373ce87eee033f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355036"
---
# <a name="versiontype-simple-type"></a>versionType Simple Type

Definiert ein Muster, das eine Version einer Aufgabe angibt.

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der **einfache typ versionType** ist eine **Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `\d+(\.\d+){1,3}`

    Ein Double gefolgt von einem, zwei oder drei Doubles. Beispiel: 1.2 oder 1.2.3.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





