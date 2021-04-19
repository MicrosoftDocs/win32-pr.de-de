---
description: Die Funktion "-Funktion" erstellt eine Eigenschaften Datenbank, in der die Eigenschaften eines Protokolls gespeichert werden.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Funktion "up propertydatabase" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348591"
---
# <a name="createpropertydatabase-function"></a>Funktion "up propertydatabase"

Die **Funktion "** -Funktion" erstellt eine Eigenschaften Datenbank, in der die Eigenschaften eines Protokolls gespeichert werden.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Handle des Protokolls, das der Datenbank zugeordnet ist. Wenn Netzwerkmonitor die [Register](register-parser.md) -Funktion aufruft, übergibt Netzwerkmonitor das Protokoll Handle an die Parser-DLL.

</dd> <dt>

*nproperties* \[ in\]
</dt> <dd>

Anzahl der in der Datenbank gespeicherten Eigenschaften. Legen Sie diesen Parameter auf die Anzahl der Eigenschaften fest, die das Protokoll unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                             | Beschreibung                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**Interner nmerr- \_ \_ Fehler**</dt> </dl>   | Ein interner Fehler ist aufgetreten.<br/>                                     |
| <dl> <dt>**nmerr \_ ungültige \_ hpotocol.**</dt> </dl> | Das Handle für das in *hprotocol* angegebene Protokoll ist ungültig.<br/>     |
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl>   | Netzwerkmonitor verfügt nicht über genügend Arbeitsspeicher, um die Datenbank zu erstellen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Funktion " **deatepropertydatabase** " sollte nur aufgerufen werden, wenn die [Register](register-parser.md) Funktion implementiert wird. Der Parser erstellt mithilfe von " **kreatepropertydatabase** " eine Eigenschaften Datenbank, in der die Eigenschaften eines Protokolls beschrieben werden. Netzwerkmonitor verwendet die Datenbank, um die Informationen innerhalb des Protokolls zu interpretieren.

Die Funktion " **kreatepropertydatabase** " ordnet die Strukturen zu, die Netzwerkmonitor für die Wartung einer Eigenschaften Datenbank benötigt.

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

[Registrieren](register-parser.md)
</dt> </dl>

 

 




