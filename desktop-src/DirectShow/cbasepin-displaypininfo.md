---
description: Die DisplayPinInfo-Methode verfolgt eine Pinverbindung während des Debuggens.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: CBasePin.DisplayPinInfo-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98930ec48d3daa13d6ae463b38ce1ae62d745de9fae65915dcabcedf3cd673aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916470"
---
# <a name="cbasepindisplaypininfo-method"></a>CBasePin.DisplayPinInfo-Methode

Die `DisplayPinInfo` -Methode verfolgt eine Stecknadelverbindung während des Debuggens.

## <a name="syntax"></a>Syntax


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die empfangende Stecknadel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

In Debugbuilds ruft diese Methode die [**DbgLog-Funktion**](dbglog.md) auf, um einen Verbindungsversuch nachzuverfolgen. In Einzelhandelsbuilds führt diese Methode nichts aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




