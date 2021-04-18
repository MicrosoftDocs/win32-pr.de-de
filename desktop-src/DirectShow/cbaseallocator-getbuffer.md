---
description: 'Die GetBuffer-Methode ruft ein Medien Beispiel ab, das einen Puffer enthält. Diese Methode implementiert die imemzuzucator:: GetBuffer-Methode.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Cbasezucator. GetBuffer-Methode (amfilter. h)
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
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358722"
---
# <a name="cbaseallocatorgetbuffer-method"></a>Cbasezucator. GetBuffer-Methode

Die- `GetBuffer` Methode ruft ein Medien Beispiel ab, das einen Puffer enthält. Diese Methode implementiert die [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode.

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

Empfängt einen Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Puffers. Der Aufrufer muss die-Schnittstelle freigeben.

</dd> <dt>

*pstarttime* 
</dt> <dd>

Zeiger auf die Startzeit des Beispiels.

</dd> <dt>

*Zeit* 
</dt> <dd>

Zeiger auf die Endzeit der Stichprobe.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Bitweise Kombination von 0 (null) oder mehr Flags. Die Basisklasse unterstützt das folgende Flag.



| Wert                                                                                                                                                          | Bedeutung                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**AM \_ GBF \_ nowait**</dt> </dl> | Warten Sie nicht, bis ein Puffer verfügbar wird. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                     |
| <dl> <dt>**VFW \_ E \_ nicht committet \_**</dt> </dl> | Ein Commit für die Zuweisung wurde nicht ausgeführt.<br/> |
| <dl> <dt>**VFW \_ E \_ Timeout**</dt> </dl>        | Timeout.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Aufrufer das **am \_ GBF \_ nowait** -Flag nicht in *dwFlags* angibt, wird diese Methode blockiert, bis das nächste Beispiel verfügbar ist.

Das abgerufene Medien Beispiel verfügt über einen gültigen Zeiger auf den zugeordneten Puffer. Der Aufrufer ist dafür verantwortlich, alle anderen Eigenschaften für das Beispiel festzulegen, z. b. die Zeitstempel, die Medien Zeiten oder die Eigenschaft für den Synchronisierungs Punkt. Weitere Informationen finden Sie unter [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).

In der Basisklasse werden die Parameter *pstarttime* und *pdtime* ignoriert. Abgeleitete Klassen können diese Werte verwenden. Beispielsweise verwendet die Zuweisung für den [Videorenderer](video-renderer-filter.md) -Filter diese Werte, um den Wechsel zwischen DirectDraw-Oberflächen zu synchronisieren.

Wenn die Methode auf ein Beispiel warten muss, erhöht Sie die Anzahl der wartenden Objekte ([**cbasezucator:: m \_ lCount**](cbaseallocator-m-lcount.md)) und ruft die [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion für das Semaphor auf ([**cbasezuordcator:: m \_ hsem**](cbaseallocator-m-hsem.md)). Wenn ein Beispiel verfügbar wird, wird die [**cbasezucator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) -Methode für die Zuweisung aufgerufen, die die Anzahl der Semaphor um **m \_ lCount** erhöht (wodurch die wartenden Threads freigegeben werden) und **m \_ lCount** auf 0 (null) festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

