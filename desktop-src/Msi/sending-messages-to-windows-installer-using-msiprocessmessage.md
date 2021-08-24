---
description: Die mit MsiProcessMessage gesendeten Nachrichten sind die gleichen Nachrichten, die von der INSTALLUI HANDLER-Rückruffunktion empfangen werden, wenn \_ MsiSetExternalUI aufgerufen wurde.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Senden von Nachrichten an Windows Installer mit msiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1c639e45b22c2406f446ab31072ceb02ab9b3e906f5973b1436356d96f3782
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629950"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>Senden von Nachrichten an Windows Installer mit msiProcessMessage

Die mit [**MsiProcessMessage gesendeten**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) Nachrichten sind die gleichen Nachrichten, die von der [**INSTALLUI \_ HANDLER-Rückruffunktion**](/windows/desktop/api/Msi/nc-msi-installui_handlera) empfangen werden, wenn [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) aufgerufen wurde. Andernfalls Windows Installer die Nachrichten verarbeitet. Weitere Informationen finden Sie unter [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).

So senden Sie beispielsweise eine INSTALLMESSAGE ERROR-Nachricht mit dem MB ICONWARNING-Symbol und den \_ \_ MB \_ ABORTRETRYCANCEL-Schaltflächen:


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Dabei *ist hInstall* das Handle für die Installation, das für eine benutzerdefinierte Aktion oder das *hProduct-Handle* von [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) oder [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)bereitgestellt wird, und *hRec* ist der Datensatz, der die zu formatierenden Fehlerinformationen enthält. Informationen zur Formatierung finden Sie unter [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).

Standardmäßig werden MB OK, kein Symbol und \_ \_ MB \_ DEFBUTTON1 verwendet, wenn eine INSTALLMESSAGE ERROR- oder INSTALLMESSAGE FATALEXIT-Nachricht ohne Angabe von Schaltflächentyp oder Symboltypen \_ gesendet wird.

Windows Das Installationsprogramm bezeichnet die **AbORT-Schaltfläche** nicht mit der Zeichenfolge "Abort", wenn ein MessageBox-Paket mit der MB ABORTRETRYIGNORE-Schaltflächenspezifikation angezeigt wird, sondern die Schaltfläche mit der \_ Zeichenfolge "Abbrechen". Bei allen Fehlermeldungen wird das Wort "Abbrechen" und stattdessen das Wort "Abbrechen" nicht verwendet.

Der *hRecord-Parameter* der [**MsiProcessMessage-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) hängt vom Nachrichtentyp ab, der an [**msiProcessMessage gesendet wird.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) In der folgenden Liste sind die Anforderungen des Datensatzes in Bezug auf den Nachrichtentyp aufgeführt:

INSTALLMESSAGE \_ FATALEXIT

 

INSTALLMESSAGE \_ INFO

 

INSTALLMESSAGE \_ OUTOFDISKSPACE



| Feld         | Beschreibung                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Vorlage für die Formatierung der resultierenden Zeichenfolge. Weitere Informationen finden Sie unter [**MsiFormatRecord.**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) Auf die Felder des Datensatzes wird \[ mithilfe von 1 \] für Feld 1, \[ 2 für Feld \] 2 usw. verwiesen. |
| 1 bis *n* | Alle nachfolgenden Felder sind direkt mit den Feldern verknüpft, auf die die Vorlage in Feld 0 verweist.                                                                                                                    |



 

Wenn Feld 0 NULL ist, wird die vom UI-Handler empfangene Zeichenfolge wie folgt formatiert: 1: Daten aus Feld 1 2: Daten aus Feld 2. Dies bedeutet, dass die Zeichenfolge für jedes Feld des Datensatzes die Feldnummer gefolgt von den im Feld gespeicherten Daten \[ \] \[ \] enthält.

Informationsmeldungen von [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) werden protokolliert, wenn [](logging.md) [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), die Befehlszeilenoption "/l" oder die Protokollierungsrichtlinie "I" oder INSTALLLOGMODE INFO [](command-line-options.md) \_ angeben.

\_INSTALLMESSAGE-FEHLER

 

INSTALLMESSAGE \_ WARNING

 

INSTALLMESSAGE \_ USER

So verwenden Sie eine Meldung aus der Tabelle Error.



