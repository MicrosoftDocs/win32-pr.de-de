---
description: HRESULT-Wert, der angibt, ob das Objekt Beispiele akzeptiert. Wenn der Wert S \_ OK ist, akzeptiert das Objekt Stichproben. Andernfalls werden Stichproben abgelehnt.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Coutputqueue:: m_hr-Member (outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372348"
---
# <a name="coutputqueuem_hr-member"></a>Coutputqueue:: m \_ HR-Mitglied

**HRESULT** -Wert, der angibt, ob das Objekt Beispiele akzeptiert. Wenn der Wert S \_ OK ist, akzeptiert das Objekt Stichproben. Andernfalls werden Stichproben abgelehnt.

## <a name="syntax"></a>Syntax


```C++
HRESULT m_hr;
```



## <a name="remarks"></a>Bemerkungen

Diese Element Variable wird verwendet, um Aktivitäten Thread übergreifend zu koordinieren. Wenn die downstreameingabepin eine Stichprobe ablehnt, oder wenn das Objekt mit dem leeren beginnt, wird der Wert auf S \_ false oder auf einen Fehlercode festgelegt. Das Objekt stellt keine weiteren Beispiele bereit, bis die Leerung beendet ist, oder bis die [**coutputqueue:: Reset**](coutputqueue-reset.md) -Methode aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




