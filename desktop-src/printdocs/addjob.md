---
description: Die AddJob-Funktion fügt der Liste der Druckaufträge, die vom Druckspooler geplant werden können, einen Druckauftrag hinzu. Die Funktion ruft den Namen der Datei ab, die Sie zum Speichern des Auftrags verwenden können.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: AddJob-Funktion (Winspool.h)
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
ms.openlocfilehash: de99b0866e8cd7ec8486d2a3f15f95194b4350008a43fe4db8ae82d970684c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950750"
---
# <a name="addjob-function"></a>AddJob-Funktion

Die **AddJob-Funktion** fügt der Liste der Druckaufträge, die vom Druckspooler geplant werden können, einen Druckauftrag hinzu. Die Funktion ruft den Namen der Datei ab, die Sie zum Speichern des Auftrags verwenden können.

> [!NOTE]
> In Windows 8 Betriebssystemen und höher wird die direkte Verwendung von **AddJob** nicht empfohlen, da es Fälle gibt (z. B. das Drucken in eine Warteschlange mit file: oder PORTPROMPT:). , **wobei AddJob** fehlschlägt. Stattdessen wird empfohlen, die [GDI-Druck-API,](gdi-printing.md) [die XPS-Druck-API,](xps-printing.md) [**StartDocPrinter**](startdocprinter.md)oder die entsprechende Methode aus dem [**Windows. Graphics.Printing-Namespace,**](/uwp/api/Windows.Graphics.Printing) je nach Druckszenario.
>
> Wenn Sie versuchen, mit **File:** oder **PORTPROMPT:** in eine Warteschlange zu drucken, gibt **AddJob** den Fehler NICHT \_ UNTERSTÜTZT zurück.

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

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle, das den Drucker für den Druckauftrag angibt. Dies muss ein lokaler Drucker sein, der als Spooldrucker konfiguriert ist. Wenn *hPrinter ein* Handle für eine Remotedruckerverbindung ist oder der Drucker für den direkten Druck konfiguriert ist, schlägt die **AddJob-Funktion** fehl. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Version der Datenstruktur der Druckauftragsinformationen, die die Funktion im Puffer speichert, auf den *pData zeigt.* Legen Sie diesen Parameter auf 1 fest.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine [**ADDJOB \_ INFO \_ 1-Datenstruktur**](addjob-info-1.md) und eine Pfadzeichenfolge empfängt.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pData zeigt.* Der Puffer muss groß genug sein, um eine [**ADDJOB \_ INFO \_ 1-Struktur**](addjob-info-1.md) und eine Pfadzeichenfolge zu enthalten.

</dd> <dt>

*-Needed* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtgröße der [**ADDJOB \_ INFO \_ 1-Datenstruktur**](addjob-info-1.md) sowie die Pfadzeichenfolge in Bytes empfängt. Wenn dieser Wert kleiner oder gleich *cbBuf* ist und die Funktion erfolgreich ist, ist dies die tatsächliche Anzahl von Bytes, die in den Puffer geschrieben werden, auf den *pData zeigt.* Wenn diese Zahl größer als *cbBuf* ist, ist der Puffer zu klein, und Sie müssen die Funktion erneut mit einer Puffergröße aufrufen, die mindestens so groß ist \* *wie "besend".*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Sie können die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aufrufen, um die vom **Path-Member** der [**ADDJOB \_ INFO \_ 1-Struktur**](addjob-info-1.md) angegebene Spooldatei zu öffnen, und dann die [**WriteFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-writefile) aufrufen, um Druckauftragsdaten in sie zu schreiben. Rufen Sie anschließend die [**ScheduleJob-Funktion**](schedulejob.md) auf, um den Druckspooler zu benachrichtigen, dass der Druckauftrag jetzt vom Spooler für den Druck geplant werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddJobW** (Unicode) und **AddJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ADDJOB \_ INFO \_ 1**](addjob-info-1.md)
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

[**Windows. Graphics.Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> </dl>

 

