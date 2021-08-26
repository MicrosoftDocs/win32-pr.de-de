---
description: Die FindPin-Methode ruft den Pin mit dem angegebenen Bezeichner ab.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: CBaseRenderer.FindPin-Methode (Renbase.h)
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
ms.openlocfilehash: 0f639e5d68b11b6a7a65ccfe0d0c6465f822d591b0c4dfd0f4916072fde40856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043770"
---
# <a name="cbaserendererfindpin-method"></a>CBaseRenderer.FindPin-Methode

Die `FindPin` -Methode ruft den Pin mit dem angegebenen Bezeichner ab.

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

Zeiger auf eine konstante, mit NULL beendete Breitzeichenzeichenfolge, die den Pin identifiziert. Muss L"In" sein.

</dd> <dt>

*ppPin* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Pins empfängt. Wenn die Methode fehlschlägt, *\* wird ppPin* auf **NULL festgelegt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                       | Beschreibung                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>         |  NULL-Zeigerargument.<br/> |
| <dl> <dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt> </dl> | Nicht gefunden:<br/>                 |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseFilter::FindPin-Methode.**](cbasefilter-findpin.md) Der einzige Pin des Filters (der Eingabepin) heißt "In".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




