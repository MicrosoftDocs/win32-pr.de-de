---
title: min-Makro (minwindef. h)
description: Das min-Makro vergleicht zwei Werte und gibt den kleineren Wert zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Min. Makro Windows Multimedia
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
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743928"
---
# <a name="min-macro"></a>min-Makro

Das **Min** -Makro vergleicht zwei Werte und gibt den kleineren Wert zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.

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

Gibt die zweite von zwei-Werten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der kleinere der beiden angegebenen-Werte.

## <a name="remarks"></a>Bemerkungen

Das **Min** -Makro wird wie folgt definiert:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





