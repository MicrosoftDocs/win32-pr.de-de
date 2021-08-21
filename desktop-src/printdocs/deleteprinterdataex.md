---
description: Die DeletePrinterDataEx-Funktion löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: DeletePrinterDataEx-Funktion (Winspool.h)
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
ms.openlocfilehash: 7a47b3a7a62ac9dd48a86a7ddf4d6634304a402b69d5dc191ce17e3f149ffb27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950070"
---
# <a name="deleteprinterdataex-function"></a>DeletePrinterDataEx-Funktion

Die **DeletePrinterDataEx-Funktion** löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz benannter und typisierter Werte, die in einer Hierarchie von Registrierungsschlüsseln gespeichert sind. Die Funktion löscht einen angegebenen Wert unter einem angegebenen Schlüssel.

Wie die [**DeletePrinterData-Funktion**](deleteprinterdata.md) kann **DeletePrinterDataEx** werte löschen, die von der [**SetPrinterData-Funktion**](setprinterdata.md) gespeichert wurden. Darüber hinaus kann **DeletePrinterDataEx** Werte löschen, die unter einem angegebenen Schlüssel von der [**SetPrinterDataEx-Funktion**](setprinterdataex.md) gespeichert sind.

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

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion einen Wert löscht. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*pKeyName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Schlüssel angibt, der den zu löschenden Wert enthält. Verwenden Sie den umgekehrten Schrägstrich \\ () als Trennzeichen, um einen Pfad anzugeben, der über einen oder mehrere Unterschlüssel verfügt.

Wenn *pKeyName* **NULL** oder eine leere Zeichenfolge ist, gibt **DeletePrinterDataEx** ERROR \_ INVALID PARAMETER \_ zurück.

</dd> <dt>

*pValueName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu löschenden Werts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehlercode.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **DeletePrinterDataExW** (Unicode) und **DeletePrinterDataExA** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterKey**](deleteprinterkey.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




