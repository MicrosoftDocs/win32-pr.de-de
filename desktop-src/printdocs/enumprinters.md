---
description: Die EnumPrinters-Funktion listet verfügbare Drucker, Druckerserver, Domänen oder Druckanbieter auf.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: EnumPrinters-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fb88cef081010f1319fb194904933ba2366d6593f0d2517c696bb6d6490ace20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353840"
---
# <a name="enumprinters-function"></a>EnumPrinters-Funktion

Die **EnumPrinters-Funktion** listet verfügbare Drucker, Druckerserver, Domänen oder Druckanbieter auf.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Die Typen von Druckobjekten, die die Funktion aufzählen soll. Dieser Wert kann einer oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**PRINTER \_ ENUM \_ LOCAL**</dt> </dl>                       | Wenn das FLAG PRINTER \_ ENUM \_ NAME nicht ebenfalls übergeben wird, ignoriert die Funktion den *Name-Parameter* und listet die lokal installierten Drucker auf. Wenn \_ PRINTER ENUM \_ NAME ebenfalls übergeben wird, listet die Funktion die lokalen Drucker unter *Name* auf. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**NAME \_ DER DRUCKERENUMER \_**</dt> </dl>                          | Die Funktion listet den Drucker auf, der durch *Name* identifiziert wird. Dies kann ein Server, eine Domäne oder ein Druckanbieter sein. Wenn *Name* **NULL** ist, listet die Funktion verfügbare Druckanbieter auf.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**\_DRUCKERENUMER FREIGEGEBEN \_**</dt> </dl>                    | Die Funktion listet Drucker auf, die über das freigegebene Attribut verfügen. Kann nicht isoliert verwendet werden. verwenden Sie einen OR-Vorgang, um mit einem anderen \_ PRINTER-ENUM-Typ zu kombinieren.<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**\_ \_ DRUCKERENUMERVERBINDUNGEN**</dt> </dl>     | Die Funktion listet die Liste der Drucker auf, mit denen der Benutzer vorherige Verbindungen hergestellt hat.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**\_DRUCKERENUMERNETZWERK \_**</dt> </dl>                 | Die Funktion listet Netzwerkdrucker in der Domäne des Computers auf. Dieser Wert ist nur gültig, wenn *Level* gleich 1 ist.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**PRINTER \_ ENUM \_ REMOTE**</dt> </dl>                    | Die Funktion listet Netzwerkdrucker und Druckerserver in der Domäne des Computers auf. Dieser Wert ist nur gültig, wenn *Level* gleich 1 ist.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**\_DRUCKERENUMERKATEGORIE \_ \_ 3D**</dt> </dl>    | Die Funktion listet nur 3D-Drucker auf.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**PRINTER \_ ENUM \_ CATEGORY \_ ALL**</dt> </dl> | Die Funktion listet alle Druckgeräte auf, einschließlich 3D-Drucker.<br/>                                                                                                                                                                           |



 

Wenn *Level* gleich 4 ist, können Sie nur die Konstanten PRINTER \_ ENUM \_ CONNECTIONS und PRINTER \_ ENUM \_ LOCAL verwenden.

> [!Note]  
> 3D-Druckgeräte werden standardmäßig nicht aufzählt. Sie müssen sowohl **PRINTER \_ ENUM \_ CATEGORY \_ 3D** als auch **PRINTER \_ ENUM \_ LOCAL** einschließen, um nur 3D-Drucker aufzuzählen. Um 3D-Drucker zusammen mit allen anderen lokalen Druckern einzubeziehen, verwenden Sie **PRINTER \_ ENUM \_ CATEGORY \_ ALL** und **PRINTER \_ ENUM \_ LOCAL**.

 

</dd> <dt>

*Name* \[ In\]
</dt> <dd>

Wenn *Level* gleich 1 ist, *Flags* PRINTER \_ ENUM \_ NAME und *Name* ungleich **NULL** ist, dann ist *Name* ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des aufzuzählenden Objekts angibt. Diese Zeichenfolge kann der Name eines Servers, einer Domäne oder eines Druckanbieters sein.

Wenn *Level* 1 ist, *enthält Flags* PRINTER \_ ENUM \_ NAME und *Name* **NULL,** dann listet die Funktion die verfügbaren Druckanbieter auf.

Wenn *Level* gleich 1 ist, *Flags* PRINTER \_ ENUM \_ REMOTE und *Name* **NULL** ist, listet die Funktion die Drucker in der Domäne des Benutzers auf.

Wenn *Level* gleich 2 oder 5 ist, ist *Name* ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen eines Servers angibt, dessen Drucker aufzählt werden sollen. Wenn diese Zeichenfolge **NULL** ist, listet die Funktion die auf dem lokalen Computer installierten Drucker auf.

