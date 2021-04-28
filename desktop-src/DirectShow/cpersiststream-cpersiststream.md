---
description: 'CPersistStream.CPersistStream-Konstruktor : Konstruktormethode.'
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: CPersistStream.CPersistStream-Konstruktor (Pstream.h)
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
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085608"
---
# <a name="cpersiststreamcpersiststream-constructor"></a>CPersistStream.CPersistStream-Konstruktor

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

*Punk* 
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle** des delegierenden Objekts.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf den allgemeinen COM-Rückgabewert. Dieser Wert wird nur geändert, wenn diese Funktion fehlschlägt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pstream.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPersistStream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




