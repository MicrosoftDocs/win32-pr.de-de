---
description: Die Funktion "Write Printer" benachrichtigt den Druck Spooler, dass Daten in den angegebenen Drucker geschrieben werden sollen.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Funktion "Write Printer" (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358916"
---
# <a name="writeprinter-function"></a>Funktion "Write Printer"

Die Funktion " **Write Printer** " benachrichtigt den Druck Spooler, dass Daten in den angegebenen Drucker geschrieben werden sollen.

> [!Note]  
> " **Write Printer** " unterstützt nur den GDI-Druck und darf nicht für den XPS-Druck verwendet werden. Wenn der Druckauftrag den XPS-oder den openxps-Druckpfad verwendet, verwenden Sie die [XPS-Druck-API](/windows/desktop/printdocs/xps-printing). Das Senden von XPS-oder openxps-Druckaufträgen an den Spooler mithilfe von " **Write Printer** " wird nicht unterstützt und kann zu unbestimmten Ergebnissen führen.

 

## <a name="syntax"></a>Syntax


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*PBUF* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Daten enthält, die in den Drucker geschrieben werden sollen.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe des Arrays in Bytes.

</dd> <dt>

*pcwritten* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der Daten Bytes empfängt, die an den Drucker geschrieben wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die Reihenfolge für einen Druckauftrag lautet wie folgt:

1.  Zum Starten eines Druckauftrags aufrufen Sie [**StartDocPrinter**](startdocprinter.md).
2.  Um jede Seite zu starten, aufrufen Sie [**startpageprinter**](startpageprinter.md).
3.  Um Daten auf eine Seite zu schreiben, müssen Sie " **Write-Printer**" anrufen.
4.  Um jede Seite zu beenden, nennen Sie [**endpageprinter**](endpageprinter.md).
5.  Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.
6.  Um den Druckauftrag zu beenden, nennen Sie [**enddocprinter**](enddocprinter.md).

Wenn ein Dokument auf hoher Ebene (z. b. eine Adobe PDF-oder Microsoft Word-Datei) oder andere Druckerdaten (z. b. PCL, PS oder HPGL) direkt an einen Drucker gesendet werden, werden die im Dokument definierten Druckeinstellungen im Vergleich zu den Windows-Druckeinstellungen Vorrang haben. Dokumente, die ausgegeben werden, wenn der Wert des *pdatatype* -Members der [**doc \_ Info \_ 1**](doc-info-1.md) -Struktur, die im *pdocinfo* -Parameter des [**StartDocPrinter**](startdocprinter.md) -Aufrufes aufgerufen wurde, "RAW" ist, muss die Einstellungen des Druckauftrags im [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-Stil in der von der Hardware erkannten Sprache vollständig beschreiben.

Wenn in Windows-Versionen vor Windows XP eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet. Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden. Die Seitengrößen Beschränkung in Windows-Versionen vor Windows XP hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Arbeitsspeichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap. In Windows XP und höheren Versionen von Windows müssen EMF-Dateien 2 GB oder weniger groß sein. Wenn zum Schreiben von nicht-EMF-Daten (z. b. Drucker bereite PDL) **der Schreibschutz** verwendet wird, wird die Dateigröße nur durch den verfügbaren Speicherplatz beschränkt.

## <a name="examples"></a>Beispiele

Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Enddocprinter**](enddocprinter.md)
</dt> <dt>

[**Endpageprinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Startpageprinter**](startpageprinter.md)
</dt> <dt>

[**"Write Printer"**](writeprinter.md)
</dt> </dl>

 

