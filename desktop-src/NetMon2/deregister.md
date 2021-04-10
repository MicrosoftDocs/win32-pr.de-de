---
description: Die Funktion zum Aufheben der Aufhebung der Funktion gibt die Ressourcen frei, die zum Erstellen der Protokoll Eigenschaften Datenbank verwendet werden. Die Parser-DLL muss die deregipperimplementierung implementieren.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Deregiester-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215889"
---
# <a name="deregister-callback-function"></a>Deregiester-Rückruffunktion

Die **Funktion zum Aufheben** der Aufhebung der Funktion gibt die Ressourcen frei, die zum Erstellen der Protokoll [*Eigenschaften Datenbank*](p.md)verwendet werden. Die Parser-DLL muss die **deregipperimplementierung** implementieren.

## <a name="syntax"></a>Syntax


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Handle des Protokolls für eine bestimmte Datenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Bemerkungen

Netzwerkmonitor Ruft die **deregitenregistrierung** auf, nachdem alle Aufzeichnungs Informationen an die Parser-DLL übergeben wurden. Die Parser-DLL muss eine **deregiester** -Funktion für jedes Protokoll implementieren, das der Parser unterstützt.

Beim Implementieren von **deregistern** muss die Parser-DLL die Funktion " [destroypropertydatabase](destroypropertydatabase.md) " aufrufen, um die [*Eigenschaften Daten Bank*](p.md) Ressourcen freizugeben.



| Für Informationen zu                                        | Siehe                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren. | [Parser](parsers.md)                                 |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Architektur der Parser-DLL](parser-dll-architecture.md) |
| Zum Implementieren der **deregiester**  gehört ein Beispiel.     | [Implementieren von deregistern](implementing-deregister.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Destroypropertydatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




