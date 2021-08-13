---
description: Die GetBuffer-Methode ruft ein Medienbeispiel ab, das einen Puffer enthält. Diese Methode implementiert die IMemAllocator::GetBuffer-Methode.
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: CBaseAllocator.GetBuffer-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a183079e954b3a0d8b07fc1d7daf039db8fcc840243a6ea421b2390ce02a3625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661682"
---
# <a name="cbaseallocatorgetbuffer-method"></a>CBaseAllocator.GetBuffer-Methode

Die `GetBuffer` -Methode ruft ein Medienbeispiel ab, das einen Puffer enthält. Diese Methode implementiert die [**IMemAllocator::GetBuffer-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IMediaSample-Schnittstelle des Puffers.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Der Aufrufer muss die Schnittstelle frei geben.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Zeiger auf die Startzeit des Beispiels.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Zeiger auf die Endzeit des Beispiels.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Bitweise Kombination von null oder mehr Flags. Die Basisklasse unterstützt das folgende Flag.



| Wert                                                                                                                                                          | Bedeutung                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**AM \_ GBF \_ NOWAIT**</dt> </dl> | Warten Sie nicht, bis ein Puffer verfügbar wird. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                           | Beschreibung                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NOT \_ COMMITTED**</dt> </dl> | Für allocator wurde kein Committed für die Zuweisungszuweisungen .)<br/> |
| <dl> <dt>**VFW \_ E \_ TIMEOUT**</dt> </dl>        | Timed out.<br/>                   |



 

## <a name="remarks"></a>Hinweise

Sofern der Aufrufer das **AM \_ GBF \_ NOWAIT-Flag** in *dwFlags* nicht angibt, wird diese Methode blockiert, bis das nächste Beispiel verfügbar ist.

Das abgerufene Medienbeispiel verfügt über einen gültigen Zeiger auf den zugeordneten Puffer. Der Aufrufer ist dafür verantwortlich, andere Eigenschaften für das Beispiel zu setzen, z. B. Zeitstempel, Medienzeiten oder die Synchronisierungspunkteigenschaft. Weitere Informationen finden Sie unter [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).

In der Basisklasse werden *die Parameter pStartTime* und *pEndTime* ignoriert. Abgeleitete Klassen können diese Werte verwenden. Beispielsweise verwendet die Zuweisung für den [Videorendererfilter](video-renderer-filter.md) diese Werte, um den Wechsel zwischen DirectDraw-Oberflächen zu synchronisieren.

Wenn die Methode auf ein Beispiel warten muss, erhöht sie die Anzahl der wartenden Objekte ([**CBaseAllocator::m \_ lCount**](cbaseallocator-m-lcount.md)) und ruft die [**WaitForSingleObject-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) für das Semaphor auf ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)). Wenn ein Beispiel verfügbar wird, ruft es die [**CBaseAllocator::ReleaseBuffer-Methode**](cbaseallocator-releasebuffer.md) für die Zuweisung auf, wodurch die Semaphoranzahl um **m \_ lCount** erhöht wird (wodurch die wartenden Threads frei werden) und **m \_ lCount** wieder auf 0 (null) gesetzt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

