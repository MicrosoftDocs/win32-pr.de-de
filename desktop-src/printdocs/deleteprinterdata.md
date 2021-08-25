---
description: Die DeletePrinterData-Funktion löscht die angegebenen Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz benannter werte und typ benannter Werte. Die DeletePrinterData-Funktion löscht einen dieser Werte, der durch ihren Wertnamen angegeben wird.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: DeletePrinterData-Funktion (Winspool.h)
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
ms.openlocfilehash: 09600b2c84192378f654758a495ee22240211759fa0e961587ff70c7a10ac939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092130"
---
# <a name="deleteprinterdata-function"></a>DeletePrinterData-Funktion

Die **DeletePrinterData-Funktion** löscht die angegebenen Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typierten Werten. Die **DeletePrinterData-Funktion** löscht einen dieser Werte, der durch ihren Wertnamen angegeben wird.

Das **Aufrufen von DeletePrinterData** entspricht dem Aufrufen der [**DeletePrinterDataEx-Funktion,**](deleteprinterdataex.md) bei der der *pKeyName-Parameter* auf "PrinterDriverData" festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, dessen Konfigurationsdaten gelöscht werden sollen. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pValueName* \[ In\]
</dt> <dd>

Ein Zeiger auf den auf NULL beendeten Namen des zu löschenden Konfigurationsdatenwerts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehlercode.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **DeletePrinterDataW** (Unicode) und **DeletePrinterDataA** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrinterData**](enumprinterdata.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

 




