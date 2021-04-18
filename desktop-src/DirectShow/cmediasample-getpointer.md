---
description: 'Die getpointer-Methode ruft einen Lese-/Schreib-Zeiger auf den Puffer ab. Diese Methode implementiert die imediasample:: getpointer-Methode.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Cmediasample. getpointer-Methode (amfilter. h)
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
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371045"
---
# <a name="cmediasamplegetpointer-method"></a>Cmediasample. getpointer-Methode

Die `GetPointer` -Methode ruft einen Lese-/schreibzeiger auf den Puffer ab. Diese Methode implementiert die [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) -Methode.

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
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




