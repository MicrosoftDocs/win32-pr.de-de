---
description: Die DestroyProtocol-Funktion zerstört das Protokoll, das von der CreateProtocol-Funktion erstellt wird.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: DestroyProtocol-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c3a89bfd74a01a7455ecd9393d913ddd906474ceabd1c8884f187444cb483a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911140"
---
# <a name="destroyprotocol-function"></a>DestroyProtocol-Funktion

Die **DestroyProtocol-Funktion** zerstört das Protokoll, das von der **CreateProtocol-Funktion** erstellt wird.

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProtocol* \[ In\]
</dt> <dd>

Handle für das zu zerstörende Protokoll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Hinweise

Die Parser-DLL ruft die **DestroyProtocol-Funktion** während der Implementierung von [DllMain auf.](dllmain-parser.md) **DestroyProtocol** wird aufgerufen, wenn das Betriebssystem die DLL entlädt.



| Für Informationen zu                                        | Siehe                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor. | [Parser](parsers.md)                                  |
| Die Implementierung von **DllMain enthält** ein Beispiel.         | [Implementieren von DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




