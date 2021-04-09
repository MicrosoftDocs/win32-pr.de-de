---
description: Die enumprinter-Funktion Listet verfügbare Drucker, Druckserver, Domänen oder Druckanbieter auf.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Enumprinter-Funktion (winspool. h)
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
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864971"
---
# <a name="enumprinters-function"></a>Enumprinter-Funktion

Die **enumprinter** -Funktion Listet verfügbare Drucker, Druckserver, Domänen oder Druckanbieter auf.

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

*Flags* \[in\]
</dt> <dd>

Die Typen von Druck Objekten, die von der Funktion aufgelistet werden sollen. Dieser Wert kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**Drucker-Aufzählung \_ \_ lokal**</dt> </dl>                       | Wenn das \_ \_ druckerenumerationsnamensflag nicht ebenfalls übergeben wird, ignoriert die Funktion den *Name* -Parameter und listet die lokal installierten Drucker auf. Wenn \_ \_ der druckerenumerationsname ebenfalls überschritten wird, listet die Funktion die lokalen Drucker unter *Name* auf. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**\_Name der druckerenum \_**</dt> </dl>                          | Die-Funktion Listet den durch den *Namen* identifizierten Drucker auf. Dabei kann es sich um einen Server, eine Domäne oder einen Druckanbieter handeln. Wenn *Name* den Wert **null** hat, listet die Funktion verfügbare Druckanbieter auf.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**Drucker-Aufzählung frei \_ \_ gegeben**</dt> </dl>                    | Die-Funktion Listet Drucker auf, die über das Shared-Attribut verfügen. Kann nicht isoliert verwendet werden; Verwenden Sie eine OR-Operation, um einen anderen druckeraufgabentyp zu verwenden \_ .<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**Drucker-Aufzählungs \_ \_ Verbindungen**</dt> </dl>     | Mit der-Funktion wird die Liste der Drucker aufgelistet, auf die der Benutzer vorherige Verbindungen hergestellt hat.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**Drucker-Aufzählungs \_ \_ Netzwerk**</dt> </dl>                 | Die-Funktion Listet Netzwerkdrucker in der Domäne des Computers auf. Dieser Wert ist nur gültig, wenn *Level* 1 ist.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**druckeraufzählungs \_ \_ Remote**</dt> </dl>                    | Die-Funktion Listet Netzwerkdrucker und Drucker Server in der Domäne des Computers auf. Dieser Wert ist nur gültig, wenn *Level* 1 ist.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**\_Druckerenum \_ \_ -Kategorie 3D**</dt> </dl>    | Die-Funktion Listet nur 3D-Drucker auf.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**\_druckerenum- \_ Kategorie \_ alle**</dt> </dl> | Die-Funktion Listet alle Druckgeräte auf, einschließlich 3D-Druckern.<br/>                                                                                                                                                                           |



 

Wenn *Level den Wert* 4 hat, können Sie nur die Drucker-enumerationsverbindungen \_ und die lokalen Drucker Enumerationskonstanten verwenden \_ \_ \_ .

> [!Note]  
> 3D-Druckgeräte werden standardmäßig nicht aufgelistet. Sie müssen die beiden **\_ druckerenum \_ \_ -Kategorie 3D** und die Drucker Enumeration **\_ \_ local** einschließen, um nur 3D-Drucker aufzuzählen. Wenn Sie 3D-Drucker zusammen mit allen anderen lokalen Druckern einschließen möchten, verwenden Sie die **\_ druckerenum- \_ Kategorie \_ all** und **Printer \_ Enum \_ local**.

 

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

Wenn *die Ebene* 1 ist *, Flags* \_ \_ den druckerenumerationsnamen und der *Name* ungleich **null** sind, ist *Name* ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des aufzuzählenden Objekts angibt. Diese Zeichenfolge kann der Name eines Servers, einer Domäne oder eines Druck Anbieters sein.

Wenn *Level* 1 ist, enthält *Flags* \_ den druckerenumerationsnamen \_ , und der *Name* ist **null**. die Funktion Listet die verfügbaren Druckanbieter auf.

Wenn die *Ebene* 1 ist, enthält *Flags* die Drucker \_ \_ -enumerationsremote, und der *Name* ist **null**. anschließend listet die Funktion die Drucker in der Domäne des Benutzers auf.

Wenn *Level* 2 oder 5 ist, ist *Name* ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen eines Servers angibt, dessen Drucker aufgelistet werden sollen. Wenn diese Zeichenfolge **null** ist, listet die Funktion die auf dem lokalen Computer installierten Drucker auf.

