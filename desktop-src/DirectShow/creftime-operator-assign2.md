---
description: Der Operator = weist eine neue Bezugszeit zu. Diese Methode verwendet den *ll* -Parameter.
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: "\"Kref time. Operator = Method (Ref time. h)-ll\"-Parameter"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372806"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>"Kref time. Operator = Method (Ref time. h)-ll"-Parameter

Der Operator = weist eine neue Bezugszeit zu.

## <a name="syntax"></a>Syntax


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ll* 
</dt> <dd>

Neue Verweis Zeit in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf das-Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Ref time. h (Include Streams. h)                                                                                   |
| Bibliothek | "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |



 

 




