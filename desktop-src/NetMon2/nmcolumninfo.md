---
description: Die nmcolumninfo-Struktur definiert eine Spalte im oberen Bereich der Ereignisanzeige.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Nmcolumninfo-Struktur (Netmon. h)
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
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373354"
---
# <a name="nmcolumninfo-structure"></a>Nmcolumninfo-Struktur

Die **nmcolumninfo** -Struktur definiert eine Spalte im oberen Bereich der Ereignisanzeige.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**szcolumnname**
</dt> <dd>

Der anzeigbare Name einer bestimmten Spalte. Wenn der Name zu lang ist, wird er in der Standard Ereignisanzeige Konfiguration nicht vollständig angezeigt.

</dd> <dt>

**Variantdata**
</dt> <dd>

Die in die Spalte eingefügten Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




