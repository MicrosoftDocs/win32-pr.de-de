---
description: Die ParserTemporaryLockFrame-Funktion sperrt einen Frame, wenn er in einen Parser eintritt, und entsperrt den Frame, wenn die Funktion den Parser beendet.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: ParserTemporaryLockFrame-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 47a8c02a29007084161897e34bd3ba6fbe3b5f53460aaced2acaf8e4924d67f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364386"
---
# <a name="parsertemporarylockframe-function"></a>ParserTemporaryLockFrame-Funktion

Die **ParserTemporaryLockFrame-Funktion** sperrt einen Frame, wenn er in einen Parser eintritt, und entsperrt den Frame, wenn die Funktion den Parser beendet.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame, auf den der Parser zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte der Daten im Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Parser sollten die **LockFrame-Funktion nicht** aufrufen. Wenn ein Parser eine Sperre verwendet und dann einen Fehler generiert oder ohne Entsperren des Frames zurückgibt, verlässt der Parser das System in einem Zustand, in dem er keine Protokolle ändern oder Frames ausschneiden oder kopieren kann. Parser sollten die **ParserTemporaryLockFrame-Funktion** verwenden, die eine Sperre nur im Kontext des Funktionseintrags im Parser gewährt. Beim Beenden des Parsers wird die Sperre für diesen Frame freigegeben. Daher ist der Zeiger nur gültig, nachdem der Parser vom Aufruf der **AttachProperties-** oder **RecognizeFrame-Funktion zurückgegeben** wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




