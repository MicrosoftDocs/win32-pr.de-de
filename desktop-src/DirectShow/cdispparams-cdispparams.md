---
description: Konstruktormethode.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Cdisppara AMS. cdispparameams-Konstruktor (ctlutil. h)
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
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368606"
---
# <a name="cdispparamscdispparams-constructor"></a>Cdisppara AMS. cdispparameams-Konstruktor

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

*"nargs"* 
</dt> <dd>

Anzahl von Argumenten, die an die Methode oder Eigenschaft übermittelt werden.

</dd> <dt>

*Argumente* 
</dt> <dd>

Zeiger auf die Liste der Argumente. In der Liste wird jedes Argument mit dem Variant-Typ gespeichert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdispparameams-Klasse**](cdispparams.md)
</dt> </dl>

 

 




