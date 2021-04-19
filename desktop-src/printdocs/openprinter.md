---
description: Die OpenPrinter-Funktion Ruft ein Handle für den angegebenen Drucker oder Druckserver oder andere Typen von Handles im Druck Subsystem ab.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: OpenPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349450"
---
# <a name="openprinter-function"></a>OpenPrinter-Funktion

Die **OpenPrinter** -Funktion Ruft ein Handle für den angegebenen Drucker oder Druckserver oder andere Typen von Handles im Druck Subsystem ab.

## <a name="syntax"></a>Syntax


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprintername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers oder Druck Servers, das Drucker Objekt, den xcvmonitor oder den xcvport angibt.

Verwenden Sie für ein Drucker Objekt: PrinterName, Job xxxx. Verwenden Sie für einen xcvmonitor Folgendes: Servername, xcvmonitor Monitorname. Verwenden Sie für einen xcvport: Servername, xcvport PORTNAME.

Wenn der Wert **null** ist, wird der lokale Drucker Server angegeben.

</dd> <dt>

*phprinter* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle (nicht Thread sicher) für den geöffneten Drucker oder das Druckserver Objekt empfängt.

Der Parameter " *phprinter* " kann ein XCV-Handle für die Verwendung mit der XcvData-Funktion zurückgeben. Weitere Informationen zu XcvData finden Sie unter DDK.

</dd> <dt>

*pdefault* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Drucker \_ Standard**](printer-defaults.md) Struktur. Dieser Wert kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.

> [!Note]  
> Ein Handle, das für einen Remote Drucker durch einen **OpenPrinter** -aufrufbefehl für einen Remote Drucker abgerufen wird, greift über einen lokalen Cache im Druckspoolerdienst auf den Drucker zu. Dieser Cache ist nicht echt Zeit genau. Um genaue Daten zu erhalten, ersetzen Sie den OpenPrinter-Befehl durch [**OpenPrinter2**](openprinter2.md) durch poptions. dwFlags, die auf Drucker \_ Option \_ kein Cache festgelegt sind \_ . Beachten Sie, dass nur OpenPrinter2W funktionsfähig ist. Die-Funktion gibt ein Drucker Handle zurück, das andere Druck-API-Aufrufe verwendet und den lokalen Cache umgeht. Diese Methode blockiert, während auf die Netzwerkkommunikation mit dem Remote Drucker gewartet wird, sodass Sie möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, wird die Anwendung möglicherweise nicht mehr reagiert.

 

> [!Note]  
> Ein Handle, das durch einen **OpenPrinter** -Aufrufvorgang für einen Remote Drucker abgerufen wird, greift über einen lokalen Cache im Druckspoolerdienst auf den Drucker zu. Bei diesem Cache handelt es sich nicht um echtzeitgenauigkeit. Wenn Sie genaue Daten abrufen müssen, ersetzen Sie den **OpenPrinter** -Befehl durch [**OpenPrinter2**](openprinter2.md) durch " *poptions. dwFlags* ", der auf " [**Printer \_ Option \_ No \_ Cache**](printer-options.md)" festgelegt ist. Beachten Sie, dass nur **OpenPrinter2W** funktionsfähig ist. Dadurch gibt die Funktion ein Drucker Handle zurück, das andere Druck-API-Aufrufe ausführt, um den lokalen Cache zu umgehen. Beachten Sie, dass diese Vorgehensweise beim Warten auf die Roundtrip-Netzwerkkommunikation mit dem Remote Drucker blockiert wird, sodass Sie möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von den Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Druckertreiber Implementierung: Faktoren, die beim Schreiben einer Anwendung schwer vorhergesagt werden können. Wenn Sie diese Funktion aus einem Thread aufrufen, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte es vorkommen, dass die Anwendung nicht mehr reagiert.

 

Das Handle, auf das von *phprinter* verwiesen wird, ist nicht Thread sicher. Wenn Aufrufer Sie gleichzeitig für mehrere Threads verwenden müssen, müssen Sie den benutzerdefinierten Synchronisierungs Zugriff auf das Drucker Handle mithilfe der [Synchronisierungs Funktionen](/windows/desktop/Sync/synchronization-functions)bereitstellen. Um das Schreiben von benutzerdefiniertem Code zu vermeiden, kann die Anwendung bei Bedarf ein Drucker Handle für jeden Thread öffnen.