Wenn die *Ebene* 4 ist, muss der *Name* **null** sein. Die Funktion fragt immer auf dem lokalen Computer ab.

Wenn *Name* den Wert **null** hat, werden die  \_ \_ \| \_ \_ auf dem lokalen Computer installierten Drucker durch Festlegen von Flags für die Drucker Enumeration lokale Drucker enumerationsverbindungen aufgelistet. Zu diesen Druckern gehören diejenigen, die physisch mit dem lokalen Computer verbunden sind, sowie Remote Drucker, an die Sie über eine Netzwerkverbindung verfügen.

Wenn *Name* nicht **null** ist, werden  \_ \_ \| \_ \_ die lokalen Drucker, die auf dem Server *Namen* installiert sind, durch Festlegen von Flags auf den Drucker enumerationsenum-Namen des lokalen Druckers aufgelistet.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Datenstrukturen, auf die von *pprinterenum* verwiesen wird. Gültige Werte sind 1, 2, 4 und 5. diese entsprechen den Datenstrukturen " [**Printer Info \_ \_ 1**](printer-info-1.md)", "Printer Info [**\_ \_ 2**](printer-info-2.md) ", "Printer Info [**\_ \_ 4**](printer-info-4.md)" und " [**Printer \_ Info \_ 5**](printer-info-5.md) ".

Dieser Wert kann 1, 2, 4 oder 5 sein.

</dd> <dt>

*pprinteraufumum* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**Druckern \_ Info \_ 1**](printer-info-1.md), [**Printer \_ Info \_ 2**](printer-info-2.md), [**Printer \_ Info \_ 4**](printer-info-4.md)oder [**Printer \_ Info \_ 5**](printer-info-5.md) -Strukturen empfängt. Jede Struktur enthält Daten, die ein verfügbares Druckobjekt beschreiben.

Wenn *Level* 1 ist, enthält das Array [**Drucker \_ Informationen \_ 1**](printer-info-1.md) -Strukturen. Wenn *Level* 2 ist, enthält das Array [**Drucker \_ Informationen \_ 2**](printer-info-2.md) -Strukturen. Wenn *Level* 4 ist, enthält das Array [**Drucker \_ Info \_ 4**](printer-info-4.md) -Strukturen. Wenn *Level* 5 ist, enthält das Array [**Drucker \_ Informationen \_ 5**](printer-info-5.md) -Strukturen.

Der Puffer muss groß genug sein, um das Array von Datenstrukturen und Zeichen folgen oder andere Daten zu empfangen, auf die die Strukturmember zeigen. Wenn der Puffer zu klein ist, gibt der Parameter *pcbrequired* die erforderliche Puffergröße zurück.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pprinterenum* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der [**Drucker \_ Info \_ 1**](printer-info-1.md), [**Printer \_ Info \_ 2**](printer-info-2.md) , [**Printer \_ Info \_ 4**](printer-info-4.md)oder [**Printer \_ Info \_ 5**](printer-info-5.md) -Strukturen empfängt, die die Funktion in dem Array zurückgibt, auf das *pprinterenum* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Wenn **enumprinter** eine [**Drucker \_ Info \_ 1**](printer-info-1.md) -Struktur zurückgibt, in der der druckerenumerationscontainer \_ \_ angegeben ist, weist dies darauf hin, dass eine Hierarchie von Drucker Objekten vorhanden ist. Eine Anwendung kann die Hierarchie durch Aufrufen von **enumdruckern** auflisten, wobei *Name* auf den Wert des **PName** -Members der **Drucker \_ Info \_ 1** -Struktur festgelegt wird.

Die **enumprinter** -Funktion ruft keine Sicherheitsinformationen ab. Wenn [**Drucker \_ Informationen \_ 2**](printer-info-2.md) -Strukturen im Array zurückgegeben werden, auf das von *pprinterenum* verwiesen wird, werden die *psecuritydescriptor* -Member auf **null** festgelegt.

Um Informationen zum Standarddrucker abzurufen, nennen Sie [**GetDefaultPrinter**](getdefaultprinter.md).

