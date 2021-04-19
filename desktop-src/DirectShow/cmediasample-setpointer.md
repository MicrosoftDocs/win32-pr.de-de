---
description: Die setpointer-Methode legt den Zeiger auf den Arbeitsspeicher Puffer fest.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Cmediasample. setpointer-Methode (amfilter. h)
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
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370572"
---
# <a name="cmediasamplesetpointer-method"></a>Cmediasample. setpointer-Methode

Die- `SetPointer` Methode legt den Zeiger auf den Arbeitsspeicher Puffer fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptr* 
</dt> <dd>

Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer mit einer Größe von *cbytes*.

</dd> <dt>

*cbytes* 
</dt> <dd>

Länge des Puffers in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ermöglicht es der Zuweisung, einen neuen Zeiger für das Beispiel festzulegen.

Diese Methode ist nicht über die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle verfügbar. Das Objekt, das das Beispiel erstellt, kann auf diese Methode (über **cmediasample**) zugreifen, andere Objekte hingegen nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




