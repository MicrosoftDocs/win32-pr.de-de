---
description: 'Die ReleaseBuffer-Methode gibt ein Medien Beispiel an die Liste der Beispiele für freie Medien zurück. Diese Methode implementiert die imemzuzucator:: ReleaseBuffer-Methode.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Cbasezucator. ReleaseBuffer-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371493"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>Cbasezucator. ReleaseBuffer-Methode

Die- `ReleaseBuffer` Methode gibt ein Medien Beispiel zur Liste der Beispiele für freie Medien zurück. Diese Methode implementiert die [**imemzuzucator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Medien Beispiel Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Verweis Zähler eines Medien Beispiels Null erreicht, ruft das Beispiel **ReleaseBuffer** mit sich selbst als Parameter auf. Diese Methode führt die folgenden Aktionen aus.

-   Gibt das Medien Beispiel in der kostenlosen Liste ([**cbasezucator:: m \_ lfree**](cbaseallocator-m-lfree.md)) zurück.
-   Ruft die [**cbasezucator:: notifysample**](cbaseallocator-notifysample.md) -Methode auf, die alle Threads freigibt, die bei Aufrufen der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode blockiert werden.
-   Wenn die [**cbasedepcator:: setnotify**](cbaseallocator-setnotify.md) -Methode zuvor aufgerufen wurde, ruft die **imemzuzucatornotifycallbacktemp:: notifyrelease** -Methode auf.
-   Wenn das letzte Beispiel freigegeben ist, wenn ein [**ausstehender cbasebelegcator::D ecommit**](cbaseallocator-decommit.md) -Aufruf vorhanden ist, ruft die [**cbasezucator:: Free**](cbaseallocator-free.md) -Methode auf, um den Pufferspeicher freizugeben. (In der Basisklasse ist **Free** eine rein virtuelle Methode.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




