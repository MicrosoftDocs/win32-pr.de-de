---
description: Die GetSourceRect-Methode ruft das Quellrechteck ab. Dies ist eine interne Methode.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: CBaseControlVideo.GetSourceRect-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a637e0f5ab5c97494dc072458a29920110363a3e4f07ba8bb7313947996bdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057050"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a>CBaseControlVideo.GetSourceRect-Methode

Die `GetSourceRect` -Methode ruft das Quellrechteck ab. Dies ist eine interne Methode.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Zeiger auf das abgerufene Quellrechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion muss in der abgeleiteten Klasse überschrieben werden, um das Quellrechteck zurückzugeben, das vom Videorenderer gehalten wird. Sie wird von den folgenden [**CBaseControlVideo-Memberfunktionen**](cbasecontrolvideo.md) aufgerufen.

-   [**CBaseControlVideo::GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)
-   [**CBaseControlVideo::put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo::get \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)
-   [**CBaseControlVideo::put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo::get \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)
-   [**CBaseControlVideo::put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo::get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)
-   [**CBaseControlVideo::put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)
-   [**CBaseControlVideo::get \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)

Im folgenden Beispiel wird eine Implementierung dieser Funktion in einer abgeleiteten Klasse veranschaulicht.


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



In diesem Beispiel ist CVideoText eine von [**CBaseControlVideo**](cbasecontrolvideo.md)abgeleitete Klasse, m \_ pRenderer enthält ein Objekt einer klasse, die von [**CBaseVideoRenderer**](cbasevideorenderer.md)abgeleitet wurde, und der \_ m DrawImage-Datenmember, der in der abgeleiteten Klasse definiert ist, enthält ein [**CDrawImage-Objekt.**](cdrawimage.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




