---
description: CDispParams.CDispParams-Konstruktor – Konstruktormethode.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: CDispParams.CDispParams-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095788"
---
# <a name="cdispparamscdispparams-constructor"></a>CDispParams.CDispParams-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nArgs* 
</dt> <dd>

Anzahl von Argumenten, die an die Methode oder Eigenschaft übergeben werden.

</dd> <dt>

*pArgs* 
</dt> <dd>

Zeiger auf die Liste der Argumente. In der Liste wird jedes Argument mit seinem Variant-Typ gespeichert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDispParams-Klasse**](cdispparams.md)
</dt> </dl>

 

 




