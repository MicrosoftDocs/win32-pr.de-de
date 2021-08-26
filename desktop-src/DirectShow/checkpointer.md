---
description: Überprüft, ob ein Zeiger NULL ist. Wenn der Zeiger NULL ist, gibt die Funktion oder Methode, in der bzw. der das Makro angezeigt wird, den angegebenen Wert zurück.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: CheckPointer-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ef1fa2370def45321958862ebaf3ded341b13f45ddae1ecafdc4a17e937aca08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999290"
---
# <a name="checkpointer-macro"></a>CheckPointer-Makro

Überprüft, ob ein Zeiger NULL **ist.** Wenn der Zeiger **NULL** ist, gibt die Funktion oder Methode, in der bzw. der das Makro angezeigt wird, den angegebenen Wert zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p* 
</dt> <dd>

Zu überprüfende Zeiger.

</dd> <dt>

*Ret* 
</dt> <dd>

Der Wert, den die Funktion oder Methode zurückgibt, wenn *p* **NULL ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die umgebende Funktion gibt *ret zurück,* wenn *p* **NULL ist.** Andernfalls führt das Makro nicht zur Rückgabe der umgebenden Funktion.

## <a name="examples"></a>Beispiele


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zeigervalidierungsmakros](pointer-validation-macros.md)
</dt> </dl>

 

 




