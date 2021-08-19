---
description: Die CreatePropertyDatabase-Funktion erstellt eine Eigenschaftendatenbank, in der die Eigenschaften eines Protokolls gespeichert werden.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: CreatePropertyDatabase-Funktion (Netmon.h)
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
ms.openlocfilehash: 7c07f6f3e4569c06f0b3890e3ef3a26bca10b3272849fc005dfb3be6cbc2836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367217"
---
# <a name="createpropertydatabase-function"></a>CreatePropertyDatabase-Funktion

Die **CreatePropertyDatabase-Funktion** erstellt eine Eigenschaftendatenbank, in der die Eigenschaften eines Protokolls gespeichert werden.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProtocol* \[ In\]
</dt> <dd>

Handle des Protokolls, das der Datenbank zugeordnet ist. Wenn Netzwerkmonitor die [Register-Funktion aufruft,](register-parser.md) übergibt Netzwerkmonitor Protokollhand handle an die Parser-DLL.

</dd> <dt>

*nEigenschaften* \[ In\]
</dt> <dd>

Anzahl der in der Datenbank gespeicherten Eigenschaften. Legen Sie diesen Parameter auf die Anzahl der Eigenschaften fest, die das Protokoll unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                             | Beschreibung                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**INTERNER \_ NMERR-FEHLER \_**</dt> </dl>   | Ein interner Fehler ist aufgetreten.<br/>                                     |
| <dl> <dt>**NMERR \_ INVALID \_ HPTOMCOL**</dt> </dl> | Das Handle für das in *hProtocol* angegebene Protokoll ist ungültig.<br/>     |
| <dl> <dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>   | Netzwerkmonitor nicht über genügend Arbeitsspeicher zum Erstellen der Datenbank verfügt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **CreatePropertyDatabase-Funktion** sollte nur aufgerufen werden, wenn die [Register-Funktion implementieren](register-parser.md) wird. Der Parser verwendet **CreatePropertyDatabase,** um eine Eigenschaftendatenbank zu erstellen, die die Eigenschaften eines Protokolls beschreibt. Netzwerkmonitor verwendet die Datenbank, um die Informationen innerhalb des Protokolls zu interpretieren.

Die **CreatePropertyDatabase-Funktion** ordnet die Strukturen zu, Netzwerkmonitor eine Eigenschaftendatenbank verwalten müssen.

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

[Registrieren](register-parser.md)
</dt> </dl>

 

 




