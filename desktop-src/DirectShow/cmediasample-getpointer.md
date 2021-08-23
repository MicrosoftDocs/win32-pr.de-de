---
description: Die GetPointer-Methode ruft einen Lese-/Schreibzeiger auf den Puffer ab. Diese Methode implementiert die IMediaSample::GetPointer-Methode.
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: CMediaSample.GetPointer-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21a39fae4f243c0a4e7305573f1b06ee2f11766729ef4933124d059b20b3a14b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832270"
---
# <a name="cmediasamplegetpointer-method"></a>CMediaSample.GetPointer-Methode

Die `GetPointer` -Methode ruft einen Lese-/Schreibzeiger auf den Puffer ab. Diese Methode implementiert die [**IMediaSample::GetPointer-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf den Puffer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




