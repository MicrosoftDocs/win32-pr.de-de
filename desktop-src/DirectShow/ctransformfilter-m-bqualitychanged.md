---
description: Flag, das angibt, ob sich die Qualität geändert hat.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Ctransformfilter:: m_bQualityChanged Member (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372660"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Ctransformfilter:: m \_ bqualitychanged-Member

Flag, das angibt, ob sich die Qualität geändert hat. Wenn der Filter zum ersten Mal ein Beispiel löscht, sendet er ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager und legt dieses Flag auf **true** fest. Dieses Ereignis wird erst dann wieder gesendet, wenn der Filter angehalten und neu gestartet wird, auch wenn es in der Zwischenzeit weiterhin Beispiele enthält.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




