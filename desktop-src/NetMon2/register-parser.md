---
description: Die Register Export-Funktion muss in allen Parser-DLLs implementiert werden. Die Implementierung von Register erstellt und füllt eine Eigenschaften Datenbank für ein Protokoll aus. Netzwerkmonitor verwendet die-Datenbank, um zu bestimmen, welche Eigenschaften das Protokoll unterstützt.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Parser-Rückruffunktion registrieren (Netmon. h)
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
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347921"
---
# <a name="register-parser-callback-function"></a>Parser-Rückruffunktion registrieren

Die **Register** Export-Funktion muss in allen Parser-DLLs implementiert werden. Die Implementierung von **Register** erstellt und füllt eine [*Eigenschaften Datenbank*](p.md) für ein Protokoll aus. Netzwerkmonitor verwendet die-Datenbank, um zu bestimmen, welche Eigenschaften das Protokoll unterstützt.

## <a name="syntax"></a>Syntax


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Das Handle des Protokolls, das Netzwerkmonitor beim Aufrufen von **Register** bereitstellt. Das *hprotocol* -Handle wird benötigt, wenn Export-Hilfsfunktionen aufgerufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Bemerkungen

Netzwerkmonitor beginnt den Aufruf der **Register** Funktion, sobald eine Erfassung geladen wurde. Netzwerkmonitor Ruft die **Register** -Funktion für jedes Protokoll auf, das Sie identifizieren kann. Die Funktion "-Funktion" übergibt einen Zeiger an die **Register** [-Funktion.](createprotocol.md)

Die Implementierung von **Register** umfasst Aufrufe der folgenden Funktionen.

-   Ein Aufrufen der Funktionen " [deatepropertydatabase](createpropertydatabase.md) " und " [AddProperty](/previous-versions/bb251873(v=msdn.10)) " zum Erstellen einer Datenbank mit allen Eigenschaften, die das Protokoll unterstützt.
-   Wenn für das Protokoll ein [*Übergabe-Satz*](h.md)verwendet wird, ist ein Aufrufen der Funktion "| [atehandofftable](createhandofftable.md) " erforderlich.

Wenn die Parser-DLL mehrere Parser enthält und der Parser mehr als ein Protokoll erkennen kann, müssen Sie eine **Register** -Funktion für jedes Protokoll implementieren.



| Informationen zu                                        | Siehe                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren. | [Parser](parsers.md)                                 |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Architektur der Parser-DLL](parser-dll-architecture.md) |
| Zum Implementieren von **Register**  ist ein Beispiel enthalten.       | [Implementieren von Register](implementing-register.md)     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

["Kreatehandofftable"](createhandofftable.md)
</dt> <dt>

["Kreatepropertydatabase"](createpropertydatabase.md)
</dt> <dt>

["Kreateprotocol"](createprotocol.md)
</dt> </dl>

 

