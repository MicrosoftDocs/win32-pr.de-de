---
description: Die deleteprinterdata-Funktion löscht die angegebenen Konfigurationsdaten für einen Drucker. Ein Drucker Konfigurationsdaten besteht aus einem Satz benannter und typisierter Werte. Die deleteprinterdata-Funktion löscht einen dieser Werte, der durch den Wert Namen angegeben wird.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: Deleteprinterdata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345309"
---
# <a name="deleteprinterdata-function"></a>Deleteprinterdata-Funktion

Die **deleteprinterdata** -Funktion löscht die angegebenen Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typisierten Werten. Die **deleteprinterdata** -Funktion löscht einen dieser Werte, der durch den Wert Namen angegeben wird.

Das Aufrufen von **deleteprinterdata** entspricht dem Aufrufen der [**deleteprinterdataex**](deleteprinterdataex.md) -Funktion, wobei der *pkeyname* -Parameter auf "printerdriverdata" festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, dessen Konfigurationsdaten gelöscht werden sollen. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pvaluename* \[ in\]
</dt> <dd>

Ein Zeiger auf den null-terminierten Namen des zu löschenden Konfigurationsdaten Werts.

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
| Unicode- und ANSI-Name<br/>   | **Deleteprinterdataw** (Unicode) und **deleteprinterdataa** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Enumprinterdata**](enumprinterdata.md)
</dt> <dt>

[**Getprinterdata**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Setprinterdata**](setprinterdata.md)
</dt> </dl>

 

 




