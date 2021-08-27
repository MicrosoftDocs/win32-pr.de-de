---
description: Stoppzeit. Standardmäßig ist der Wert auf eine sehr große Zahl festgelegt. Die abgeleitete Klasse kann den Wert in ihrem Konstruktor oder beim Initialisieren des Filters zurücksetzen.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: CSourceSeeking::m_rtStop Member (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4408fddf42070012aa6e1eb3a0268e8e449b571828c0904524f3cc8d27df3bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103000"
---
# <a name="csourceseekingm_rtstop-member"></a>CSourceSeeking::m \_ rtStop-Member

Stoppzeit. Standardmäßig ist der Wert auf eine sehr große Zahl festgelegt. Die abgeleitete Klasse kann den Wert in ihrem Konstruktor oder beim Initialisieren des Filters zurücksetzen.

## <a name="syntax"></a>Syntax


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a>Hinweise

Halten Sie den **Abschnitt "m \_ pLock** critical" vor dem Zugriff auf diese Variable.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




