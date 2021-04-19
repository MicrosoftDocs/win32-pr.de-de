---
description: Die Funktion "| atehandofftable" erstellt eine Übergabe Tabelle, die die in der INI-Datei des Parsers gespeicherten Übergabe-Informationen enthält.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Funktion "anatehandofftable" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355689"
---
# <a name="createhandofftable-function"></a>"Anatehandofftable"-Funktion

Die Funktion "| **atehandofftable** " erstellt eine [*Übergabe Tabelle*](h.md) , die die in der INI-Datei des Parsers gespeicherten Übergabe-Informationen enthält.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*secname* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Abschnitt der INI-Datei angibt, in der sich die handaus Satz Informationen befinden.

</dd> <dt>

*IniFile* \[ in\]
</dt> <dd>

Zeichenfolge, die den Namen der INI-Datei des Parsers enthält.

</dd> <dt>

*htable* \[ vorgenommen\]
</dt> <dd>

Handle für eine **handofftable** -Struktur, die von Netzwerkmonitor erstellt und verwaltet wird.

</dd> <dt>

*nmaxprotocolentries* \[ in\]
</dt> <dd>

Zahl, die die maximale Anzahl von Einträgen angibt, die von der Übergabe-Tabelle verarbeitet werden können.

</dd> <dt>

*Basis* \[ in\]
</dt> <dd>

Numerische Basis der Übergabe Satz Nummern, die in der INI-Datei gespeichert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Anzahl der Einträge in der Übergabe-Tabelle.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Die von Netzwerkmonitor erstellte Übergabe Tabelle basiert auf Informationen, die in der-Parser-ini bereitgestellt werden. Der zurückgegebene Handle der Übergabe-Tabelle kann dann verwendet werden, um ein Handle für eines der in der Tabelle enthaltenen Protokolle abzurufen. Rufen Sie [getprotocolfromtable](getprotocolfromtable.md)auf, um ein Handle für eines dieser Protokolle zu erhalten.

Beachten Sie, dass die parseranwendung niemals direkt auf die **handofftable** -Struktur zugreift. Diese Struktur wird von Netzwerkmonitor erstellt und verwaltet.

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

[Getprotocolfromtable](getprotocolfromtable.md)
</dt> <dt>

[Handofftable](handofftable.md)
</dt> </dl>

 

 




