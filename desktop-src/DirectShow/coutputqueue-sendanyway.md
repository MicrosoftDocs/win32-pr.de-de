---
description: Die sendanyway-Methode liefert alle ausstehenden Beispiele.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Coutputqueue. sendanyway-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373600"
---
# <a name="coutputqueuesendanyway-method"></a>Coutputqueue. sendanyway-Methode

Die- `SendAnyway` Methode stellt alle ausstehenden Beispiele bereit.

## <a name="syntax"></a>Syntax


```C++
void SendAnyway();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Element Variable [**coutputqueue:: m \_ bbatchexact**](coutputqueue-m-bbatchexact.md) den Wert **true** hat, füllt das Objekt das [**coutputqueue:: m \_ ppsamples**](coutputqueue-m-ppsamples.md) -Array aus, bevor es einen Batch von Beispielen liefert. Mit dieser Methode können Sie einen partiellen Batch bereitstellen. Beispielsweise ruft die [**coutputqueue:: EOS**](coutputqueue-eos.md) -Methode `SendAnyway` auf, um Streamende-Nachrichten zu serialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




