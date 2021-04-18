---
title: Maximales Makro (minwindef. h)
description: Das Maximum-Makro vergleicht zwei Werte und gibt den größeren Wert zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Maximales Makro Windows Multimedia
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
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517633"
---
# <a name="max-macro"></a>max-Makro

Das **Maximum** -Makro vergleicht zwei Werte und gibt den größeren Wert zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.

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

Gibt die zweite von zwei-Werten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der größere der beiden angegebenen-Werte.

## <a name="remarks"></a>Bemerkungen

Das **Maximum** -Makro wird wie folgt definiert:


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





