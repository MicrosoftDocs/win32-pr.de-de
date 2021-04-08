---
description: Der Experte muss die Register-expertenfunktion implementieren. Netzwerkmonitor Ruft die Register-expertenfunktion auf, um Informationen über den Experten zu erhalten.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Expertenrückruf Funktion registrieren (Netmon. h)
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
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864063"
---
# <a name="register-expert-callback-function"></a>Expertenrückruf Funktion registrieren

Der Experte muss die **Register** -expertenfunktion implementieren. Netzwerkmonitor Ruft die **Register** -expertenfunktion auf, um Informationen über den Experten zu erhalten.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pexpertinfo* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**expertenuminfo**](expertenuminfo.md) -Struktur, die von Netzwerkmonitor zugeordnet wird. Der Experte füllt die Struktur mit allen angeforderten Informationen aus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **true**, und die Funktion gibt die angeforderten Informationen zurück.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Das  Versionsmember der [**expertenenuminfo**](expertenuminfo.md) -Struktur muss NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




