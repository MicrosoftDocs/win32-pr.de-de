---
description: Die KSMULTIPLE \_ ITEM-Struktur beschreibt die Größe und Anzahl von Eigenschaften variabler Länge für Pins im Kernelmodus.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM-Struktur (Ks.h)
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
ms.openlocfilehash: 2e1cdf3d8edcea88fbcfb260d87d3e79d62eb2aebc57144ae38defb018065f1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823310"
---
# <a name="ksmultiple_item-structure"></a>KSMULTIPLE \_ ITEM-Struktur

Die `KSMULTIPLE_ITEM` -Struktur beschreibt die Größe und Anzahl von Eigenschaften variabler Länge für Pins im Kernelmodus.

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

Größe des zurückgegebenen Speicherblocks in Bytes. Die Größe umfasst die **KSMULTIPLE \_ ITEM-Struktur** und die darauf folgenden Elemente.

</dd> <dt>

**Count**
</dt> <dd>

Gibt die Gesamtzahl der Elemente an, die dieser Struktur folgen.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




