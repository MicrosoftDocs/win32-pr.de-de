---
description: CEnumMediaTypes.CEnumMediaTypes-Konstruktor – Konstruktormethode.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: CEnumMediaTypes.CEnumMediaTypes-Konstruktor (Amfilter.h)
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
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095678"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>CEnumMediaTypes.CEnumMediaTypes-Konstruktor

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

*pPin* 
</dt> <dd>

Zeiger auf den Stecknadel, an dem die Enumeration ausgeführt werden soll.

</dd> <dt>

*pEnumMediaTypes* 
</dt> <dd>

Zeiger auf die [**IEnumMediaTypes-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) eines zu klonenden Enumerators oder **NULL.**

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn *pEnumMediaTypes* **NULL** ist, initialisiert diese Methode den Enumerator am Anfang der Enumerationssequenz. Andernfalls wird der interne Zustand des durch *pEnumMediaTypes* angegebenen Enumerators dupliziert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CEnumMediaTypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




