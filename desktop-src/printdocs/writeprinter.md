---
description: Die WritePrinter-Funktion benachrichtigt den Druckspooler, dass Daten auf den angegebenen Drucker geschrieben werden sollen.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: WritePrinter-Funktion (Winspool.h)
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
ms.openlocfilehash: 4b8b413854f8634477f7fec9010f4306587a093bd5c791b1b7d0117b6c3ef91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971159"
---
# <a name="writeprinter-function"></a>WritePrinter-Funktion

Die **WritePrinter-Funktion** benachrichtigt den Druckspooler, dass Daten auf den angegebenen Drucker geschrieben werden sollen.

> [!Note]  
> **WritePrinter unterstützt** nur GDI-Druck und darf nicht für XPS-Druck verwendet werden. Wenn Ihr Druckauftrag den XPS- oder OpenXPS-Druckpfad verwendet, verwenden Sie die [XPS-Druck-API](/windows/desktop/printdocs/xps-printing). Das Senden von XPS- oder OpenXPS-Druckaufträgen an den Spooler mit **WritePrinter** wird nicht unterstützt und kann zu unbestimmten Ergebnissen führen.

 

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

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pBuf* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Daten enthält, die auf den Drucker geschrieben werden sollen.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Arrays in Bytes.

</dd> <dt>

*pcWritten* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der Bytes von Daten empfängt, die auf den Drucker geschrieben wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die Sequenz für einen Druckauftrag lautet wie folgt:

1.  Um einen Druckauftrag zu starten, rufen [**Sie StartDocPrinter auf.**](startdocprinter.md)
2.  Um jede Seite zu starten, rufen [**Sie StartPagePrinter auf.**](startpageprinter.md)
3.  Um Daten auf eine Seite zu schreiben, rufen Sie **WritePrinter auf.**
4.  Um jede Seite zu beenden, rufen Sie [**EndPagePrinter auf.**](endpageprinter.md)
5.  Wiederholen Sie 2, 3 und 4 für so viele Seiten wie erforderlich.
6.  Um den Druckauftrag zu beenden, rufen Sie [**EndDocPrinter auf.**](enddocprinter.md)

Wenn ein Dokument auf hoher Ebene (z. B. eine Adobe PDF- oder Microsoft Word-Datei) oder andere Druckerdaten (z. B. PCL, PS oder HPGL) direkt an einen Drucker gesendet werden, haben die im Dokument definierten Druckeinstellungen Vorrang vor Windows-Druckeinstellungen. Dokumentiert die Ausgabe, wenn der Wert des *pDatatype-Members* der [**DOC INFO \_ \_ 1-Struktur,**](doc-info-1.md) der im *pDocInfo-Parameter* des [**StartDocPrinter-Aufrufs**](startdocprinter.md) übergeben wurde, "RAW" ist, die DevMODE-Druckauftragseinstellungen in der sprache, die von der Hardware verstanden wird, vollständig beschreiben muss. [](/windows/win32/api/wingdi/ns-wingdi-devmodea)

In Versionen von Windows vor Windows XP kann eine Seite in einer Spooldatei, die ungefähr 350 MB überschreitet, nicht gedruckt werden und keine Fehlermeldung senden. Dies kann beispielsweise beim Drucken großer EMF-Dateien auftreten. Die Seitengrößenbeschränkung in Versionen von Windows vor Windows XP hängt von vielen Faktoren ab, einschließlich der Menge des verfügbaren virtuellen Arbeitsspeichers, der Durch aufrufenden Prozesse zugewiesenen Arbeitsspeichermenge und der Fragmentierung im Prozesshap. In Windows XP und neueren Versionen von Windows müssen EMF-Dateien mindestens 2 GB groß sein. Wenn **WritePrinter** zum Schreiben von Nicht-EMF-Daten verwendet wird, z. B. druckerbereite PDL, wird die Größe der Datei nur durch den verfügbaren Speicherplatz beschränkt.

## <a name="examples"></a>Beispiele

Ein Beispielprogramm, das diese Funktion verwendet, finden Sie unter How To: Print Using the GDI Print API (How [To: Drucken mithilfe der GDI-Druck-API).](how-to--print-using-the-gdi-print-api.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

