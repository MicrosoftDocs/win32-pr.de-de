---
description: Die Exportfunktion "Registrierung aufheben" gibt die Ressourcen frei, die zum Erstellen der Protokolleigenschaftsdatenbank verwendet werden. Die Parser-DLL muss Deregister implementieren.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Rückruffunktion aufheben (Netmon.h)
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
ms.openlocfilehash: cb06ab6e08a674a186bcdb260140915c378db9affc13b17db33d9132109cec78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911220"
---
# <a name="deregister-callback-function"></a>Rückruffunktion "Registrierung aufheben"

Die Exportfunktion **"Registrierung** aufheben" gibt die Ressourcen frei, die zum Erstellen der [*Protokolleigenschaftsdatenbank*](p.md)verwendet werden. Die Parser-DLL muss **deregister** implementieren.

## <a name="syntax"></a>Syntax


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProtocol* \[ In\]
</dt> <dd>

Handle des Protokolls für eine bestimmte Datenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Hinweise

Netzwerkmonitor ruft **die Registrierung auf,** nachdem alle Erfassungsinformationen an die Parser-DLL übergeben wurden. Die Parser-DLL muss eine **Deregister-Funktion** für jedes Protokoll implementieren, das der Parser unterstützt.

Beim Implementieren von **Deregister** muss die Parser-DLL die [DestroyPropertyDatabase-Funktion](destroypropertydatabase.md) aufrufen, um die [*Eigenschaftendatenbankressourcen*](p.md) freizugeben.



| Für Informationen zu                                        | Siehe                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor arbeiten. | [Parser](parsers.md)                                 |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Parser-DLL-Architektur](parser-dll-architecture.md) |
| Das Implementieren von **"Deregister"**  enthält ein Beispiel.     | [Implementieren der Registrierung](implementing-deregister.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




