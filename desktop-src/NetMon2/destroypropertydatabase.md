---
description: Die Funktion "destroypropertydatabase" gibt die Ressourcen frei, die zum Erstellen der Protokoll Eigenschaften Datenbank verwendet werden.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Destroypropertydatabase-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960639"
---
# <a name="destroypropertydatabase-function"></a>Destroypropertydatabase-Funktion

Die Funktion " **destroypropertydatabase** " gibt die Ressourcen frei, die zum Erstellen der Protokoll [*Eigenschaften Datenbank*](p.md)verwendet werden.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Handle für die zu zerstörende Eigenschaften Datenbank. Das Handle wird an die Parser-DLL übergeben, wenn Netzwerkmonitor die [deregiester](deregister.md) -Funktion aufruft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                              | Beschreibung                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**Interner nmerr- \_ \_ Fehler**</dt> </dl>    | Interner Fehler. <br/>    |
| <dl> <dt>**nmerr \_ ungültiges \_ hprotocol**</dt> </dl> | Ungültiges Handle in *hprotocol*. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **destroypropertydatabase** -Funktion sollte nur aufgerufen werden, wenn [die Funktion](deregister.md) zum Aufheben der Aufhebung des Registrierungs Diensts für das Protokoll implementiert wird. Für Parser-DLLs, die mehrere Protokolle unterstützen, wird die Funktion " **destroypropertydatabase** " für jede Implementierung von " **deregiester**" aufgerufen.



| Für Informationen zu                                        | Siehe                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren. | [Parser](parsers.md)                                 |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Architektur der Parser-DLL](parser-dll-architecture.md) |
| Zum Implementieren der **deregiester**  gehört ein Beispiel.     | [Implementieren von deregistern](implementing-deregister.md) |



 

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

[Registrierung aufheben](deregister.md)
</dt> </dl>

 

 




