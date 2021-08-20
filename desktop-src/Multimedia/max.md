---
title: max-Makro (Minwindef.h)
description: Das Makro max vergleicht zwei Werte und gibt den größeren zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- max macro Windows Multimedia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc592fcc588c14ee04c1f595c5b5bc95c860b2ab0b761906886010db478d5f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138646"
---
# <a name="max-macro"></a>max-Makro

Das **Makro max** vergleicht zwei Werte und gibt den größeren zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.

## <a name="syntax"></a>Syntax


```C++
 max(
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

Der Rückgabewert ist der größere der beiden angegebenen Werte.

## <a name="remarks"></a>Hinweise

Das **Makro max** ist wie folgt definiert:


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





