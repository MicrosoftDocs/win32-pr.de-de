---
description: Die getprotocolinfo-Funktion gibt einen Zeiger auf einen Protokoll Informationswert zurück.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Getprotocolinfo-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958708"
---
# <a name="getprotocolinfo-function"></a>Getprotocolinfo-Funktion

Die **getprotocolinfo** -Funktion gibt einen Zeiger auf einen Protokoll Informationswert zurück.

## <a name="syntax"></a>Syntax


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Handle für ein Protokoll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Wert der Protokollinformationen.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getprotocolinfo** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




