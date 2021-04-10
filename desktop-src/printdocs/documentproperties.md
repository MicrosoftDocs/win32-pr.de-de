---
description: Die DocumentProperties-Funktion ruft Drucker Initialisierungs Informationen ab oder ändert Sie oder zeigt ein Eigenschaften Blatt der Druckerkonfiguration für den angegebenen Drucker an.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: DocumentProperties-Funktion (winspool. h)
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
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131909"
---
# <a name="documentproperties-function"></a>DocumentProperties-Funktion

Die **DocumentProperties** -Funktion ruft Drucker Initialisierungs Informationen ab oder ändert Sie oder zeigt ein Eigenschaften Blatt der Druckerkonfiguration für den angegebenen Drucker an.

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

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Druckerkonfigurations-Eigenschaften Blatts.

</dd> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für ein Drucker Objekt. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pdevicename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Geräts angibt, für das das Eigenschaften Blatt "Druckerkonfiguration" angezeigt wird.

</dd> <dt>

*pdevmodeoutput* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die vom Benutzer angegebenen Drucker Konfigurationsdaten empfängt.

</dd> <dt>

*pdevmodeinput* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die das Betriebssystem verwendet, um die Eigenschaften Blatt-Steuerelemente zu initialisieren.

Dieser Parameter wird nur verwendet, wenn das **DM \_ in- \_ pufferflag** im Parameter " *f Mode* " festgelegt ist. Wenn **DM \_ im \_ Puffer** nicht festgelegt ist, verwendet das Betriebssystem den standardmäßigen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)des Druckers.

</dd> <dt>

*f-Modus* \[ in\]
</dt> <dd>

Die Vorgänge, die die Funktion ausführt. Wenn dieser Parameter NULL ist, gibt die **DocumentProperties** -Funktion die Anzahl der Bytes zurück, die für die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Datenstruktur des Druckertreibers erforderlich ist. Verwenden Sie andernfalls mindestens eine der folgenden Konstanten, um einen Wert für diesen Parameter zu erstellen. Beachten Sie jedoch, dass eine Anwendung mindestens einen Eingabe Wert und einen Ausgabewert angeben muss, um die Druckeinstellungen zu ändern.



| Wert                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**DM \_ in \_ Puffer**</dt> </dl>    | Der Eingabe Wert. Vor dem aufrufen, kopieren oder aktualisieren führt die Funktion die aktuellen Druckeinstellungen des Druckertreibers mit den Einstellungen in der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur zusammen, die durch den *pdevmodeinput* -Parameter angegeben wird. Die-Funktion aktualisiert die-Struktur nur für die Elemente, die vom **dmFields** -Member der **DEVMODE** -Struktur angegeben werden. Dieser Wert wird auch als **DM- \_ Änderung** definiert. Bei einem Konflikt während der Zusammenführung überschreiben die Einstellungen in der **DEVMODE** -Struktur, die von *pdevmodeinput* angegeben werden, die aktuellen Druckeinstellungen des Druckertreibers.<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**DM \_ - \_ Eingabeaufforderung**</dt> </dl>    | Der Eingabe Wert. Die Funktion zeigt das Druck Setup-Eigenschaften Blatt des Druckertreibers an und ändert anschließend die Einstellungen in der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Datenstruktur des Druckers auf die vom Benutzer angegebenen Werte. Dieser Wert wird auch als **DM- \_ Eingabeaufforderung** definiert.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**DM- \_ out- \_ Puffer**</dt> </dl> | Ausgabewert. Die-Funktion schreibt die aktuellen Druckeinstellungen des Druckertreibers, einschließlich privater Daten, in die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Datenstruktur, die durch den *pdevmodeoutput* -Parameter angegeben wird. Der Aufrufer muss einen ausreichend großen Puffer zuordnen, um die Informationen zu enthalten. Wenn die Bit- **DM- \_ out- \_ Puffer** Sätze eindeutig sind, kann der *pdevmodeoutput* -Parameter **null** sein. Dieser Wert wird auch als **DM- \_ Kopie** definiert.<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der *fmode* -Parameter 0 (null) ist, ist der Rückgabewert die Größe des Puffers, der zum enthalten der Initialisierungs Daten für den Druckertreiber erforderlich ist. Beachten Sie, dass dieser Puffer größer als eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur sein kann, wenn der Druckertreiber private Daten an die Struktur anfügt.

Wenn die Funktion das Eigenschaften Blatt anzeigt, ist der Rückgabewert entweder **IDOK** oder **IDCANCEL**, abhängig von der Schaltfläche, die der Benutzer auswählt.

Wenn die Funktion das Eigenschaften Blatt nicht anzeigt und erfolgreich ist, lautet der Rückgabewert **IDOK**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert kleiner als 0 (null).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Die Zeichenfolge, auf die der *pdevicename* -Parameter verweist, kann durch Aufrufen der [**GetPrinter**](getprinter.md) -Funktion abgerufen werden.

Die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die tatsächlich von einem Druckertreiber verwendet wird, enthält den geräteunabhängigen Teil (wie oben definiert), gefolgt von einem treiberspezifischen Teil, der in Größe und Inhalt mit den einzelnen Treiber-und Treiberversionen variiert. Aufgrund dieser Treiber Abhängigkeit ist es sehr wichtig, dass Anwendungen den Treiber nach der richtigen Größe der **DEVMODE** -Struktur Abfragen, bevor Sie einen Puffer dafür zuordnen.

**Um Änderungen an den Druckeinstellungen vorzunehmen, die für eine Anwendung lokal sind, sollte eine Anwendung die folgenden Schritte ausführen:**

1.  Rufen Sie die Anzahl der Bytes ab, die für die vollständige [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur erforderlich sind, indem Sie **DocumentProperties** aufrufen und NULL im *fmode* -Parameter angeben.
2.  Zuweisen von Speicher für die vollständige [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur.
3.  Rufen Sie die aktuellen Druckereinstellungen durch Aufrufen von **DocumentProperties** ab. Übergeben Sie einen Zeiger an die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die in Schritt 2 als *pdevmodeoutput* -Parameter zugewiesen wurde, und geben Sie den Wert für **DM \_ out- \_ Puffer** an
4.  Ändern Sie die entsprechenden Member der zurückgegebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, und geben Sie an, welche Elemente geändert wurden, indem Sie die entsprechenden Bits im **dmFields** -Member von **DEVMODE** festgelegt haben.
5.  Verwenden Sie **DocumentProperties** , und übergeben Sie die geänderte [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur zurück als *pdevmodeinput* -Parameter und *pdevmodeoutput* -Parameter, und geben Sie sowohl den **DM \_ in \_ buffer** -als auch den **DM \_ out- \_ Puffer** Wert an (die mithilfe des OR-Operators kombiniert werden). Die **DEVMODE** -Struktur, die vom dritten **DocumentProperties** -Befehl zurückgegeben wird, kann als Argument in einem aufrufen [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createdca) -Funktion" verwendet werden.

Um mithilfe der aktuellen Druckereinstellungen ein Handle für einen Druckergerätekontext zu erstellen, müssen Sie die **DocumentProperties** -Eigenschaft wie oben beschrieben zweimal abrufen. Der erste-Befehl ruft die Größe des vollständigen [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ab, und der zweite aufrufsinitialisiert den **DEVMODE** mit den aktuellen Druckereinstellungen. Übergeben Sie den initialisierten **DEVMODE** -Typ an " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ", um das Handle für den Drucker Gerätekontext zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Documentpropertiesw** (Unicode) und **documentpropertiesa** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Advanceddocumentproperties**](advanceddocumentproperties.md)
</dt> <dt>

[**-**](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

