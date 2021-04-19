---
description: 'Dauer des Streams. Standardmäßig wird der Wert auf den Wert der csourceseeking:: m rtstoppt-Element Variablen festgelegt \_ .'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Csourceseeking:: m_rtDuration Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361982"
---
# <a name="csourceseekingm_rtduration-member"></a>Csourceseeking:: m \_ rtduration-Member

Dauer des Streams. Standardmäßig wird der Wert auf den Wert der [**csourceseeking:: m \_ rtstoppt**](csourceseeking-m-rtstop.md) -Element Variablen festgelegt.

## <a name="syntax"></a>Syntax


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Bemerkungen

Halten Sie den kritischen Abschnitt **m \_ Plock** vor dem Zugriff auf diese Variable gedrückt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