Die [**Drucker \_ Info \_ 4**](printer-info-4.md) -Struktur bietet eine einfache und äußerst schnelle Möglichkeit, die Namen der Drucker, die auf einem lokalen Computer installiert sind, sowie die von einem Benutzer eingerichteten Remote Verbindungen abzurufen. Wenn **enumprinter** mit einer Datenstruktur vom Typ " **Printer \_ Info \_ 4** " aufgerufen wird, fragt diese Funktion die Registrierung nach den angegebenen Informationen ab und wird dann sofort zurückgegeben. Dies unterscheidet sich vom Verhalten von **enumdruckern** , wenn es mit anderen Ebenen von **Printer \_ Info \_ \* *_-Datenstrukturen aufgerufen wird. Insbesondere, wenn _* enumprinter** mit einer Datenstruktur der Ebene 2 ([**Printer \_ Info \_ 2**](printer-info-2.md)) aufgerufen wird, führt Sie einen [**OpenPrinter**](openprinter.md) -Aufruf für jede Remote Verbindung aus. Wenn eine Remote Verbindung nicht mehr vorhanden ist oder der Remote Server nicht mehr vorhanden ist oder der Remote Drucker nicht mehr vorhanden ist, muss die Funktion auf das Timeout von RPC warten und somit den **OpenPrinter** -Aufruf nicht mehr ausführen. Dies kann eine Weile dauern. Durch die Übergabe einer **Drucker \_ Info \_ 4** -Struktur kann eine Anwendung ein Minimum an erforderlichen Informationen abrufen. wenn ausführlichere Informationen gewünscht werden, kann ein nachfolgende **aufrufergrad** 2 aufgerufen werden.

**Windows Vista:** Die von **enumdruckern** zurückgegebenen Druckerdaten werden aus einem lokalen Cache abgerufen, wenn der Wert der *Ebene* 4 ist.

In der folgenden Tabelle wird die **enumprinter** -Ausgabe für verschiedene *Flags* -Werte angezeigt, wenn der *Level* -Parameter auf 1 festgelegt ist.

In der Spalte *namens* Parameter der Tabelle sollten Sie einen entsprechenden Namen für Druckanbieter, Domäne und Computer ersetzen. Beispielsweise können Sie für "Druckanbieter" den Namen des Netzwerkdruck Anbieters oder den Namen des lokalen Druck Anbieters verwenden. Rufen Sie zum Abrufen der Namen von Druckanbietern **enumprinter** auf, deren *Name* auf **null** festgelegt ist.



| *Flags* -Parameter                                  | *Name* -Parameter                            | Ergebnis                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| Drucker Aufzählung \_ \_ lokal (und nicht Drucker Aufzählungs \_ \_ Name) | Der *Name* -Parameter wird ignoriert.<br/> | Alle lokalen Drucker.<br/>                                                                    |
| \_Name der druckerenum \_                                | "Druckanbieter"<br/>                 | Alle Domänen Namen<br/>                                                                       |
| \_Name der druckerenum \_                                | "Druckanbieter! -<br/>          | Alle Drucker und Druckserver in der Domäne des Computers<br/>                                |
| \_Name der druckerenum \_                                | "Druckanbieter!! \\ \\ Computer<br/>    | Alle auf dem Computer freigegebenen Drucker \\ \\<br/>                                                     |
| \_Name der druckerenum \_                                | Eine leere Zeichenfolge: ""<br/>              | Alle lokalen Drucker.<br/>                                                                    |
| \_Name der druckerenum \_                                | **NULL**<br/>                         | Alle Druckanbieter in der Domäne des Computers<br/>                                           |
| Drucker-Aufzählungs \_ \_ Verbindungen                         | Der *Name* -Parameter wird ignoriert.<br/> | Alle verbundenen Remote Drucker<br/>                                                          |
| Drucker-Aufzählungs \_ \_ Netzwerk                             | Der *Name* -Parameter wird ignoriert.<br/> | Alle Drucker in der Domäne des Computers<br/>                                                  |
| druckeraufzählungs \_ \_ Remote                              | Eine leere Zeichenfolge: ""<br/>              | Alle Drucker und Druckserver in der Domäne des Computers<br/>                                |
| druckeraufzählungs \_ \_ Remote                              | "Druckanbieter"<br/>                 | Identisch mit dem \_ druckerenum- \_ Namen<br/>                                                            |
| druckeraufzählungs \_ \_ Remote                              | "Druckanbieter! -<br/>          | Alle Drucker und Druckserver in der Domäne des Computers, unabhängig von der angegebenen *Domäne* .<br/> |
| \_Druckerenum \_ \_ -Kategorie 3D                        | Der *Name* -Parameter wird ignoriert.<br/> | Nur 3D-Drucker werden aufgezählt.<br/>                                                       |
| \_druckerenum- \_ Kategorie \_ alle                       | Der *Name* -Parameter wird ignoriert.<br/> | 3D-Drucker werden zusammen mit allen anderen Druckern aufgelistet.<br/>                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumprintersw** (Unicode) und **enumprintersa** (ANSI)<br/>                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Deleteprinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 1**](printer-info-1.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

