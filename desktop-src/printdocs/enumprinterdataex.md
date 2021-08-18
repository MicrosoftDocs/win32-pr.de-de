---
description: Die EnumPrinterDataEx-Funktion listet alle Wertnamen und Daten für einen angegebenen Drucker und Schlüssel auf.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: EnumPrinterDataEx-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c1e78c17cccf416d186c4669e3576c5a0c9bf2365cb048a73b42d583b187156f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034268"
---
# <a name="enumprinterdataex-function"></a>EnumPrinterDataEx-Funktion

Die **EnumPrinterDataEx-Funktion** listet alle Wertnamen und Daten für einen angegebenen Drucker und Schlüssel auf.

Druckerdaten werden in der Registrierung gespeichert. Rufen Sie beim Aufzählen von Druckerdaten keine Registrierungsfunktionen auf, die die Daten möglicherweise ändern.

## <a name="syntax"></a>Syntax


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion Konfigurationsdaten abruft. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*pKeyName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Schlüssel angibt, der die aufzuzählenden Werte enthält. Verwenden Sie den umgekehrten Schrägstrich \\ () als Trennzeichen, um einen Pfad mit einem oder mehreren Unterschlüsseln anzugeben. **EnumPrinterDataEx** listet alle Werte des Schlüssels auf, zählt jedoch keine Werte von Unterschlüsseln des angegebenen Schlüssels auf. Verwenden Sie die [**EnumPrinterKey-Funktion,**](enumprinterkey.md) um Unterschlüssel aufzuzählen.

Wenn *pKeyName* **NULL** oder eine leere Zeichenfolge ist, gibt **EnumPrinterDataEx** ERROR \_ INVALID PARAMETER \_ zurück.

</dd> <dt>

*pEnumValues* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**PRINTER \_ ENUM \_ VALUES-Strukturen**](printer-enum-values.md) empfängt. Jede Struktur enthält den Wertnamen, den Typ, die Daten und die Größen eines Werts unter dem Schlüssel.

</dd> <dt>

*cbEnumValues* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *von "pwEnumValues"* verwiesen wird. Wenn Sie *cbEnumValues* auf 0 (null) festlegen, gibt der *parameter pwEnumValues* die erforderliche Puffergröße zurück.

</dd> <dt>

*pwEnumValues* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der abgerufenen Konfigurationsdaten in Bytes empfängt. Wenn die von *cbEnumValues* angegebene Puffergröße zu klein ist, gibt die Funktion ERROR \_ MORE \_ DATA zurück, und *"pwEnumValues"* gibt die erforderliche Puffergröße an.

</dd> <dt>

*pnEnumValues* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der in *pEnumValues* [**zurückgegebenen PRINTER \_ ENUM \_ VALUES-Strukturen**](printer-enum-values.md) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehlercode.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

**EnumPrinterDataEx** ruft das Druckerkonfigurationsdataset von den Funktionen [**SetPrinterDataEx**](setprinterdataex.md) und [**SetPrinterData**](setprinterdata.md) ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **EnumPrinterDataExW** (Unicode) und **EnumPrinterDataExA** (ANSI)<br/>                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_ \_ DRUCKERENUMERWERTE**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




