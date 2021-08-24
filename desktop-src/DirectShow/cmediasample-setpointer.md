---
description: Die SetPointer-Methode legt den Zeiger auf den Speicherpuffer fest.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: CMediaSample.SetPointer-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af6747eb9ed39a973d795d8701fd9d7afd1b88e9d0b0db577de6a8e963b840bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634350"
---
# <a name="cmediasamplesetpointer-method"></a>CMediaSample.SetPointer-Methode

Die `SetPointer` -Methode legt den Zeiger auf den Speicherpuffer fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ptr* 
</dt> <dd>

Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer der Größe *cBytes.*

</dd> <dt>

*cBytes* 
</dt> <dd>

Länge des Puffers in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Mit dieser Methode kann die Zuweisung einen neuen Zeiger für das Beispiel festlegen.

Diese Methode ist nicht über die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) verfügbar. Das Objekt, das das Beispiel erstellt, kann (über **CMediaSample)** auf diese Methode zugreifen, andere Objekte jedoch nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