Wenn *Level* gleich 4 ist, sollte *Name* **NULL** sein. Die Funktion fragt immer auf dem lokalen Computer ab.

Wenn *Name* **NULL** ist, listet das Festlegen von *Flags* auf PRINTER \_ ENUM \_ LOCAL PRINTER \| \_ ENUM \_ CONNECTIONS die Drucker auf, die auf dem lokalen Computer installiert sind. Zu diesen Druckern gehören solche, die physisch an den lokalen Computer angefügt sind, sowie Remotedrucker, mit denen er über eine Netzwerkverbindung verfügt.

Wenn *Name* nicht **NULL** ist, listet das Festlegen von *Flags* auf PRINTER \_ ENUM \_ LOCAL PRINTER \| \_ ENUM \_ NAME die lokalen Drucker auf, die auf dem Server installiert sind *Name*.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Der Typ der Datenstrukturen, auf die *pPrinterEnum* zeigt. Gültige Werte sind 1, 2, 4 und 5, die den Datenstrukturen [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)und [**PRINTER INFO \_ \_ 5**](printer-info-5.md) entsprechen.

Dieser Wert kann 1, 2, 4 oder 5 sein.

</dd> <dt>

*pPrinterEnum* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**PRINTER \_ INFO \_ 1-,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2-,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4-**](printer-info-4.md)oder [**PRINTER INFO \_ \_ 5-Strukturen**](printer-info-5.md) empfängt. Jede Struktur enthält Daten, die ein verfügbares Druckobjekt beschreiben.

Wenn *Level* gleich 1 ist, enthält das Array [**PRINTER INFO \_ \_ 1-Strukturen.**](printer-info-1.md) Wenn *Level* gleich 2 ist, enthält das Array [**PRINTER INFO \_ \_ 2-Strukturen.**](printer-info-2.md) Wenn *Level* gleich 4 ist, enthält das Array [**PRINTER INFO \_ \_ 4-Strukturen.**](printer-info-4.md) Wenn *Level* gleich 5 ist, enthält das Array [**PRINTER INFO \_ \_ 5-Strukturen.**](printer-info-5.md)

Der Puffer muss groß genug sein, um das Array von Datenstrukturen und alle Zeichenfolgen oder anderen Daten zu empfangen, auf die die Strukturmember zeigen. Wenn der Puffer zu klein ist, gibt der *Parameter "pwNeeded"* die erforderliche Puffergröße zurück.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pPrinterEnum* zeigt.

</dd> <dt>

*"Needed"* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbBuf* zu klein ist.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der [**PRINTER \_ INFO \_ 1-,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2-,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4-**](printer-info-4.md)oder [**PRINTER INFO \_ \_ 5-Strukturen**](printer-info-5.md) empfängt, die die Funktion im Array zurückgibt, auf das *pPrinterEnum* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)auf.

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Wenn **EnumPrinters** eine [**PRINTER INFO \_ \_ 1-Struktur**](printer-info-1.md) zurückgibt, in der PRINTER \_ ENUM \_ CONTAINER angegeben ist, gibt dies an, dass eine Hierarchie von Druckerobjekten vorhanden ist. Eine Anwendung kann die Hierarchie aufzählen, indem **sie EnumPrinters** erneut aufruft und *Name* auf den Wert des **pName-Elements** der **PRINTER INFO \_ \_ 1-Struktur** festlegt.

Die **EnumPrinters-Funktion** ruft keine Sicherheitsinformationen ab. Wenn [**PRINTER \_ INFO \_ 2-Strukturen**](printer-info-2.md) im Array zurückgegeben werden, auf das *pPrinterEnum* zeigt, werden ihre *pSecurityDescriptor-Member* auf **NULL** festgelegt.

Rufen [**Sie GetDefaultPrinter**](getdefaultprinter.md)auf, um Informationen zum Standarddrucker abzurufen.

