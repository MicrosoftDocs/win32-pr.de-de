---
description: Zeiger auf einen kritischen Abschnitt.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: CBaseMediaFilter::m_pLock-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad92cf07cc096c50ffa50f862c26f6133fc8dbb9b9b059419bb516e07cbd5daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910790"
---
# <a name="cbasemediafilterm_plock-member"></a>CBaseMediaFilter::m \_ pLock-Member

Zeiger auf einen kritischen Abschnitt.

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Hinweise

Der kritische Abschnitt wird während Zustandsübergängen [**(CBaseMediaFilter::Run,**](cbasemediafilter-run.md) [**CBaseMediaFilter::P ause,**](cbasemediafilter-pause.md) [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), beim Zugriff auf die Referenzuhr ([**CBaseMediaFilter::SetSyncSource,**](cbasemediafilter-setsyncsource.md) [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)) und in der [**CBaseMediaFilter::IsActive-Methode**](cbasemediafilter-isactive.md) gehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




