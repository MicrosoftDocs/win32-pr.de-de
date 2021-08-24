---
description: Die CreateHandoffTable-Funktion erstellt eine Übergabetabelle, die die in der INI-Datei des Parsers gespeicherten Handoffsetinformationen enthält.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: CreateHandoffTable-Funktion (Netmon.h)
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
ms.openlocfilehash: 70709223d5dcebcae819389feb8623006b793126a911fc674491b1d665268056
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911200"
---
# <a name="createhandofftable-function"></a>CreateHandoffTable-Funktion

Die **CreateHandoffTable-Funktion** erstellt eine [*Übergabetabelle,*](h.md) die die in der INI-Datei des Parsers gespeicherten Handoffsetinformationen enthält.

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

*secName* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die den Abschnitt der INI-Datei angibt, in dem sich die Informationen zum Übergabesatz befinden.

</dd> <dt>

*iniFile* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der PARSER-INI-Datei enthält.

</dd> <dt>

*hTable* \[ out\]
</dt> <dd>

Handle für eine **HANDOFFTABLE-Struktur,** die von einem -Netzwerkmonitor.

</dd> <dt>

*nMaxProtocolEntries* \[ In\]
</dt> <dd>

Zahl, die die maximale Anzahl von Einträgen angibt, die die Übergabetabelle verarbeiten kann.

</dd> <dt>

*base* \[ In\]
</dt> <dd>

Numerische Basis der in der INI-Datei gespeicherten Übergabesatznummern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Anzahl der Einträge in der Übergabetabelle.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Die von Netzwerkmonitor Handofftabelle basiert auf Informationen, die im Parser-INI bereitgestellt werden. Das zurückgegebene Handle für die Übergabetabelle kann dann verwendet werden, um ein Handle für eines der in der Tabelle enthaltenen Protokolle zu erhalten. Um ein Handle eines dieser Protokolle zu erhalten, rufen [Sie GetProtocolFromTable auf.](getprotocolfromtable.md)

Beachten Sie, dass die Parseranwendung nie direkt auf die **HANDOFFTABLE-Struktur** zutritt. Diese Struktur wird von der -Netzwerkmonitor.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




