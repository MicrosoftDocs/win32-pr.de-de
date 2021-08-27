---
description: Der Operator = weist eine neue Verweiszeit zu.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: CRefTime.operator=-Methode (Reftime.h)
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
ms.openlocfilehash: f4fe9a8f6f40dd1d0a7b0e38339c3ab21c44a989648e6c032b17a0ed3ac3b4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108070"
---
# <a name="creftimeoperator-method-reftimeh"></a>CRefTime.operator=-Methode (Reftime.h)

Der Operator = weist eine neue Verweiszeit zu.

## <a name="syntax"></a>Syntax


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Verweis auf ein **CRefTime-Objekt,** das die neue Verweiszeit angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf das -Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Reftime.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




