---
description: Die Reset-Methode setzt das-Objekt zurück, sodass mehr Daten empfangen werden können.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Coutputqueue. Reset-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356324"
---
# <a name="coutputqueuereset-method"></a>Coutputqueue. Reset-Methode

Die- `Reset` Methode setzt das-Objekt zurück, sodass mehr Daten empfangen werden können.

## <a name="syntax"></a>Syntax


```C++
void Reset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode setzt die Element Variable [**coutputqueue:: m \_ HR**](coutputqueue-m-hr.md) auf S \_ OK zurück. Das Objekt kann erneut Medien Beispiele empfangen. beispielsweise nach einem Löschvorgang.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




