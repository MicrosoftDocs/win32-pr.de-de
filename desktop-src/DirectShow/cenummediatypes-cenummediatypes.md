---
description: Konstruktormethode.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Cenenmediatypes. cenenmediatypes-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355956"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Cenenmediatypes. cenenmediatypes-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die PIN, auf der die Enumeration ausgeführt werden soll.

</dd> <dt>

*Datentypen* 
</dt> <dd>

Ein Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle eines Enumerators, der geklont werden soll, oder **null**.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn " *pummediatypes* " **null** ist, initialisiert diese Methode den Enumerator bis zum Anfang der enumerationssequenz. Andernfalls dupliziert Sie den internen Zustand des Enumerators, der durch " *pummediatypes*" angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cenum mediatypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




