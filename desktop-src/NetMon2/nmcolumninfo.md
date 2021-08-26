---
description: Die NMCOLUMNINFO-Struktur definiert eine Spalte im oberen Bereich der Ereignisanzeige.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: NMCOLUMNINFO-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95683eb812a2b8a668664f7ad8092a91c1940d2c3f7185225e8364959777538b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037120"
---
# <a name="nmcolumninfo-structure"></a>NMCOLUMNINFO-Struktur

Die **NMCOLUMNINFO-Struktur** definiert eine Spalte im oberen Bereich der Ereignisanzeige.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**szColumnName**
</dt> <dd>

Der anzeigebare Name einer bestimmten Spalte. Wenn der Name zu lang ist, wird er in der Standardkonfiguration nicht Ereignisanzeige angezeigt.

</dd> <dt>

**VariantData**
</dt> <dd>

Die in die Spalte eingefügten Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




