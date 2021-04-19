---
description: 'Array von Stichproben der Größe coutputqueue:: m \_ lbatchsize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Coutputqueue:: m_ppSamples-Member (outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361983"
---
# <a name="coutputqueuem_ppsamples-member"></a>Coutputqueue:: m \_ ppsamples-Member

Array von Stichproben der Größe [**coutputqueue:: m \_ lbatchsize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Syntax


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Bemerkungen

Der Arbeits Thread ruft Beispiele aus der Warteschlange ab und platziert Sie in diesem Array. Er übergibt das Array an die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode. Wenn das Objekt keinen Arbeits Thread verwendet, platziert das Objekt Samples direkt in dieses Array. Die Member-Variable [**coutputqueue \_ :: m**](coutputqueue-m-list.md) enthält die Warteschlange.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