Mit dem *pdefault* -Parameter können Sie die Werte für Datentyp und Geräte Modus angeben, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter**](startdocprinter.md) -Funktion übermittelt werden. Sie können diese Werte jedoch überschreiben, indem Sie die Funktion [**setjob**](setjob.md) verwenden, nachdem ein Dokument gestartet wurde.

Die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Einstellungen, die in der [**Drucker \_ Standard**](printer-defaults.md) Struktur des *pdefault* -Parameters definiert sind, werden nicht verwendet, wenn der Wert des *pdatatype* -Members der [**doc \_ Info \_ 1**](doc-info-1.md) -Struktur, die im *pdocinfo* -Parameter des [**StartDocPrinter**](startdocprinter.md) -Aufrufes übergeben wurde, "RAW" lautet. Wenn ein Dokument auf hoher Ebene (z. b. eine Adobe PDF-oder Microsoft Word-Datei) oder andere Druckerdaten (z. b. PCL, PS oder HPGL) direkt an einen Drucker gesendet werden, bei dem *pdatatype* auf "RAW" festgelegt ist, muss das Dokument die Einstellungen des Druckauftrags im **DEVMODE**-Stil in der Sprache beschreiben, die von

Sie können die **OpenPrinter** -Funktion aufrufen, um ein Handle für einen Drucker Server zu öffnen oder um die Zugriffsrechte zu ermitteln, die ein Client auf einen Druckserver hat. Geben Sie hierzu den Namen des Drucker Servers im *pprintername* -Parameter an, legen Sie die **pdatatype** -und **pdevmode** -Member der [**\_ Standard**](printer-defaults.md) Struktur der Drucker Standards auf **null** fest, und legen Sie das **desiredAccess** -Element auf einen Server Zugriffs Maskenwert fest, wie z \_ . b. Zugriff auf den Server \_ . Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**closeprinter**](closeprinter.md) -Funktion, um es zu schließen.

Verwenden Sie das **desiredAccess** -Mitglied [**der \_ Drucker Standard**](printer-defaults.md) Struktur, um die Zugriffsrechte anzugeben, die Sie für den Drucker benötigen. Die Zugriffsrechte können eines der folgenden sein: (Wenn *pdefault* den Wert **null** hat, sind die Zugriffsrechte Drucker \_ . Zugriffs \_ Verwendung.)



| Gewünschter Zugriffs Wert                        | Bedeutung                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drucker \_ Zugriffs \_ Verwaltung                 | Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md)bereitgestellten.                                                                                                 |
| Drucker \_ Zugriffs \_ Verwendung                        | Zum Ausführen grundlegender Druckvorgänge.                                                                                                                                                        |
| Drucker \_ \_ Zugriff                        | Zum Ausführen aller Verwaltungsaufgaben und grundlegenden Druckvorgänge mit Ausnahme von Synchronisierung (siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)).                                     |
| Drucker \_ Zugriff \_ mit \_ eingeschränkter Verwaltung            | Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md) und [**setprinterdata**](setprinterdata.md)bereitgestellten. Dieser Wert ist ab Windows 8.1 verfügbar. |
| generische Sicherheitswerte, z. b. \_ DAC schreiben | , Um bestimmte Zugriffsrechte für das Steuerelement zuzulassen. Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Wenn ein Benutzer nicht berechtigt ist, einen angegebenen Drucker oder Druckserver mit dem gewünschten Zugriff zu öffnen, schlägt der **OpenPrinter** -Rückruf mit dem Rückgabewert NULL fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Wert für den Fehler \_ Zugriff verweigert zurück \_ .

## <a name="examples"></a>Beispiele

Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Openprinterw** (Unicode) und **openprintera** (ANSI)<br/>                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**"Write Printer"**](writeprinter.md)
</dt> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Drucker \_ Standardwerte**](printer-defaults.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

