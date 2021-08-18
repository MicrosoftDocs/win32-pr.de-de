---
description: Die GetPrinterDriver-Funktion ruft Treiberdaten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, wird er von GetPrinterDriver installiert.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: GetPrinterDriver-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 0a20cd1dedb515714565c1e94f7847fdfc5c7969429686f17682b76cfef070e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971379"
---
# <a name="getprinterdriver-function"></a>GetPrinterDriver-Funktion

Die **GetPrinterDriver-Funktion** ruft Treiberdaten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, wird er von **GetPrinterDriver** installiert.

## <a name="syntax"></a>Syntax


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, für den die Treiberdaten abgerufen werden sollen. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pUmgebung* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Umgebung angibt (z. B. Windows x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL ist,** wird die aktuelle Umgebung der aufrufenden Anwendung und des Clientcomputers (nicht der Zielanwendung und des Druckerservers) verwendet.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die im *pDriverInfo-Puffer zurückgegebene Druckertreiberstruktur.* Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine -Struktur empfängt, die Informationen zum Treiber enthält, wie von Level angegeben. Der Puffer muss groß genug sein, um die Zeichenfolgen zu speichern, auf die die Strukturmitglieder zeigt.

Um die erforderliche Puffergröße zu bestimmen, rufen **Sie GetPrinterDriver** mit *cbBuf* auf 0 (null) auf. **Bei GetPrinterDriver** tritt ein Fehler auf, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR INSUFFICIENT BUFFER zurück, und der \_ parameter \_ *"arraysNeeded"* gibt die Größe des Puffers in Bytes zurück, der zum Speichern des Arrays von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Arrays in Bytes, auf das *pDriverInfo* zeigt.

</dd> <dt>

*-Needed* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ist, oder die Erforderliche Anzahl von Bytes, wenn *cbBuf* zu klein ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Für einen nicht vorhandenen Treiber gibt die Funktion ERROR \_ UNKNOWN \_ PRINTER DRIVER \_ zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die [**Driver \_ INFO \_ 2-,**](driver-info-2.md) [**DRIVER INFO \_ \_ 3-,**](driver-info-3.md) [**DRIVER INFO \_ \_ 4-,**](driver-info-4.md) [**DRIVER INFO \_ \_ 5-**](driver-info-5.md)und [**DRIVER INFO \_ \_ 6-Strukturen**](driver-info-6.md) enthalten den Dateinamen oder den vollständigen Pfad und Dateinamen des Druckertreibers im **pDriverPath-Mitglied.** Eine Anwendung kann den Pfad und den Dateinamen verwenden, um einen Druckertreiber zu laden, indem sie die [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufruft und den Pfad und den Dateinamen als einzelnes Argument anordnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetPrinterDriverW** (Unicode) und **GetPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 1**](driver-info-1.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 5**](driver-info-5.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

