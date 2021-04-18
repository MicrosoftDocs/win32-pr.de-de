---
description: Endzeit. Standardmäßig ist der Wert auf eine sehr große Zahl festgelegt. Die abgeleitete Klasse kann den Wert im Konstruktor zurücksetzen oder wenn der Filter initialisiert wird.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Csourceseeking:: m_rtStop Member (ctlutil. h)'
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
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365527"
---
# <a name="csourceseekingm_rtstop-member"></a>Csourceseeking:: m \_ rtstoppt-Member

Endzeit. Standardmäßig ist der Wert auf eine sehr große Zahl festgelegt. Die abgeleitete Klasse kann den Wert im Konstruktor zurücksetzen oder wenn der Filter initialisiert wird.

## <a name="syntax"></a>Syntax


```C++
CRefTime m_rtStop;
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

 

 




