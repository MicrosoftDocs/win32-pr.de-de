---
description: Zeiger auf eine \_ AMOVIESETUP-FILTER-Struktur.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: CFactoryTemplate::m_pAMovieSetup_Filter Member (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc4ee059eb47e08ae827392e8f29968463bb9bd4ca86e0c6b8a87a9f3bbd5667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697710"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>CFactoryTemplate::m \_ pAMovieSetup \_ Filter-Member

Zeiger auf eine [**AMOVIESETUP-FILTER-Struktur. \_**](amoviesetup-filter.md)

## <a name="syntax"></a>Syntax


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Hinweise

Verwenden Sie diese Struktur, um einen Filter selbst zu registrieren. Wenn ihre Komponente kein Filter ist, kann diese Membervariable **NULL sein.** Weitere Informationen finden Sie unter Registrieren von DirectShow-Filtern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CFactoryTemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




