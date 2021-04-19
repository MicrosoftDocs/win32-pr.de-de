---
description: Die \_ Member-Variable m palloc ist ein Zeiger auf die imemzuordcator-Schnittstelle der Speicherzuweisung.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Cpullpin:: m_pAlloc Member (pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359709"
---
# <a name="cpullpinm_palloc-member"></a>Cpullpin:: m \_ palloc-Member

Die `m_pAlloc` Member-Variable ist ein Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle der Speicherzuweisung.

## <a name="syntax"></a>Syntax


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Bemerkungen

Die [**cpullpin::D ecidezuordcator**](cpullpin-decideallocator.md) -Methode legt diese Element Variable fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




