---
description: Die DocumentProperties-Funktion ruft Druckerin initialisierungsinformationen ab oder ändert sie oder zeigt ein Eigenschaftenblatt für die Druckerkonfiguration für den angegebenen Drucker an.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: DocumentProperties-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 349a085cc8f55f391b33dd5048d23a35fdac3c2b33b3771290bcecd9fdbcfc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235107"
---
# <a name="documentproperties-function"></a>DocumentProperties-Funktion

Die **DocumentProperties-Funktion** ruft Druckerin initialisierungsinformationen ab oder ändert sie oder zeigt ein Eigenschaftenblatt für die Druckerkonfiguration für den angegebenen Drucker an.

## <a name="syntax"></a>Syntax


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hWnd* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Eigenschaftenblatts für die Druckerkonfiguration.

</dd> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für ein Druckerobjekt. Verwenden Sie [**die OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pDeviceName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL terminierte Zeichenfolge, die den Namen des Geräts angibt, für das das Eigenschaftenblatt für die Druckerkonfiguration angezeigt wird.

</dd> <dt>

*pDevModeOutput* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die die vom Benutzer angegebenen Druckerkonfigurationsdaten empfängt.

</dd> <dt>

*pDevModeInput* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die das Betriebssystem zum Initialisieren der Eigenschaftenblattsteuerelemente verwendet.

Dieser Parameter wird nur verwendet, wenn das **DM \_ IN \_ BUFFER-Flag** im *fMode-Parameter festgelegt* ist. Wenn **DM \_ IN \_ BUFFER** nicht festgelegt ist, verwendet das Betriebssystem den standardmäßigen DEVMODE des [**Druckers.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)

</dd> <dt>

*fMode* \[ In\]
</dt> <dd>

Die Vorgänge, die die Funktion ausführt. Wenn dieser Parameter 0 (null) ist, gibt die **DocumentProperties-Funktion** die Anzahl von Bytes zurück, die für die [**DEVMODE-Datenstruktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) des Druckertreibers erforderlich sind. Verwenden Sie andernfalls eine oder mehrere der folgenden Konstanten, um einen Wert für diesen Parameter zu erstellen. Beachten Sie jedoch, dass eine Anwendung mindestens einen Eingabe- und einen Ausgabewert angeben muss, um die Druckeinstellungen zu ändern.



| Wert                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**DM \_ IM \_ PUFFER**</dt> </dl>    | Eingabewert. Vor dem Auffordern, Kopieren oder Aktualisieren führt die Funktion die aktuellen Druckeinstellungen des Druckertreibers mit den Einstellungen in der [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) zusammen, die durch den *pDevModeInput-Parameter angegeben* wird. Die -Funktion aktualisiert die -Struktur nur für die Member, die vom **dmFields-Member der DEVMODE-Struktur angegeben** werden.  Dieser Wert wird auch als **DM \_ MODIFY definiert.** Bei Konflikten während der Zusammenführung überschreiben die Einstellungen in der **devmode-Struktur,** die von *pDevModeInput* angegeben werden, die aktuellen Druckeinstellungen des Druckertreibers.<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**DM \_ IN \_ PROMPT**</dt> </dl>    | Eingabewert. Die -Funktion stellt das Eigenschaftenblatt für das Druckersetup des Druckertreibers vor und ändert dann die Einstellungen in der [**DEVMODE-Datenstruktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) des Druckers in die vom Benutzer angegebenen Werte. Dieser Wert wird auch als **DM \_ PROMPT definiert.**<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**DM \_ OUT \_ BUFFER**</dt> </dl> | Ausgabewert. Die Funktion schreibt die aktuellen Druckeinstellungen des Druckertreibers, einschließlich privater Daten, in die [**DEVMODE-Datenstruktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die durch den *pDevModeOutput-Parameter angegeben* wird. Der Aufrufer muss einen Puffer zuordnen, der groß genug ist, um die Informationen zu enthalten. Wenn die **DM \_ OUT \_ BUFFER-Bitsätze** eindeutig sind, kann der *pDevModeOutput-Parameter* **NULL sein.** Dieser Wert wird auch als **DM \_ COPY definiert.**<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der *fMode-Parameter* 0 (null) ist, ist der Rückgabewert die Größe des Puffers, der zum Enthalten der Initialisierungsdaten des Druckertreibers erforderlich ist. Beachten Sie, dass dieser Puffer größer als eine [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) sein kann, wenn der Druckertreiber private Daten an die Struktur anfügen.

Wenn die Funktion das Eigenschaftenblatt anzeigt, ist der Rückgabewert entweder **IDOK** oder **IDCANCEL,** je nachdem, welche Schaltfläche der Benutzer auswählt.

Wenn die Funktion das Eigenschaftenblatt nicht zeigt und erfolgreich ist, ist der Rückgabewert **IDOK.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert kleiner als 0 (null).

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu kommen, dass die Anwendung nicht reagiert.

 

Die Zeichenfolge, auf die der *pDeviceName-Parameter* zeigt, kann durch Aufrufen der [**GetPrinter-Funktion ermittelt**](getprinter.md) werden.

Die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die tatsächlich von einem Druckertreiber verwendet wird, enthält den geräteunabhängigen Teil (wie oben definiert), gefolgt von einem treiberspezifischen Teil, der je nach Treiber und Treiberversion in Größe und Inhalt variiert. Aufgrund dieser Treiberabhängigkeit ist es sehr wichtig, dass Anwendungen den Treiber nach der richtigen Größe der **DEVMODE-Struktur** abfragen, bevor sie einen Puffer dafür zuweisen.

**Um Änderungen an den für eine Anwendung lokal vorgenommenen Druckeinstellungen vorzunehmen, sollte eine Anwendung die folgenden Schritte ausführen:**

1.  Rufen Sie die Anzahl der Bytes ab, die für die vollständige [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) erforderlich sind, indem **Sie DocumentProperties aufrufen** und 0 (null) im *fMode-Parameter* angeben.
2.  Ordnen Sie Arbeitsspeicher für die vollständige [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) zu.
3.  Rufen Sie die aktuellen Druckereinstellungen ab, indem **Sie DocumentProperties aufrufen.** Übergeben Sie einen Zeiger auf die [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die in Schritt 2 als *pDevModeOutput-Parameter* zugeordnet wurde, und geben Sie den **DM OUT \_ \_ BUFFER-Wert** an.
4.  Ändern Sie die entsprechenden Member der zurückgegebenen [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) und geben Sie an, welche Member geändert wurden, indem Sie die entsprechenden Bits im **dmFields-Member** von **DEVMODE festlegen.**
5.  Rufen **Sie DocumentProperties** auf, und übergeben Sie die geänderte [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) als *pDevModeInput-* und *pDevModeOutput-Parameter* zurück, und geben Sie sowohl **die DM IN \_ \_ BUFFER-** als auch **die DM OUT \_ \_ BUFFER-Werte** an (die mit dem OR-Operator kombiniert werden). Die **DEVMODE-Struktur,** die durch den dritten Aufruf von **DocumentProperties** zurückgegeben wird, kann als Argument in einem Aufruf der [**CreateDC-Funktion verwendet**](/windows/desktop/api/wingdi/nf-wingdi-createdca) werden.

Um ein Handle für einen Druckergerätekontext mithilfe der aktuellen Druckereinstellungen zu erstellen, müssen Sie **DocumentProperties** wie oben beschrieben nur zweimal aufrufen. Der erste Aufruf ruft die Größe des vollständigen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ab, und der zweite Aufruf initialisiert **devMODE** mit den aktuellen Druckereinstellungen. Übergeben Sie den initialisierten **DEVMODE** an [**CreateDC,**](/windows/desktop/api/wingdi/nf-wingdi-createdca) um das Handle für den Druckergerätekontext zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **DocumentPropertiesW** (Unicode) und **DocumentPropertiesA** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AdvancedDocumentProperties**](advanceddocumentproperties.md)
</dt> <dt>

[**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