Die [**PRINTER \_ INFO \_ 4-Struktur**](printer-info-4.md) bietet eine einfache und äußerst schnelle Möglichkeit, die Namen der drucker, die auf einem lokalen Computer installiert sind, sowie die Remoteverbindungen abzurufen, die ein Benutzer hergestellt hat. Wenn **EnumPrinters** mit einer **PRINTER INFO \_ \_ 4-Datenstruktur** aufgerufen wird, fragt diese Funktion die Registrierung nach den angegebenen Informationen ab und gibt dann sofort zurück. Dies unterscheidet sich vom Verhalten von **EnumPrinters,** wenn es mit anderen Ebenen von **PRINTER INFO \_ \_ \* *_-Datenstrukturen aufgerufen wird. Insbesondere wenn _* EnumPrinters** mit einer Datenstruktur der Ebene 2 ([**PRINTER INFO \_ \_ 2**](printer-info-2.md)) aufgerufen wird, wird für jede Remoteverbindung ein [**OpenPrinter-Aufruf**](openprinter.md) ausgeführt. Wenn eine Remoteverbindung getrennt ist oder der Remoteserver nicht mehr vorhanden ist oder der Remotedrucker nicht mehr vorhanden ist, muss die Funktion warten, bis für RPC ein Time out aufgetreten ist, und der **OpenPrinter-Aufruf** schlägt daher fehl. Dies kann eine Weile dauern. Wenn eine **PRINTER \_ INFO \_ 4-Struktur** übergeben wird, kann eine Anwendung nur minimal erforderliche Informationen abrufen. Wenn ausführlichere Informationen gewünscht werden, kann ein **nachfolgender EnumPrinters-Aufruf** der Ebene 2 erfolgen.

**Windows Vista:** Die von **EnumPrinters zurückgegebenen** Druckerdaten werden aus einem lokalen Cache abgerufen, wenn der Wert von *Level* gleich 4 ist.

Die folgende Tabelle zeigt die **EnumPrinters-Ausgabe** für verschiedene *Flags-Werte,* wenn der *Level-Parameter* auf 1 festgelegt ist.

In der Parameterspalte *Name* der Tabelle sollten Sie einen entsprechenden Namen für Druckanbieter, Domäne und Computer ersetzen. Beispielsweise können Sie für "Druckanbieter" den Namen des Netzwerkdruckanbieters oder den Namen des lokalen Druckanbieters verwenden. Um Druckanbieternamen abzurufen, rufen Sie **EnumPrinters** auf, wobei *Name* auf **NULL** festgelegt ist.



| *Flags-Parameter*                                  | *Name-Parameter*                            | Ergebnis                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| PRINTER \_ ENUM \_ LOCAL (and not PRINTER \_ ENUM \_ NAME) | Der *Name-Parameter* wird ignoriert.<br/> | Alle lokalen Drucker.<br/>                                                                    |
| NAME \_ DER DRUCKERENUMER \_                                | "Druckanbieter"<br/>                 | Alle Domänennamen<br/>                                                                       |
| NAME \_ DER DRUCKERENUMER \_                                | "Druckanbieter! Domäne"<br/>          | Alle Drucker und Druckserver in der Domäne des Computers<br/>                                |
| NAME \_ DER DRUCKERENUMER \_                                | "Druckanbieter!" \\ \\ Computer"<br/>    | Alle Drucker, die auf \\ dem Computer freigegeben sind \\<br/>                                                     |
| NAME \_ DER DRUCKERENUMER \_                                | Eine leere Zeichenfolge, "".<br/>              | Alle lokalen Drucker.<br/>                                                                    |
| NAME \_ DER DRUCKERENUMER \_                                | **NULL**<br/>                         | Alle Druckanbieter in der Domäne des Computers<br/>                                           |
| \_ \_ DRUCKERENUMERVERBINDUNGEN                         | Der *Name-Parameter* wird ignoriert.<br/> | Alle verbundenen Remotedrucker<br/>                                                          |
| \_DRUCKERENUMERNETZWERK \_                             | Der *Name-Parameter* wird ignoriert.<br/> | Alle Drucker in der Domäne des Computers<br/>                                                  |
| PRINTER \_ ENUM \_ REMOTE                              | Eine leere Zeichenfolge, "".<br/>              | Alle Drucker und Druckserver in der Domäne des Computers<br/>                                |
| PRINTER \_ ENUM \_ REMOTE                              | "Druckanbieter"<br/>                 | Identisch mit PRINTER \_ ENUM \_ NAME<br/>                                                            |
| PRINTER \_ ENUM \_ REMOTE                              | "Druckanbieter! Domäne"<br/>          | Alle Drucker und Druckserver in der Domäne des Computers, unabhängig von der angegebenen *Domäne.*<br/> |
| \_DRUCKERENUMERKATEGORIE \_ \_ 3D                        | Der *Name-Parameter* wird ignoriert.<br/> | Nur 3D-Drucker werden aufzählt.<br/>                                                       |
| PRINTER \_ ENUM \_ CATEGORY \_ ALL                       | Der *Name-Parameter* wird ignoriert.<br/> | 3D-Drucker werden zusammen mit allen anderen Druckern aufzählt.<br/>                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **EnumPrintersW** (Unicode) und **EnumPrintersA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

