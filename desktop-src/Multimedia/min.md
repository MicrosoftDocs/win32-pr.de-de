---
title: min-Makro (Minwindef.h)
description: Das Min-Makro vergleicht zwei Werte und gibt den kleineren zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- min macro Windows Multimedia
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832adc4a4d326ca8e0689d1ca44ade2e0b77db770cabe6042e42c47e23a44f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985672"
---
# <a name="min-macro"></a>min-Makro

Das **Min-Makro** vergleicht zwei Werte und gibt den kleineren zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.

## <a name="syntax"></a>Syntax


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value1* 
</dt> <dd>

Gibt den ersten von zwei Werten an.

</dd> <dt>

*value2* 
</dt> <dd>

Gibt den zweiten von zwei Werten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der kleinere der beiden angegebenen Werte.

## <a name="remarks"></a>Hinweise

Das **min-Makro** ist wie folgt definiert:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





