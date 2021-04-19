---
description: Erstellt eine Speicher Kopie eines Bilds.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Cbasecontrolvideo. CopyImage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370065"
---
# <a name="cbasecontrolvideocopyimage-method"></a>Cbasecontrolvideo. CopyImage-Methode

Erstellt eine Speicher Kopie eines Bilds.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf das Beispiel, das das Videobild enthält.

</dd> <dt>

*pvideoinfo* 
</dt> <dd>

Zeiger auf das Format, das das Videobild darstellt.

</dd> <dt>

*pbuffersize* 
</dt> <dd>

Ein Zeiger auf die Größe des Ausgabepuffers.

</dd> <dt>

*pvideoimage* 
</dt> <dd>

Zeiger auf den Ausgabepuffer.

</dd> <dt>

*psourcerect* 
</dt> <dd>

Zeiger auf das Quellvideo Rechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der *pvideoimage* -Parameter **null** ist, wird der *pbuffersize* -Parameter mit der Anzahl der Bytes aufgefüllt, die der Ausgabepuffer zum Speichern des Bilds benötigt. Wenn der über gegebene Puffer zu klein ist oder die Member-Funktion nicht genügend Arbeitsspeicher zuweist, gibt die Member-Funktion E \_ outo fmemory zurück.

## <a name="remarks"></a>Bemerkungen

Die Member-Funktion Ruft das Bild aus dem Beispiel ab und kopiert es in den Ausgabepuffer. Der Abschnitt des Videos, das in den Ausgabepuffer kopiert wird, spiegelt das Quell Rechteck wider, das über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle festgelegt wird (obwohl das Ziel Rechteck nicht widergespiegelt wird).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




