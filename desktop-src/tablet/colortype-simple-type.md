---
description: Definiert den Typ, der verwendet wird, um gültige Werte für die Farbe bestimmter Elemente in einer Journal-XML-Datei anzugeben.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: ColorType simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344990"
---
# <a name="colortype-simple-type"></a>ColorType simple-Typ

Definiert den Typ, der verwendet wird, um gültige Werte für die Farbe bestimmter Elemente in einer Journal-XML-Datei anzugeben.

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Bemerkungen

Eine Farbe kann ein Hexadezimal-RGB-Wert im Format \# RRGGBB sein. Er muss dem folgenden regulären Ausdruck entsprechen: \# \[ 0-9a-FA-F \] {6} . Beispiel: " \# 4a79b5".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



 

 




