---
description: Die setconfiginfo-Methode gibt den igraphconfig-Zeiger und das-Ereignis zum Abbrechen an.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Cdynamicoutputpin. setconfiginfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368409"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>Cdynamicoutputpin. setconfiginfo-Methode

Die `SetConfigInfo` -Methode gibt den [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) -Zeiger und das-Ereignis zum Abbrechen an.

## <a name="syntax"></a>Syntax


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pgraphconfig* 
</dt> <dd>

Ein Zeiger auf die [**igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) -Schnittstelle oder **null**.

</dd> <dt>

*hstopevent* 
</dt> <dd>

Handle für ein Ereignis, das signalisiert wird, wenn der Filter beendet wird, oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Filter muss diese Methode aufzurufen, wenn er dem Filter Diagramm Beitritt. Der Filter Graph-Manager unterstützt **igraphconfig**. Erstellen Sie für den *hstopevent* -Parameter ein manuelles Zurücksetzungs Ereignis. Wenn der Filter das Filter Diagramm verlässt, muss diese Methode erneut mit **null** für beide Parameter aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




