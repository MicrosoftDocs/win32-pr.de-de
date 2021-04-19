---
description: Zeiger auf einen kritischen Abschnitt.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Cbasemediafilter:: m_pLock Member (amfilter. h)'
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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361358"
---
# <a name="cbasemediafilterm_plock-member"></a>Cbasemediafilter:: m \_ Plock-Member

Zeiger auf einen kritischen Abschnitt.

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Bemerkungen

Der kritische Abschnitt wird während der Statusübergänge ([**cbasemediafilter:: Run**](cbasemediafilter-run.md), [**cbasemediafilter::P ause**](cbasemediafilter-pause.md), [**cbasemediafilter:: beenden**](cbasemediafilter-stop.md)), beim Zugriff auf die Referenzuhr ([**cbasemediafilter:: setsyncsource**](cbasemediafilter-setsyncsource.md), [**cbasemediafilter:: getsyncsource**](cbasemediafilter-getsyncsource.md)) und in der [**cbasemediafilter:: IsActive**](cbasemediafilter-isactive.md) -Methode gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




