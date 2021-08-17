---
description: CEnumPins.CEnumPins-Konstruktor – Konstruktormethode.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: CEnumPins.CEnumPins-Konstruktor (Amfilter.h)
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
ms.openlocfilehash: 1972533b86215e34563b9b1aa8f1b8ac3c14450b804fdae01ed7c7eafa78def4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131240"
---
# <a name="cenumpinscenumpins-constructor"></a>CEnumPins.CEnumPins-Konstruktor

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

Zeiger auf den Filter, für den die Stecknadeln aufzählt werden sollen.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Zeiger auf die [**IEnumPins-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) eines zu klonenden Enumerators oder **NULL.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn *pEnumPins* **NULL** ist, initialisiert diese Methode den Enumerator am Anfang der Enumerationssequenz. Andernfalls wird der interne Zustand des durch *pEnumPins* angegebenen Enumerators dupliziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CEnumPins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