| Feld         | Beschreibung                                           |
|---------------|-------------------------------------------------------|
| 0             | Muss NULL sein.                                         |
| 1             | Meldungsnummer in der [Fehlertabelle](error-table.md). |
| 2 bis *n* | Im Zusammenhang mit der angegebenen Meldung in der Tabelle Error.  |



 

Beispiel:



| Feld | Typ   | Daten       |
|-------|--------|------------|
| 0     | Zeichenfolge | NULL       |
| 1     | INT    | 1304       |
| 2     | Zeichenfolge | Myfile.txt |



 

Die resultierende Meldung, die vom Benutzeroberflächenhandler empfangen wird, ist:

Fehler 1304. Fehler beim Schreiben in eine Datei: Myfile.txt. Vergewissern Sie sich, dass Sie Zugriff auf dieses Verzeichnis haben.

Wenn Feld 0 nicht NULL ist, wird die Meldung aus der Fehlertabelle überschrieben. Stattdessen bestimmt die Vorlage feld 0 das Format der Nachricht.

Die Meldung kann auch die Schaltflächen angeben, einschließlich der Standardschaltfläche und des Symbols für die Verwendung mit der Oben erwähnten Nachricht. Die Schaltflächen- und Symboltypen sind unter [**INSTALLUI \_ HANDLER aufgeführt.**](/windows/desktop/api/Msi/nc-msi-installui_handlera)

INSTALLMESSAGE \_ COMMONDATA

Diese Meldung wird gesendet, um die Schaltfläche **Abbrechen** in einem Statusdialogfeld zu aktivieren oder zu deaktivieren.



| Feld | Beschreibung                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nicht verwendet.                                                                                                                                      |
| 1     | 2 bezieht sich auf die **Schaltfläche Abbrechen.**                                                                                                           |
| 2     | Der Wert 1 gibt an, dass **die Schaltfläche** Abbrechen sichtbar sein soll. Der Wert 0 gibt an, dass **die Schaltfläche Abbrechen** unsichtbar sein sollte.<br/> |



 

Um beispielsweise die Schaltfläche Abbrechen zu deaktivieren **oder** auszublenden, wird der Datensatz wie folgt angezeigt.



| Feld | Typ   | Daten |
|-------|--------|------|
| 0     | Zeichenfolge | NULL |
| 1     | INT    | 2    |
| 2     | INT    | 0    |



 

INSTALLMESSAGE \_ ACTIONSTART

 

INSTALLMESSAGE \_ ACTIONDATA

Der INSTALLMESSAGE \_ ACTIONSTART-Datensatz bestimmt das Format des ActionData-Datensatzes.



| Feld | Beschreibung                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | NULL                                                                                                          |
| 1     | Aktionsname. Der Name in diesem Feld muss nicht NULL sein.                                                         |
| 2     | Beschreibung der Aktion.                                                                                           |
| 3     | Aktionsvorlage. Dies wird für die ActionData-Klasse verwendet, deren Nachricht gemäß dieser Vorlage formatiert wird. |



 

Verweisen Sie in der Meldung Aktionsvorlage nicht auf Feld 0.

Der \_ INSTALLMESSAGE ACTIONDATA-Datensatz ist wie folgt formatiert.



| Feld         | Beschreibung                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | NULL                                                                                                                                               |
| 1 bis *n* | Abhängig von Feld 3 der entsprechenden INSTALLMESSAGE \_ ACTIONSTART-Nachricht oder -Vorlage, die in der [ActionText-Tabelle](actiontext-table.md)angegeben ist. |



 

Beispielsweise der \_ INSTALLMESSAGE ACTIONSTART-Eintrag.



| Feld | Typ   | Daten                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | Zeichenfolge | NULL                                                            |
| 1     | Zeichenfolge | MyAction                                                        |
| 2     | Zeichenfolge | Dies ist die Beschreibung von "MyAction".                           |
| 3     | Zeichenfolge | MyAction-Vorlage: Field1-Daten sind \[ 1 \] . Feld 2-Daten sind \[ 2 \] . |



 

Die Vorlage für INSTALLMESSAGE \_ ACTIONSTART (Feld 3) verweist auf die Felder 1 und 2. Der \_ INSTALLMESSAGE ACTIONDATA-Datensatz sollte 2 Felder mit den garantierten Daten enthalten. Die Felder können zeichenfolgen- oder ganzzahlige Felder sein.

