---
description: Die deleteprinterdataex-Funktion löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Deleteprinterdataex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757387"
---
# <a name="deleteprinterdataex-function"></a>Deleteprinterdataex-Funktion

Die **deleteprinterdataex** -Funktion löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz benannter und typisierter Werte, die in einer Hierarchie von Registrierungs Schlüsseln gespeichert sind. Die-Funktion löscht einen angegebenen Wert unter einem angegebenen Schlüssel.

Wie die [**deleteprinterdata**](deleteprinterdata.md) -Funktion kann **deleteprinterdataex** Werte löschen, die von der [**setprinterdata**](setprinterdata.md) -Funktion gespeichert werden. Außerdem kann **deleteprinterdataex** Werte löschen, die unter einem angegebenen Schlüssel von der [**setprinterdataex**](setprinterdataex.md) -Funktion gespeichert sind.

## <a name="syntax"></a>Syntax


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion einen Wert löscht. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Schlüssel mit dem zu löschenden Wert angibt. Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad anzugeben, der über mindestens einen Unterschlüssel verfügt.

Wenn *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **deleteprinterdataex** einen \_ ungültigen \_ Parameter zurück.

</dd> <dt>

*pvaluename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des zu löschenden Werts angibt.

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
| Unicode- und ANSI-Name<br/>   | **Deleteprinterdataexw** (Unicode) und **deleteprinterdataexa** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deleteprinterkey**](deleteprinterkey.md)
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

 

 




