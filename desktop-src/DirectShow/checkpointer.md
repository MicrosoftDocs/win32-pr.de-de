---
description: Überprüft, ob ein Zeiger NULL ist. Wenn der Zeiger NULL ist, gibt die Funktion oder Methode, in der das Makro angezeigt wird, den angegebenen Wert zurück.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Check Pointer-Makro (wxdebug. h)
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
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372135"
---
# <a name="checkpointer-macro"></a>Check Pointer-Makro

Überprüft, ob ein Zeiger **null** ist. Wenn der Zeiger **null** ist, gibt die Funktion oder Methode, in der das Makro angezeigt wird, den angegebenen Wert zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cker* 
</dt> <dd>

Der zu Überprüfung Ende Zeiger.

</dd> <dt>

*TZI* 
</dt> <dd>

Der Wert, den die Funktion oder Methode zurückgibt, wenn *p* **null** ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die umgebende Funktion gibt *ret* zurück, wenn *p* **null** ist. Andernfalls bewirkt das Makro nicht, dass die umgebende Funktion zurückgibt.

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
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zeiger Validierungs Makros](pointer-validation-macros.md)
</dt> </dl>

 

 