INSTALLMESSAGE \_ ACTIONDATA-Datensatz.



| Feld | Typ   | Daten                    |
|-------|--------|-------------------------|
| 0     | Zeichenfolge | NULL                    |
| 1     | INT    | 2                       |
| 2     | Zeichenfolge | ActionData für MyAction |



 

INSTALLMESSAGE \_ FILESINUSE

Der FILESINUSE-Eintrag ist ein Datensatz variabler Länge.



| Feld | Beschreibung                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Dieses Feld kann NULL sein. Bei einer Installation mit einer einfachen Benutzeroberfläche kann dieses Feld statischen Text für die Anzeige im [ListBox-Steuerelement](listbox-control.md) des [Dialogfelds FilesInUse](filesinuse-dialog.md)angeben. Bei einer Installation mit einer vollständigen Benutzeroberfläche hat dieses Feld keine Auswirkungen, da der Text durch die Erstellung des benutzerdefinierten Dialogfelds FilesInUse angegeben wird. |
| 1     | Name der verwendeten Datei.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Dieses Feld identifiziert den Prozess, in dem die Datei verwendet wird. **Windows Installer Version 4.0:** Die Prozess-ID (PID) des Prozesses oder der Titel des Fensters für den Prozess.<br/> **Windows Installer Version 3.1 und früher:** Dieses Feld muss die Prozess-ID (PID) des Prozesses sein.<br/>                                                      |



 

Um z. B. eine FilesInUse-Nachricht mit zwei verwendeten Dateien zu senden, red.exe und blue.exe, weist der Datensatz vier Felder plus dem Feld 0 auf. Das Format des Datensatzes wäre wie in der folgenden Tabelle dargestellt. Für dieses Beispiel ist Windows Installer Version 4.0 erforderlich.

**Windows Installer Version 3.1 und früher:** Die Felder 2 und 4 im folgenden Beispiel müssen die PIDs der Prozesse enthalten, die red.exe und blue.exe enthalten.



| Feld | Beschreibung       |
|-------|-------------------|
| 0     | NULL              |
| 1     | Red.exe           |
| 2     | Titel des roten Fensters  |
| 3     | Blue.exe          |
| 4     | Titel des blauen Fensters |



 

> [!Note]  
> Wenn die vom Dienst übergebene PID auf Windows Installer-Version 4.0 keinen Fenstertitel aufweist, z. B. eine Taskleistenanwendung, wird die Datei nicht angezeigt, und das ausführliche Protokoll enthält die folgenden Meldungen.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

INSTALLMESSAGE \_ RESOLVESOURCE

Der \_ INSTALLMESSAGE RESOLVESOURCE-Eintrag verfügt über sieben Felder. Damit INSTALLMESSAGE \_ RESOLVESOURCE ordnungsgemäß funktioniert, verarbeitet ein externer UI-Handler die INSTALLMESSAGE \_ RESOLVESOURCE-Nachricht möglicherweise nicht. Windows Das Installationsprogramm muss die INSTALLMESSAGE \_ RESOLVESOURCE-Nachricht verarbeiten. Das heißt, der externe UI-Handler gibt 0 zurück, um anzugeben, dass beim Filtern der INSTALLMESSAGE RESOLVESOURCE-Nachricht keine Aktion ausgeführt \_ wird. Die bewährte Methode besteht darin, das Senden einer RESOLVESOURCE-Nachricht zu vermeiden.



| Feld | Beschreibung                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | NULL                                                                                                                                                               |
| 1     | NULL                                                                                                                                                               |
| 2     | Name des Pakets.                                                                                                                                                      |
| 3     | Produktcode.                                                                                                                                                      |
| 4     | Der relative Pfad, sofern bekannt, kann NULL sein.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Gibt an, ob der Paketcode überprüft werden soll. Der Wert "1" gibt an, dass der Paketcode überprüft werden soll. Der Wert "0" gibt an, dass das Paket nicht überprüft werden soll. |
| 7     | Erforderlicher Datenträger aus der Medientabelle. Der Wert "0" gibt an, dass jeder Datenträger akzeptabel ist.                                                                              |



 

 

 




