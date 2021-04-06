---
description: Bei den mithilfe von "msiprocessmessage" gesendeten Nachrichten handelt es sich um dieselben Nachrichten, die von der installui- \_ handlerrückruf-Funktion empfangen werden, wenn msisettexternalui
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960825"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage"

Bei den mithilfe von " [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) " gesendeten Nachrichten handelt es sich um dieselben Nachrichten, die von der [**installui- \_ handlerrückruf**](/windows/desktop/api/Msi/nc-msi-installui_handlera) -Funktion empfangen werden, wenn [**msisettexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) Andernfalls verarbeitet Windows Installer die Nachrichten. Weitere Informationen finden Sie unter [Windows Installer-Nachrichten](parsing-windows-installer-messages.md).

Um z. b. eine installmessage \_ -Fehlermeldung mit dem \_ Symbol "MB iconwarning" und den Schaltflächen "MB \_ abortretrycancel" zu senden:


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Dabei *ist hinstall* das Handle für die Installation, das für eine benutzerdefinierte Aktion oder das *hproduct* -Handle von [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) oder [**msiopenpackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)bereitgestellt wird, und *hrec* ist der Datensatz, der die zu formatierenden Fehlerinformationen enthält. Weitere Informationen zur Formatierung finden Sie unter [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).

Wenn ein installmessage- \_ Fehler oder eine installmessage-Nachricht " \_ fatalexit" gesendet wird, ohne den Schalt Flächentyp oder die Symboltypen anzugeben, werden standardmäßig MB \_ OK, kein Symbol und MB \_ DEFBUTTON1 verwendet.

Windows Installer die Schaltfläche **Abbrechen** nicht mit der Zeichenfolge "Abort" beschriftet, wenn eine MessageBox mit der Schaltflächen Spezifikation "MB \_ AbortRetryIgnore" angezeigt wird, wird die Schaltfläche mit der Zeichenfolge "Cancel" beschriftet. Bei allen Fehlermeldungen wird das Wort "Abort" nicht verwendet, sondern stattdessen das Wort "Cancel" verwendet.

