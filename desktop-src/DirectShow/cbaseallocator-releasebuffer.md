---
description: Die ReleaseBuffer-Methode gibt ein Medienbeispiel an die Liste kostenloser Medienbeispiele zurück. Diese Methode implementiert die IMemAllocator::ReleaseBuffer-Methode.
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: CBaseAllocator.ReleaseBuffer-Methode (Amfilter.h)
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
ms.openlocfilehash: 5d1096cc7cd4ed31346b38719a3f622edf780408fd50262d93515f68d92b421d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661506"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>CBaseAllocator.ReleaseBuffer-Methode

Die `ReleaseBuffer` -Methode gibt ein Medienbeispiel an die Liste der Beispiele für kostenlose Medien zurück. Diese Methode implementiert die [**IMemAllocator::ReleaseBuffer-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer)

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Medienbeispielobjekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Wenn der Verweiszähler eines Medienbeispiels 0 (null) erreicht, ruft das Beispiel **ReleaseBuffer** mit sich selbst als Parameter auf. Diese Methode führt die folgenden Aktionen aus.

-   Gibt das Medienbeispiel an die Freie Liste zurück ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Ruft die [**CBaseAllocator::NotifySample-Methode**](cbaseallocator-notifysample.md) auf, die alle Threads freigibt, die bei Aufrufen der [**CBaseAllocator::GetBuffer-Methode**](cbaseallocator-getbuffer.md) blockiert werden.
-   Wenn die [**CBaseAllocator::SetNotify-Methode**](cbaseallocator-setnotify.md) zuvor aufgerufen wurde, ruft die **IMemAllocatorNotifyCallbackTemp::NotifyRelease-Methode** auf.
-   Wenn das letzte Beispiel freigegeben wird und ein ausstehender [**CBaseAllocator::D ecommit-Aufruf**](cbaseallocator-decommit.md) vorhanden ist, ruft die [**CBaseAllocator::Free-Methode**](cbaseallocator-free.md) auf, um den Pufferspeicher freizugeben. (In der Basisklasse ist **Free** eine reine virtuelle Methode.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




