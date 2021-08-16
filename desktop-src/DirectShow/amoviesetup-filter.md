---
description: Die AMOVIESETUP \_ FILTER-Struktur enthält Informationen zum Registrieren eines Filters.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: AMOVIESETUP_FILTER-Struktur (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: fe50295f87e2932d3eb0fe53aac4896343a31441f8fa832bbaa69d5256846414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824790"
---
# <a name="amoviesetup_filter-structure"></a>\_AMOVIESETUP-FILTERstruktur

Die **AMOVIESETUP \_ FILTER-Struktur** enthält Informationen zum Registrieren eines Filters.

## <a name="syntax"></a>Syntax


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a>Member

<dl> <dt>

**Clsid**
</dt> <dd>

Klassenbezeichner des Filters.

</dd> <dt>

**strName**
</dt> <dd>

Name des Filters.

</dd> <dt>

**dwMerit**
</dt> <dd>

Filtervererz. Wird von der [**IGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) beim Erstellen eines Filterdiagramms verwendet. Eine Liste mit Denkwerten finden Sie unter [Vererz.](merit.md)

</dd> <dt>

**nPins**
</dt> <dd>

Anzahl der Elemente im *lpPin-Array.* Wenn *lpPin* **NULL** ist, legen Sie diesen Member auf 0 (null) fest.

</dd> <dt>

**lpPin**
</dt> <dd>

Zeiger auf ein Array von [**AMOVIESETUP-PIN-Strukturen \_**](amoviesetup-pin.md) der Größe *nPins*. Jedes Element dieses Arrays beschreibt eine Stecknadel für den Filter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Informationen zur Verwendung dieser Struktur finden Sie unter Registrieren von [DirectShow-Filtern.](how-to-register-directshow-filters.md) Verwenden Sie diese Struktur nur für Filter, die in der Standardfilterkategorie (CLSID \_ LegacyAmFilterCategory) registriert sind. Um einen Filter in einer anderen Kategorie zu registrieren, verwenden Sie die [**IFilterMapper2::RegisterFilter-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) wie unter [Implementieren von DllRegisterServer](implementing-dllregisterserver.md)beschrieben.

> [!Note]  
> Die Headerdatei combase.h wird mit den [DirectShow-Basisklassen](directshow-base-classes.md)bereitgestellt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Combase.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> </dl>

 

 




