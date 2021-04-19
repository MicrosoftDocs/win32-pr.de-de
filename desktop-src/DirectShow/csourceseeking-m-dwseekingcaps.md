---
description: Suchfunktionen.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Csourceseeking:: m_dwSeekingCaps Member (ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372571"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Csourceseeking:: m \_ dwseekingcaps-Member

Suchfunktionen.

## <a name="syntax"></a>Syntax


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Bemerkungen

Standardmäßig wird der Wert auf die bitweise Kombination der folgenden Flags festgelegt:

-   Sucht nach " \_ \_ canseekforward"
-   Sucht nach " \_ \_ canseekabwärts"
-   Sucht nach " \_ \_ canseekabsolute"
-   \_Sucht nach \_ cangetstoppos
-   \_Suche nach \_ cangetduration

Wenn der Filter einen anderen Satz von Funktionen unterstützt, überschreiben Sie diesen Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




