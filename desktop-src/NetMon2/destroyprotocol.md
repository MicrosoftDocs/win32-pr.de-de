---
description: Die Funktion "destroyprotocol" zerstört das Protokoll, das von der Funktion "kreateprotocol" erstellt wird.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Destroyprotocol-Funktion (Netmon. h)
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
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215888"
---
# <a name="destroyprotocol-function"></a>Destroyprotocol-Funktion

Die Funktion " **destroyprotocol** " zerstört das Protokoll, das von der Funktion " **kreateprotocol** " erstellt wird.

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Handle für das Protokoll, das zerstört werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Bemerkungen

Die Parser-DLL ruft die **destroyprotocol** -Funktion während der Implementierung von [DllMain](dllmain-parser.md)auf. **Destroyprotocol** wird aufgerufen, wenn das Betriebssystem die DLL entladen wird.



| Für Informationen zu                                        | Siehe                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren. | [Parser](parsers.md)                                  |
| Zur Implementierung von **DllMain** gehört ein Beispiel.         | [Implementieren von DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




