---
description: Die Exportfunktion Register muss in allen Parser-DLLs implementiert werden. Die Implementierung von Register erstellt und füllt eine Eigenschaftendatenbank für ein Protokoll auf. Netzwerkmonitor verwendet die Datenbank, um zu bestimmen, welche Eigenschaften das Protokoll unterstützt.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Registrieren der Parser-Rückruffunktion (Netmon.h)
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
ms.openlocfilehash: 4c24f719018f155fab26df4673b7dc3be18546675532657cb8fb3a0271763af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128920"
---
# <a name="register-parser-callback-function"></a>Register Parser callback function (Parser-Rückruffunktion registrieren)

Die **Exportfunktion Register** muss in allen Parser-DLLs implementiert werden. Die Implementierung von **Register** erstellt und füllt eine [*Eigenschaftendatenbank*](p.md) für ein Protokoll auf. Netzwerkmonitor verwendet die Datenbank, um zu bestimmen, welche Eigenschaften das Protokoll unterstützt.

## <a name="syntax"></a>Syntax


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProtocol* \[ In\]
</dt> <dd>

Das Handle des Protokolls, das Netzwerkmonitor beim Aufrufen von **Register** bereitstellt. Das *hProtocol-Handle* wird beim Aufrufen von Exporthilfsfunktionen benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Hinweise

Netzwerkmonitor beginnt mit dem  Aufrufen der Register-Funktion, sobald eine Erfassung geladen wird. Netzwerkmonitor ruft die **Register-Funktion** für jedes Protokoll auf, das identifiziert werden kann. Die [CreateProtocol-Funktion](createprotocol.md) übergibt einen Zeiger auf die **Register-Funktion.**

Die Implementierung von **Register** umfasst Aufrufe der folgenden Funktionen.

-   Ein Aufruf der Funktionen [CreatePropertyDatabase](createpropertydatabase.md) und [AddProperty,](/previous-versions/bb251873(v=msdn.10)) um eine Datenbank mit allen Eigenschaften zu erstellen, die das Protokoll unterstützt.
-   Ein Aufruf der [CreateHandoffTable-Funktion](createhandofftable.md) ist erforderlich, wenn das Protokoll einen [*Übergabesatz verwendet.*](h.md)

Wenn die Parser-DLL mehrere Parser enthält und der Parser mehrere Protokolle erkennen kann, müssen Sie für jedes Protokoll eine **Register-Funktion** implementieren.



| Informationen zu                                        | Siehe                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor arbeiten. | [Parser](parsers.md)                                 |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Parser-DLL-Architektur](parser-dll-architecture.md) |
| Das Implementieren von **Register**  enthält ein Beispiel.       | [Implementieren von Registern](implementing-register.md)     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Addproperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> <dt>

[CreatePropertyDatabase](createpropertydatabase.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> </dl>

 

