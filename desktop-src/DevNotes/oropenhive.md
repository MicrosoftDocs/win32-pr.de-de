---
description: Lädt die angegebene Registrierungs Struktur Datei in den Arbeitsspeicher und überprüft die Hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Oropenhive-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367725"
---
# <a name="oropenhive-function"></a>Oropenhive-Funktion

Lädt die angegebene Registrierungs Struktur Datei in den Arbeitsspeicher und überprüft die Hive.

## <a name="syntax"></a>Syntax


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lphivepath* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen der Hive-Registrierungsdatei angibt, die in den Arbeitsspeicher geladen werden soll. Dabei kann es sich um eine Hive-Datei handeln, die mit der [**orsavehive**](orsavehive.md) -Funktion gespeichert oder mit der [regsavekey](/windows/win32/api/winreg/nf-winreg-regsavekeya) -Funktion oder der [regsavekeyex](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) -Funktion erstellt wurde. Die Datei muss weniger als 4 GB groß sein, und der Aufrufer muss über Datei \_ Lese \_ Zugriff auf die Datei verfügen. Weitere Informationen finden Sie unter [Datei Sicherheit und Zugriffsrechte](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*phkResult* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle für den Stamm Schlüssel der geladenen Offline Registrierungs Struktur empfängt. Wenn die Hive-Registrierungsdatei nicht geöffnet werden kann oder die Validierung fehlschlägt, legt die Funktion diesen Parameter auf **null** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten. Folgende Fehlercodes sind möglich:

-   Wenn die Datei leer oder größer als 4 GB ist, gibt die Funktion den Fehler \_ baddb zurück.
-   Wenn der Aufrufer nicht über die erforderlichen Zugriffsrechte verfügt, um die Datei zu öffnen, gibt die Funktion den Fehler \_ Zugriff \_ verweigert zurück.
-   Wenn die Überprüfung der Registrierungs Struktur fehlschlägt, gibt die Funktion die Fehlermeldung \_ nicht die \_ Registrierungs \_ Datei zurück.

## <a name="remarks"></a>Bemerkungen

Die **oropenhive** -Funktion ist die einzige Offline-Registrierungsfunktion, die eine Registrierungs Struktur überprüft. Wenn die Überprüfung fehlschlägt, wird nicht versucht, die Struktur zu reparieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orclosehive**](orclosehive.md)
</dt> <dt>

[**Orkreatehive**](orcreatehive.md)
</dt> <dt>

[**Orsavehive**](orsavehive.md)
</dt> <dt>

[Regsavekey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[Regsavekeyex](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
