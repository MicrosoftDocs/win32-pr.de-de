---
description: Konstruktormethode.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Cpersiststream. cpersiststream-Konstruktor (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354215"
---
# <a name="cpersiststreamcpersiststream-constructor"></a>Cpersiststream. cpersiststream-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kro* 
</dt> <dd>

Ein Zeiger auf die **IUnknown** -Schnittstelle des Delegatenobjekts.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf den allgemeinen com-Rückgabewert. Dieser Wert wird nur geändert, wenn diese Funktion fehlschlägt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




