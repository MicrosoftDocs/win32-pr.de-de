---
description: Konstruktormethode.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Cenumpins. cenumpins-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355955"
---
# <a name="cenumpinscenumpins-constructor"></a>Cenumpins. cenumpins-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, für den die Pins aufgelistet werden sollen.

</dd> <dt>

*Anmeldungen* 
</dt> <dd>

Ein Zeiger auf die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle eines Enumerators, der geklont werden soll, oder **null**.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die *penumpins* **null** sind, initialisiert diese Methode den Enumerator bis zum Anfang der enumerationssequenz. Andernfalls dupliziert Sie den internen Zustand des Enumerators, der durch *penumpins* angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cenumpins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




