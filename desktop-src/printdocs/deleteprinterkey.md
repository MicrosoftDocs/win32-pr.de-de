---
description: Die deleteprinterkey-Funktion löscht einen angegebenen Schlüssel und alle zugehörigen Unterschlüssel für einen angegebenen Drucker.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Deleteprinterkey-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757747"
---
# <a name="deleteprinterkey-function"></a>Deleteprinterkey-Funktion

Die **deleteprinterkey** -Funktion löscht einen angegebenen Schlüssel und alle zugehörigen Unterschlüssel für einen angegebenen Drucker.

## <a name="syntax"></a>Syntax


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion einen Schlüssel löscht. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den zu löschenden Schlüssel angibt. Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad mit einem oder mehreren unter Schlüsseln anzugeben.

Wenn *pkeyname* eine leere Zeichenfolge ("") ist, löscht **deleteprinterkey** alle Schlüssel unter dem Schlüssel der obersten Ebene für den Drucker. Wenn *pkeyname* **null** ist, gibt **deleteprinterkey** einen \_ ungültigen \_ Parameter zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Deleteprinterkeyw** (Unicode) und **deleteprinterkeya** (ANSI)<br/>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deleteprinterdataex**](deleteprinterdataex.md)
</dt> <dt>

[**Enumprinterdataex**](enumprinterdataex.md)
</dt> <dt>

[**Enumprinterkey**](enumprinterkey.md)
</dt> <dt>

[**Getprinterdataex**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinterdataex**](setprinterdataex.md)
</dt> </dl>

 

 




