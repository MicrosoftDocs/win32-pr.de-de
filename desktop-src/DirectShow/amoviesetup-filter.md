---
description: Die amoviesetup- \_ Filter Struktur enthält Informationen zum Registrieren eines Filters.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: AMOVIESETUP_FILTER-Struktur (ComBase. h)
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
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361656"
---
# <a name="amoviesetup_filter-structure"></a>Amoviesetup- \_ Filter Struktur

Die **amoviesetup- \_ Filter** Struktur enthält Informationen zum Registrieren eines Filters.

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

**clsID**
</dt> <dd>

Klassen Bezeichner des Filters.

</dd> <dt>

**strName**
</dt> <dd>

Name des Filters.

</dd> <dt>

**dwmerit**
</dt> <dd>

Filter Verdienst. Wird von der [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle beim Erstellen eines Filter Diagramms verwendet. Eine Liste der Verdienst Werte finden Sie unter [Verdienst](merit.md).

</dd> <dt>

**npins**
</dt> <dd>

Anzahl der Elemente im *lppin* -Array. Wenn *lppin* **null** ist, legen Sie diesen Member auf NULL fest.

</dd> <dt>

**lppin**
</dt> <dd>

Zeiger auf ein Array von [**amoviesetup- \_ Pin**](amoviesetup-pin.md) -Strukturen der Größe *npins*. Jedes Element dieses Arrays beschreibt eine PIN für den Filter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zur Verwendung dieser Struktur finden Sie unter [Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md). Verwenden Sie diese Struktur nur für Filter, die in der Standardfilter Kategorie (CLSID \_ legacyamfiltercategory) registriert sind. Um einen Filter in einer anderen Kategorie zu registrieren, verwenden Sie die [**IFilterMapper2:: registerfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) -Methode, wie unter [Implementieren von DllRegisterServer](implementing-dllregisterserver.md)beschrieben.

> [!Note]  
> Die Header Datei "ComBase. h" wird mit den [DirectShow-Basisklassen](directshow-base-classes.md)bereitgestellt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> </dl>

 

 




