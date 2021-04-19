---
description: Die ksmultiple \_ -Elementstruktur beschreibt die Größe und die Anzahl der Eigenschaften variabler Länge in den kernelmoduspins.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM Struktur (". h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361366"
---
# <a name="ksmultiple_item-structure"></a>Ksmultiple- \_ Elementstruktur

Die `KSMULTIPLE_ITEM` -Struktur beschreibt die Größe und die Anzahl der Eigenschaften variabler Länge in den kernelmoduspins.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Größe des zurückgegebenen Speicherblocks in Bytes. Die Größe schließt die **ksmultiple- \_ Element** Struktur und die folgenden Elemente ein.

</dd> <dt>

**Count**
</dt> <dd>

Gibt die Gesamtzahl der Elemente an, die dieser Struktur folgen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>. H.</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[**Ikspin:: ksquerymediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**Regpinmedium**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




