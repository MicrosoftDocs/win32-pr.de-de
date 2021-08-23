---
title: ICONRESDIR-Struktur
description: Enthält die Dimensionen und das Farbformat eines einzelnen Symbolbilds in einer Ressourcengruppe. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- ICONRESDIR-StrukturMenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f81f8b0a530e7c6c85f2ad1749e0a7373f68b0bf902b71a86889b92184806ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034278"
---
# <a name="iconresdir-structure"></a>ICONRESDIR-Struktur

Enthält die Dimensionen und das Farbformat eines einzelnen Symbolbilds in einer Ressourcengruppe. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Die Breite des Symbols in Pixel. Zulässige Werte sind 16, 32 und 64.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Die Höhe des Symbols in Pixel. Zulässige Werte sind 16, 32 und 64.

</dd> <dt>

**ColorCount**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Die Anzahl der Farben im Symbol. Zulässige Werte sind 2, 8 und 16.

</dd> <dt>

**reserved**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Reserviert; muss auf den gleichen Wert wie für das reservierte Feld im Symboldateiheader festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **ICONRESDIR-Struktur** wird in der [**RESDIR-Struktur**](resdir.md) übergeben, wenn die **RESDIR-Struktur** ein Symbol beschreibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





