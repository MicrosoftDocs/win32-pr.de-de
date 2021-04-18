---
description: Die loadstringaddr-Funktion transformiert eine Zeichenfolge (z \# . b. &0034; 157.54.32.45&\# 0034;) und erstellt eine DWORD-Adresse.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Loadstringaddr-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368112"
---
# <a name="loadstringaddr-function"></a>Loadstringaddr-Funktion

Die **loadstringaddr** -Funktion transformiert eine Zeichenfolge (z. b. "157.54.32.45") und erstellt eine **DWORD** -Adresse.

## <a name="syntax"></a>Syntax


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAddress* 
</dt> <dd>

Zeiger auf ein **DWORD**.

</dd> <dt>

*str* 
</dt> <dd>

Zeiger auf eine Zeichenfolge mit x. x. x. x-Darstellung einer IP-Adresse (z. b. 127.0.0.1).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

, Wenn die Funktion erfolgreich ausgeführt wurde (der Adress Name wurde gefunden); der Rückgabewert ist " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




