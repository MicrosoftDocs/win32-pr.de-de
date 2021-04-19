---
description: Die parsertemporarylockframe-Funktion sperrt einen Frame, wenn er in einen Parser eintritt, und entsperrt den Frame, wenn die Funktion den Parser beendet.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Funktion "parametertemporarylockframe" (Netmon. h)
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
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363338"
---
# <a name="parsertemporarylockframe-function"></a>Funktion "parametertemporarylockframe"

Die **parsertemporarylockframe** -Funktion sperrt einen Frame, wenn er in einen Parser eintritt, und entsperrt den Frame, wenn die Funktion den Parser beendet.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame, auf den der Parser zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte der Daten im Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Parser sollten die **Lock Frame** -Funktion nicht aufzurufen. Wenn ein Parser eine Sperre annimmt und dann einen Fehler generiert oder zurückgibt, ohne den Frame zu entsperren, verlässt der Parser das System in einem Zustand, in dem er keine Protokolle ändern oder Frames Ausschneiden oder kopieren kann. Parser sollten die **parsertemporarylockframe** -Funktion verwenden, die eine Sperre nur im Kontext des Funktions Eintrags in den Parser erteilt. Beim Beenden des Parsers wird die Sperre für diesen Frame freigegeben. Folglich ist der Zeiger nur dann gültig, wenn der Parser vom Aufrufen der **attachproperties** -Funktion oder der **erkenzeframe** -Funktion zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




