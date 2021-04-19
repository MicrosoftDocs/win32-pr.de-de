---
description: Zeigt ein Meldungs Feld mit der angegebenen Zeichenfolge, dem Namen der Quelldatei und der Zeilennummer an. Der Benutzer kann die Nachricht ignorieren, den Debugger eingeben oder die Anwendung beenden. Wird in Einzelhandels Builds ignoriert.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Dbgbreak-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372723"
---
# <a name="dbgbreak-macro"></a>Dbgbreak-Makro

Zeigt ein Meldungs Feld mit der angegebenen Zeichenfolge, dem Namen der Quelldatei und der Zeilennummer an. Der Benutzer kann die Nachricht ignorieren, den Debugger eingeben oder die Anwendung beenden. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*"Straume"* 
</dt> <dd>

Text Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Assert-und breakpointmakros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