Der *hrecord* -Parameter der [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion hängt von dem Nachrichtentyp ab, der an die [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)gesendet wurde. In der folgenden Liste sind die Anforderungen des Datensatzes in Bezug auf den Nachrichtentyp aufgeführt:

installmessage \_ fatalexit

 

installmessage- \_ Info

 

installmessage \_ oudeatdiskspace



| Feld         | BESCHREIBUNG                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Vorlage für die Formatierung der resultierenden Zeichenfolge. Weitere Informationen finden Sie unter [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) . Auf die Felder des Datensatzes wird mithilfe \[ \] von 1 für Feld 1, \[ 2 \] für Feld 2 usw. verwiesen. |
| 1 bis *n* | Alle nachfolgenden Felder sind direkt mit den Feldern verknüpft, auf die die Vorlage in Feld 0 verweist.                                                                                                                    |



 

Wenn Field 0 den Wert NULL aufweist, wird die vom UI-Handler empfangene Zeichenfolge wie folgt formatiert: 1: \[ Daten aus Feld 1 \] 2: \[ Daten aus Feld 2 \] . Dies bedeutet, dass die Zeichenfolge die Feldnummer und die im Feld gespeicherten Daten enthält.

Informationsmeldungen von [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) werden protokolliert, wenn [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga), die [Befehlszeilenoption](command-line-options.md)"/l" oder die [Protokollierungs Richtlinie](logging.md) die Informationen "I" oder "installlogmode" angeben \_ .

installmessage- \_ Fehler

 

installmessage- \_ Warnung

 

installmessage- \_ Benutzer

, Wenn eine Meldung aus der Fehler Tabelle verwendet werden soll.



| Feld         | BESCHREIBUNG                                           |
|---------------|-------------------------------------------------------|
| 0             | Muss NULL sein.                                         |
| 1             | Die Nachrichtennummer in der [Fehler Tabelle](error-table.md). |
| 2 bis *n* | Bezieht sich auf die angegebene Meldung in der Fehler Tabelle.  |



 

Beispiel:



| Feld | Typ   | Daten       |
|-------|--------|------------|
| 0     | Zeichenfolge | NULL       |
| 1     | INT    | 1304       |
| 2     | Zeichenfolge | Myfile.txt |



 

Die resultierende Nachricht, die vom Benutzeroberflächen Handler empfangen wurde, lautet:

Fehler 1304. Fehler beim Schreiben in die Datei: Myfile.txt. Vergewissern Sie sich, dass Sie Zugriff auf dieses Verzeichnis haben.

Wenn Field 0 nicht NULL ist, wird die Meldung aus der Fehler Tabelle überschrieben. Stattdessen bestimmt die Vorlage Field 0 das Format der Nachricht.

In der Meldung können auch die Schaltflächen, einschließlich der Standard Schaltfläche, und das Symbol für die Verwendung mit der Meldung wie oben beschrieben angegeben werden. Die Schaltflächen-und Symboltypen werden im [**installlui- \_ Handler**](/windows/desktop/api/Msi/nc-msi-installui_handlera)aufgeführt.

installmessage \_ commondata

Diese Meldung wird gesendet, um die Schaltfläche **Abbrechen** in einem Status Dialogfeld zu aktivieren oder zu deaktivieren.



| Feld | BESCHREIBUNG                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nicht verwendet.                                                                                                                                      |
| 1     | 2 verweist auf die Schaltfläche " **Abbrechen** ".                                                                                                           |
| 2     | Der Wert 1 gibt an, dass die Schaltfläche **Abbrechen** sichtbar sein soll. Der Wert 0 gibt an, dass die Schaltfläche **Abbrechen** unsichtbar sein sollte.<br/> |



 

Zum Deaktivieren oder Ausblenden der Schaltfläche **Abbrechen** würde der Datensatz z. b. wie folgt aussehen.



| Feld | Typ   | Daten |
|-------|--------|------|
| 0     | Zeichenfolge | NULL |
| 1     | INT    | 2    |
| 2     | INT    | 0    |



 

installmessage- \_ Aktions Start

 

installmessage- \_ Aktions Daten

Der installmessage- \_ Aktions Daten Satz bestimmt das Format des Aktions Datensatzes.



| Feld | BESCHREIBUNG                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | NULL                                                                                                          |
| 1     | Der Aktionsname. Der Name in diesem Feld darf nicht NULL sein.                                                         |
| 2     | Aktions Beschreibung.                                                                                           |
| 3     | Aktions Vorlage. Diese wird für die Aktions Daten verwendet, deren Nachricht entsprechend dieser Vorlage formatiert wird. |



 

Verweisen Sie in der Aktions Vorlagen Nachricht nicht auf Feld 0.

Der "installmessage"- \_ Aktions Daten Satz ist wie folgt formatiert.



| Feld         | BESCHREIBUNG                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | NULL                                                                                                                                               |
| 1 bis *n* | Abhängig von Feld 3 der entsprechenden installmessage- \_ Aktions Meldung oder-Vorlage, die in der [Tabelle "aktiontext](actiontext-table.md)" angegeben ist. |



 

Beispielsweise der "installmessage"- \_ Aktions Daten Satz.



| Feld | Typ   | Daten                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | Zeichenfolge | NULL                                                            |
| 1     | Zeichenfolge | Myaction                                                        |
| 2     | Zeichenfolge | Dies ist die Beschreibung von "myaction".                           |
| 3     | Zeichenfolge | Vorlage myaction: field1 Data ist \[ 1 \] . die Daten des Felds 2 sind \[ 2 \] . |



 

Die Vorlage für installmessage- \_ Aktions Start (Field 3) verweist auf die Felder 1 und 2. der installmessage- \_ Aktions Daten Satz sollte 2 Felder mit den berechtigten Daten aufweisen. Die Felder können entweder Zeichen folgen-oder ganzzahlige Felder sein.

Installmessage- \_ Aktions Daten Satz.



| Feld | Typ   | Daten                    |
|-------|--------|-------------------------|
| 0     | Zeichenfolge | NULL                    |
| 1     | INT    | 2                       |
| 2     | Zeichenfolge | Action Data für myaction |



 

installmessage \_ FilesInUse

Der FilesInUse-Datensatz ist ein Datensatz variabler Länge.



| Feld | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Dieses Feld kann NULL sein. Für eine Installation mit einer einfachen Benutzeroberfläche kann in diesem Feld statischer Text für die Anzeige im [ListBox-Steuer](listbox-control.md) Element des [Dialog Felds FilesInUse](filesinuse-dialog.md)angegeben werden. Für eine Installation mit einer vollständigen Benutzeroberfläche hat dieses Feld keine Auswirkung, da der Text durch die Erstellung des benutzerdefinierten FilesInUse-Dialog Felds angegeben wird. |
| 1     | Der Name der verwendeten Datei.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Dieses Feld identifiziert den Prozess, der die verwendete Datei enthält. **Windows Installer Version 4,0:** Die Prozess-ID (PID) des Prozesses oder der Titel des Fensters für den Prozess.<br/> **Windows Installer Version 3,1 und früher:** Dieses Feld muss die Prozess-ID (PID) des Prozesses sein.<br/>                                                      |



 

Um z. b. eine FilesInUse-Nachricht mit zwei verwendeten Dateien zu senden, red.exe und blue.exe, verfügt der Datensatz über vier Felder und das Feld 0. Das Format des Datensatzes wäre wie in der folgenden Tabelle dargestellt. Für dieses Beispiel ist Windows Installer Version 4,0 erforderlich.

**Windows Installer Version 3,1 und früher:** Die Felder 2 und 4 im folgenden Beispiel müssen die PIDs der Prozesse enthalten, in denen red.exe und blue.exe verwendet werden.



| Feld | BESCHREIBUNG       |
|-------|-------------------|
| 0     | NULL              |
| 1     | Red.exe           |
| 2     | Titel des roten Fensters  |
| 3     | Blue.exe          |
| 4     | Titel des blauen Fensters |



 

> [!Note]  
> Wenn die von dem Dienst übergebenen PID in Windows Installer Version 4,0 keinen Fenstertitel aufweist, wie z. b. eine Task leisten Anwendung, wird die Datei nicht angezeigt, und das ausführliche Protokoll enthält die folgenden Meldungen.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

installmessage \_ ResolveSource

Der installmessage \_ ResolveSource-Datensatz enthält sieben Felder. Damit installmessage \_ ResolveSource ordnungsgemäß funktioniert, wird die installmessage ResolveSource-Nachricht möglicherweise nicht von einem externen Benutzeroberflächen Handler verarbeitet \_ . Windows Installer müssen die installmessage \_ ResolveSource-Nachricht verarbeiten. Das heißt, der externe UI-Handler gibt 0 zurück, um anzugeben, dass keine Aktion ausgeführt wird, wenn die installmessage \_ ResolveSource-Nachricht gefiltert wird. Es wird empfohlen, keine ResolveSource-Nachricht zu senden.



| Feld | BESCHREIBUNG                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | NULL                                                                                                                                                               |
| 1     | NULL                                                                                                                                                               |
| 2     | Name des Pakets.                                                                                                                                                      |
| 3     | Produktcode.                                                                                                                                                      |
| 4     | Relativer Pfad, sofern bekannt, kann NULL sein.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Gibt an, ob der Paketcode überprüft werden soll. Der Wert "1" gibt an, dass der Paketcode überprüft werden soll. Der Wert ' 0 ' gibt an, dass das Paket nicht überprüft werden sollte. |
| 7     | Erforderlicher Datenträger aus der Medien Tabelle. Der Wert ' 0 ' gibt an, dass ein beliebiger Datenträger zulässig ist.                                                                              |



 

 

 




