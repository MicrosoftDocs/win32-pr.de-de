---
description: Die AddJob-Funktion fügt der Liste der Druckaufträge, die vom Druck Spooler geplant werden können, einen Druckauftrag hinzu. Die-Funktion Ruft den Namen der Datei ab, die Sie verwenden können, um den Auftrag zu speichern.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: AddJob-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756409"
---
# <a name="addjob-function"></a>AddJob-Funktion

Die **AddJob** -Funktion fügt der Liste der Druckaufträge, die vom Druck Spooler geplant werden können, einen Druckauftrag hinzu. Die-Funktion Ruft den Namen der Datei ab, die Sie verwenden können, um den Auftrag zu speichern.

> [!NOTE]
> In Windows 8 und höheren Betriebssystemen wird die Verwendung von **AddJob** nicht direkt empfohlen, da es Fälle gibt (z. b. das Drucken in eine Warteschlange mithilfe von file: oder portprompt:) bei **AddJob** tritt ein Fehler auf. Stattdessen empfiehlt es sich, abhängig vom Druck Szenario [GDI-Druck-API](gdi-printing.md), [XPS-Druck-API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)oder die entsprechende Methode aus dem [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) -Namespace zu verwenden.
>
> Wenn Sie versuchen, in einer Warteschlange mithilfe von **file:** oder **portprompt:** zu drucken, gibt **AddJob** den nicht \_ unterstützten Fehler zurück.

## <a name="syntax"></a>Syntax

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle, das den Drucker für den Druckauftrag angibt. Dabei muss es sich um einen lokalen Drucker handeln, der als Druck Drucker konfiguriert ist. Wenn *hprinter* ein Handle für eine Remote Druckerverbindung ist oder wenn der Drucker für den direkten Druck konfiguriert ist, tritt bei der **AddJob** -Funktion ein Fehler auf. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Version der Datenstruktur der Druckauftrags Informationen, die die Funktion im Puffer speichert, auf die von *pData* verwiesen wird. Legen Sie diesen Parameter auf einen Wert fest.

</dd> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine Datenstruktur vom Typ [**AddJob \_ Info \_ 1**](addjob-info-1.md) und eine Pfad Zeichenfolge empfängt.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pData* zeigt. Der Puffer muss groß genug sein, um eine [**AddJob \_ Info \_ 1**](addjob-info-1.md) -Struktur und eine Pfad Zeichenfolge zu enthalten.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtgröße der Datenstruktur von [**AddJob \_ Info \_ 1**](addjob-info-1.md) in Bytes und die Pfad Zeichenfolge empfängt. Wenn dieser Wert kleiner oder gleich *cbbuf* ist und die Funktion erfolgreich ist, ist dies die tatsächliche Anzahl von Bytes, die in den Puffer geschrieben werden, auf den *pData* zeigt. Wenn diese Zahl größer als *cbbuf* ist, ist der Puffer zu klein, und Sie müssen die Funktion mit einer Puffergröße, die mindestens so groß wie \* *pcbbenöist*, erneut aufzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Sie können die Funktion "-Funktion" aufrufen, um die Spooldatei zu öffnen, die vom **path** -Member der [**AddJob \_ Info \_ 1**](addjob-info-1.md) -Struktur angegeben wird, und dann [**die Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " aufrufen, um Druckauftrags Daten in die Datei zu schreiben. Nachdem dies geschehen ist, wird die [**schedulejob**](schedulejob.md) -Funktion aufgerufen, um den Druck Spooler zu benachrichtigen, dass der Druckauftrag jetzt vom Spooler für den Druck geplant werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Addjobw** (Unicode) und **addjoba** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AddJob- \_ Info \_ 1**](addjob-info-1.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[GDI-Druck-API](gdi-printing.md)
</dt> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> </dl>

 

