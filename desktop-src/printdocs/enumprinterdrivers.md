---
description: Die EnumPrinterDrivers-Funktion listet die druckertreiber auf, die auf einem angegebenen Druckerserver installiert sind.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: EnumPrinterDrivers-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7be4efb1de46a960508972b00d113c5a27ab57187c1a89475eebcde69f14d978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686732"
---
# <a name="enumprinterdrivers-function"></a>EnumPrinterDrivers-Funktion

Die **EnumPrinterDrivers-Funktion** listet die druckertreiber auf, die auf einem angegebenen Druckerserver installiert sind.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem die Druckertreiber aufzählt werden.

Wenn *pName* **NULL** ist, listet die Funktion die lokalen Druckertreiber auf.

</dd> <dt>

*pEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt (z. B. Windows x86, Windows IA64, Windows x64 oder Windows NT R4000). Wenn dieser Parameter **NULL** ist, verwendet die Funktion die aktuelle Umgebung des Aufrufers/Clients (nicht des Ziels/Servers).

Wenn die *pEnvironment-Zeichenfolge* "all" angibt, listet **EnumPrinterDrivers** Druckertreiber für alle auf dem angegebenen Server installierten Plattformen auf.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Der Im *pDriverInfo-Puffer* zurückgegebene Informationsstrukturtyp. Dies kann einer der folgenden Sein:



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

Ein Zeiger auf einen Puffer, der ein Array von DRIVER \_ INFO-Strukturen \_ \* empfängt, wie durch *Ebene* angegeben. Jede Struktur enthält Daten, die einen verfügbaren Druckertreiber beschreiben. Der Puffer muss groß genug sein, um das Array von Strukturen und alle Zeichenfolgen oder anderen Daten zu empfangen, auf die die Strukturmember zeigen.

Um die erforderliche Puffergröße zu bestimmen, rufen Sie **EnumPrinterDrivers** auf, wobei *cbBuf* auf 0 (null) festgelegt ist. **EnumPrinterDrivers** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ INSUFFICIENT BUFFER \_ zurück, und der parameter *pwNeeded* gibt die Größe des Puffers in Bytes zurück, der zum Speichern des Arrays von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pDriverInfo* zeigt

</dd> <dt>

*"Needed"* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der in den *pDriverInfo-Puffer* kopierten Bytes empfängt, wenn die Funktion erfolgreich ist. Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable empfängt die erforderliche Anzahl von Bytes.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im *pDriverInfo-Puffer* zurückgegebenen Strukturen empfängt. Dies ist die Anzahl der Druckertreiber, die auf dem angegebenen Druckerserver installiert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

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
| Unicode- und ANSI-Name<br/>   | **EnumPrinterDriversW** (Unicode) und **EnumPrinterDriversA** (ANSI)<br/>                           |



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

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

