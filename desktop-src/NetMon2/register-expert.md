---
description: Der Experte muss die Register expert-Funktion implementieren. Netzwerkmonitor ruft die Register expert-Funktion auf, um Informationen zum Experten abzurufen.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrieren der Rückruffunktion "Expert" (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 1203682e82b01b7665c9661c3f58c14bbf2cd479cac62c72a64505b0e25feaa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889570"
---
# <a name="register-expert-callback-function"></a>Registrieren der Rückruffunktion "Expert"

Der Experte muss die **Register** expert-Funktion implementieren. Netzwerkmonitor ruft die **Register** expert-Funktion auf, um Informationen zum Experten abzurufen.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pExpertInfo* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**EXPERTENUMINFO-Struktur,**](expertenuminfo.md) die Netzwerkmonitor zuordnet. Der Experte füllt die Struktur mit allen angeforderten Informationen aus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **TRUE,** und die Funktion gibt die angeforderten Informationen zurück.

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Der **Version-Member** der [**EXPERTENUMINFO-Struktur**](expertenuminfo.md) muss 0 (null) sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




