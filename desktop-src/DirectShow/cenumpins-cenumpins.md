---
description: 'CEnumPins.CEnumPins-Konstruktor : Konstruktormethode.'
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
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099228"
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

Zeiger auf den Filter, für den die Stecknadeln aufzählt werden.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Zeiger auf die [**IEnumPins-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) eines zu klonenden Enumerators oder **NULL.**

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn *pEnumPins* **NULL ist,** initialisiert diese Methode den Enumerator am Anfang der Enumerationssequenz. Andernfalls wird der interne Zustand des durch *pEnumPins angegebenen Enumerators dupliziert.*

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CEnumPins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




