---
description: Die GetPrinter-Funktion ruft Informationen zu einem angegebenen Drucker ab.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: GetPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: b6823795ea715ac72dfdb7150dac08fd7feb34445fcfab94412cb2dd0c6bd7a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949089"
---
# <a name="getprinter-function"></a>GetPrinter-Funktion

Die **GetPrinter-Funktion** ruft Informationen zu einem angegebenen Drucker ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion Informationen abruft. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Ebene oder der Typ der Struktur, die die Funktion in dem Puffer speichert, auf den *pPrinter* zeigt.

Dieser Wert kann 1, 2, 3, 4, 5, 6, 7, 8 oder 9 sein.

</dd> <dt>

*pPrinter* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine -Struktur empfängt, die Informationen zum angegebenen Drucker enthält. Der Puffer muss groß genug sein, um die -Struktur und alle Zeichenfolgen oder andere Daten zu empfangen, auf die die Strukturmember zeigen. Wenn der Puffer zu klein ist, gibt der *Parameter "pwNeeded"* die erforderliche Puffergröße zurück.

Der Typ der Struktur wird durch den Wert von *Ebene* bestimmt.



| Ebene                                                                                                | Struktur                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 1-Struktur,**](printer-info-1.md) die allgemeine Druckerinformationen enthält.<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 2-Struktur,**](printer-info-2.md) die ausführliche Informationen zum Drucker enthält.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 3-Struktur,**](printer-info-3.md) die die Sicherheitsinformationen des Druckers enthält.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 4-Struktur**](printer-info-4.md) mit minimalen Druckerinformationen, einschließlich des Druckernamens, des Servernamens und der Angabe, ob der Drucker remote oder lokal ist.<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 5-Struktur,**](printer-info-5.md) die Druckerinformationen wie Druckerattribute und Time out-Einstellungen enthält.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 6-Struktur,**](printer-info-6.md) die den Statuswert eines Druckers angibt.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 7-Struktur,**](printer-info-7.md) die angibt, ob der Drucker im Verzeichnisdienst veröffentlicht wird.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 8-Struktur,**](printer-info-8.md) die die globalen Standarddruckereinstellungen angibt.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Eine [**PRINTER \_ INFO \_ 9-Struktur,**](printer-info-9.md) die die Standarddruckereinstellungen pro Benutzer angibt.<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pPrinter* zeigt.

</dd> <dt>

*"Needed"* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Funktion auf die Größe der Druckerinformationen in Bytes festlegt. Wenn *cbBuf* kleiner als dieser Wert ist, schlägt **GetPrinter** fehl, und der Wert stellt die erforderliche Puffergröße dar. Wenn *cbBuf* gleich oder größer als dieser Wert ist, ist **GetPrinter** erfolgreich, und der Wert stellt die Anzahl der im Puffer gespeicherten Bytes dar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Der **pDevMode-Member** in den Strukturen [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 8**](printer-info-8.md)und [**PRINTER INFO \_ \_ 9**](printer-info-9.md) kann **NULL** sein. In diesem Fall kann der Drucker erst verwendet werden, wenn der Treiber erfolgreich neu installiert wurde.

Für die Strukturen [**PRINTER \_ INFO \_ 2**](printer-info-2.md) und [**PRINTER INFO \_ \_ 3,**](printer-info-3.md) die einen Zeiger auf einen Sicherheitsdeskriptor enthalten, ruft die Funktion nur die Komponenten des Sicherheitsdeskriptors ab, die der Aufrufer lesen darf. Um bestimmte Sicherheitsbeschreibungskomponenten abzurufen, müssen Sie die erforderlichen Zugriffsrechte angeben, wenn Sie die [**OpenPrinter-Funktion**](openprinter.md) aufrufen, um ein Handle für den Drucker abzurufen. In der folgenden Tabelle sind die Zugriffsrechte aufgeführt, die zum Lesen der verschiedenen Sicherheitsbeschreibungskomponenten erforderlich sind.



| Zugriffsrecht                        | Sicherheitsbeschreibungskomponente                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| \_READ-STEUERELEMENT<br/>            | Besitzer<br/> Primäre Gruppe<br/> Dacl (Discretionary Access Control List)<br/> |
| ZUGREIFEN AUF \_ \_ SYSTEMSICHERHEIT<br/> | Systemzugriffssteuerungsliste (SACL)<br/>                                                  |



 

Wenn Sie Ebene 7 angeben, gibt das **dwAction-Element** von [**PRINTER INFO \_ \_ 7**](printer-info-7.md) einen der folgenden Werte zurück, um anzugeben, ob der Drucker im Verzeichnisdienst veröffentlicht wird.



| dwAction-Wert     | Bedeutung                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPRINT \_ PUBLISH   | Der Drucker wird veröffentlicht. Das **pszObjectGUID-Element** enthält die GUID des Druckwarteschlangenobjekts der Verzeichnisdienste, das dem Drucker zugeordnet ist.                                                                                                       |
| DSPRINT \_ UNPUBLISH | Der Drucker wird nicht veröffentlicht.                                                                                                                                                                                                                            |
| DSPRINT \_ AUSSTEHEND   | Gibt an, dass das System versucht, einen Veröffentlichungs- oder Nichtveröffentlichungsvorgang abzuschließen. Wenn ein [**SetPrinter-Aufruf**](setprinter.md) einen Drucker nicht veröffentlichen oder die Veröffentlichung aufheben kann, unternimmt das System weitere Versuche, den Vorgang im Hintergrund abzuschließen. |



 

Ab Windows Vista werden die von **GetPrinter** zurückgegebenen Druckerdaten aus einem lokalen Cache abgerufen, wenn *hPrinter* auf einen Drucker verweist, der von einem Druckerserver gehostet wird und mindestens eine offene Verbindung mit dem Druckerserver besteht. In allen anderen Konfigurationen werden die Druckerdaten vom Druckerserver abgefragt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetPrinterW** (Unicode) und **GetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AbortPrinter**](abortprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 7**](printer-info-7.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 8**](printer-info-8.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




