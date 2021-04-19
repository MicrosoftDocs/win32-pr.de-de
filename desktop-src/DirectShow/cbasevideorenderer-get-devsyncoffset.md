---
description: Die get \_ devsyncoffset-Methode ruft die Standardabweichung der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem tatsächlichen Rendern ab, seit das Streaming gestartet wurde.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: CBaseVideoRenderer.get_DevSyncOffset-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366954"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>Cbasevideorenderer. get \_ devsyncoffset-Methode

Die `get_DevSyncOffset` -Methode ruft die Standardabweichung der Zeit in Millisekunden zwischen dem Zeitpunkt der Erstellung der einzelnen Frames und dem tatsächlichen Rendern ab, seit das Streaming gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidev* 
</dt> <dd>

Zeiger auf die Standardabweichung der Zeit, wie zuvor beschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**iqualprop:: get \_ devsyncoffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




