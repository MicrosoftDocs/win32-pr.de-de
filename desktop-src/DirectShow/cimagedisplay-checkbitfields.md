---
description: Die CheckBitFields-Methode überprüft die Farbmasken in einer VIDEOINFO-Struktur.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: CImageDisplay.CheckBitFields-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44e60b6693dde202cd458cd09495dce9e4bea52ed96a468a8d3dcb6b2370eac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074174"
---
# <a name="cimagedisplaycheckbitfields-method"></a>CImageDisplay.CheckBitFields-Methode

Die `CheckBitFields` -Methode überprüft die Farbmasken in einer [**VIDEOINFO-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="syntax"></a>Syntax


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInput* 
</dt> <dd>

Zeiger auf eine **VIDEOINFO-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Farbmasken gültig sind, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode überprüft, ob die Farbmaske für jede Farbkomponente zwischen einem und acht Bits lang ist und dass jede Farbmaske eine zusammenhängende Sequenz von Bits ist. Rufen Sie diese Methode nur auf, wenn der **biCompression-Member** auf BI \_ BITFIELDS festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




