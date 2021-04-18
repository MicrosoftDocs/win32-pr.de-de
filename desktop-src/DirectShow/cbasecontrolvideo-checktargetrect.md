---
description: Die checktargetrect-Methode bestimmt, ob ein Ziel Rechteck gültig ist.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Cbasecontrolvideo. checktargetrect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368508"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>Cbasecontrolvideo. checktargetrect-Methode

Die- `CheckTargetRect` Methode bestimmt, ob ein Ziel Rechteck gültig ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptargetrect* 
</dt> <dd>

Zeiger auf das zu Überprüfung des Ziel Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ invalidArg" zurück, wenn es ungültig ist; andernfalls wird "noError (S OK)" zurückgegeben \_ .

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion bestimmt, ob das angeforderte Ziel Rechteck gültig ist. Da das Ziel Rechteck eine Position im logischen Client des Fensters angibt, können die Koordinaten negativ sein, obwohl die Gesamtbreite und Höhe nicht 0 (null) oder ein negativer Wert sein dürfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




