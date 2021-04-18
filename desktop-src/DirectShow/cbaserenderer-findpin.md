---
description: Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Cbaserderderer. findpin-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364761"
---
# <a name="cbaserendererfindpin-method"></a>Cbaserderderer. findpin-Methode

Die- `FindPin` Methode ruft die PIN mit dem angegebenen Bezeichner ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Ein Zeiger auf eine Konstante, mit NULL endender breit Zeichen Zeichenfolge, die die PIN identifiziert. Muss L "in" lauten.

</dd> <dt>

*pppin* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN empfängt. Wenn die Methode fehlschlägt, wird *\* pppin* auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                       | Beschreibung                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>         | **Null** -Zeigerargument.<br/> |
| <dl> <dt>**VFW \_ E \_ nicht \_ gefunden**</dt> </dl> | Nicht gefunden:<br/>                 |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasefilter:: findpin**](cbasefilter-findpin.md) -Methode. Die einzige PIN des Filters (die Eingabe-PIN) heißt "in".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




