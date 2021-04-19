---
description: Beschreibt verschiedene Programmier Überlegungen für Transaktions-NTFS.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Überlegungen zur Programmierung für transaktionale NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79dc7eba4de1258c294d3e41f8042f3cb01dc87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362394"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Überlegungen zur Programmierung für transaktionale NTFS

Eine Beschreibung der verschiedenen Programmier Überlegungen für Transaktions-NTFS finden Sie in den folgenden Abschnitten:

-   [Welche Dateiänderungen werden verarbeitet?](#which-file-changes-are-transacted)
-   [Komprimierung](#compression)
-   [Erstellen einer Datei oder eines Verzeichnisses](#creating-a-file-or-directory)
-   [Löschen einer Datei](#deleting-a-file)
-   [Löschen eines Verzeichnisses](#deleting-a-directory)
-   [Probleme bei der Verzeichnis Sperrung](#directory-locking-issues)
-   [Verzeichnisenumeration](#directory-enumeration)
-   [Im Speicher abgebildete Dateien](#memory-mapped-files)
-   [Benannte Datenströme](#named-streams)
-   [Umbenennen einer Datei oder eines Verzeichnisses](#renaming-a-file-or-directory)
-   [Reparse Points](#reparse-points)
-   [Fehlercodes](#error-codes)
-   [Verschlüsseltes Datei System](#encrypted-file-system)
-   [Datei-e/a-Funktionen und transaktionale NTFS](#file-io-functions-and-transactional-ntfs)
    -   [Transaktive Funktionen](#transacted-functions)
    -   [Von TxF geänderte Datei-e/a-Funktionen](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Welche Dateiänderungen werden verarbeitet?

Die meisten Dateiänderungen, wie z. b. Änderungen an Dateiinhalten, Streams, Analyse Punkten, Attributen und der Dateisystem-Namespace, werden transaktiv behandelt. Wenn eine dieser Änderungen an einem transaktiven Datei Handle vorgenommen wird, wird die Änderung von anderen Transaktionen isoliert, und die Änderung wird rückgängig gemacht, wenn für die Transaktion ein Rollback ausgeführt wird.

Änderungen, die sich nicht auf Dateiinhalte, Metadaten oder den Dateisystem-Namespace auswirken, wie z. b. Änderungen an der Komprimierung oder Defragmentierung, werden nicht transaktiv behandelt. Diese Änderungen sind nicht von anderen Transaktionen isoliert und werden nicht rückgängig gemacht, wenn für die Transaktion ein Rollback ausgeführt wird.

## <a name="compression"></a>Komprimierung

Der Komprimierungs Status einer Datei, die in einer Transaktion geöffnet wurde, kann nicht geändert werden.

## <a name="creating-a-file-or-directory"></a>Erstellen einer Datei oder eines Verzeichnisses

Eine Datei oder ein Verzeichnis, das in einer Transaktion erstellt wird, ist für nichts außerhalb der aktuellen Transaktion sichtbar. Außerhalb dieser Transaktion schlägt der Versuch, eine Datei mit demselben Namen zu erstellen, mit dem Fehler **\_ Transaktions \_ Konflikt** fehl, sodass der Dateiname für die Transaktion, für die ein Commit ausgeführt wird oder für die ein Rollback ausgeführt wird, effektiv reserviert wird.

## <a name="deleting-a-file"></a>Löschen einer Datei

Eine Datei oder ein Verzeichnis, das durch den Aufruf der [**deletefiletransall**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) -Funktion gelöscht wird, bleibt für alle externen Leser sichtbar.

> [!Note]  
> Alle Transaktions Handles für die Datei müssen vor dem Ende der Transaktion geschlossen werden. Wenn die Handles nicht ordnungsgemäß geschlossen werden, erfolgt kein Löschvorgang. Alle geöffneten Handles für die Datei müssen geschlossen werden, bevor der Commit für den Löschvorgang durchgeführt wird, um als Teil der Transaktion angesehen zu werden. Dies liegt daran, dass das System eine Datei erst dann löscht, wenn das letzte Handle geschlossen wurde, auch wenn der Vorgang nicht als Teil des Windows-Datei-e/a-Subsystems behandelt wird.

 

## <a name="deleting-a-directory"></a>Löschen eines Verzeichnisses

Ein Verzeichnis, das durch den Aufruf der [**removedirectorytransall**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) -Funktion gelöscht wird, bleibt für alle externen Leser sichtbar.

> [!Note]  
> Die gleichen Einschränkungen gelten für geöffnete Handles bei transaktiven Verzeichnis Vorgängen wie für Dateien. Weitere Informationen finden Sie unter [Löschen einer Datei](#deleting-a-file).

 

## <a name="directory-locking-issues"></a>Probleme bei der Verzeichnis Sperrung

Wenn eine Datei in einer Transaktion geändert wird, werden alle Verzeichnis Komponenten des Pfads zur Datei bis zum Ende der Transaktion als *fixiert gegen Rename* bezeichnet. Das heißt, das System hindert Sie daran, Sie zu umbenennen, bis für die Transaktion ein Commit oder ein Rollback ausgeführt wird. Der Versuch, ein Verzeichnis umzubenennen, das ein übergeordnetes Element einer Datei ist, die in einer laufenden Transaktion geändert wurde, schlägt mit der Fehlermeldung "Fehler beim **\_ Auflösen der \_ \_ Transaktions \_ Abhängigkeit**" fehl.

## <a name="directory-enumeration"></a>Verzeichnisenumeration

Der Inhalt eines Verzeichnisses kann geändert werden, während eine Enumeration durch die Verwendung von APIs, die aufgelistet werden, z. b. die Funktionen [**findfirstfiletransaktive**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) und [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) , ausgeführt wird.

Änderungen an einem Verzeichnis außerhalb einer Transaktion sind nicht von der Transaktion isoliert und in der Transaktion sofort sichtbar. Wenn ein nicht transaktiver Writer beispielsweise eine Datei zu einem Verzeichnis hinzufügt, wird die neue Datei sofort innerhalb der Transaktion angezeigt, sodass der Aufruf der [**findfirstfiletranscommit**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) -Funktion oder der [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) -Funktion die neue Datei zurückgibt.

Änderungen, die an einem Verzeichnis innerhalb einer Transaktion vorgenommen werden, werden bis zum Commit der Transaktion isoliert. Beispielsweise eine Datei, die im Verzeichnis als Teil der Transaktion erstellt wurde. Ein nicht transaktiver Reader, der die [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) -oder [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) -Funktion aufrufen, wird die neu erstellte Datei erst sehen, wenn für die Transaktion ein Commit ausgeführt wird.

## <a name="memory-mapped-files"></a>Speicherabbilddateien

Der Client muss die [**flushviewoffile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) -Funktion aufrufen, das Datei Zuordnungs Objekt schließen und das Datei Handle schließen, bevor die zugehörige Transaktion in einer Speicher Abbild Datei committet wird.

## <a name="named-streams"></a>Benannte Datenströme

Benannte Streams sind vollständig transaktional, aber das Sperren erfolgt auf Dateiebene, nicht auf der Streamebene. Writer außerhalb einer Transaktion, die versuchen, Datenströme innerhalb einer gesperrten Datei zu ändern, erhalten die Fehler **\_ Freigabe \_ Verletzung**.

Sie können einen sekundären Datenstrom nicht in einer Transaktion umbenennen.

## <a name="renaming-a-file-or-directory"></a>Umbenennen einer Datei oder eines Verzeichnisses

Zum Umbenennen einer Datei in einem transaktiven Vorgang wird [**movefiletranshandelten**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) aufgerufen, um die Datei zu verschieben.

## <a name="reparse-points"></a>Reparse Points

Änderungen an Analyse Punkten werden transaktiv ausgeführt. das bedeutet, dass ein neuer Analyse Punkt, der einer Datei in einer Transaktion zugewiesen wird, nicht für die anderen Transaktionen sichtbar ist. Entsprechend sind Änderungen oder Entfernungs Vorgänge eines vorhandenen Analyse Punkts bis zum Commit nicht sichtbar.

## <a name="error-codes"></a>Fehlercodes

Der Kerneltransaktions-Manager (KTM) verwendet die Systemfehler Codes im Bereich von 6700 bis 6799. Transaktionale NTFS (TxF) verwendet Windows-Fehlercodes im Bereich von 6800 bis 6899. Weitere Informationen finden Sie unter Winerror. h und System Fehler Codes (6000-8199).

## <a name="encrypted-file-system"></a>Verschlüsseltes Datei System

TxF unterstützt keine Vorgänge für EFS-Dateien. Eine EFS-verschlüsselte Datei kann für Transaktionen nicht geöffnet werden. Das Aufrufen der [**createfiletransfailed**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) -Funktion für eine EFS-Datei schlägt mit der Fehler **Meldung \_ EFS \_ nicht \_ zulässig \_ in der \_ Transaktion** fehl. Ebenso schlägt das Aufrufen der [**verschlüsseltfile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) -Funktion für eine Datei in einer Transaktion mit der Fehler **Meldung \_ EFS \_ nicht \_ zulässig \_ in der \_ Transaktion** fehl.

## <a name="file-io-functions-and-transactional-ntfs"></a>Datei-e/a-Funktionen und transaktionale NTFS

TxF bietet neue transaktive Funktionen, die einen Dateinamen annehmen, und ändert das Verhalten vorhandener Datei-e/a-API-Funktionen, die ein Datei Handle annehmen.

### <a name="transacted-functions"></a>Transaktive Funktionen

Wenn Sie anstelle der nicht transaktiven Version eine der folgenden transaktiven Funktionen aufzurufen, wird der Vorgang nicht transaktiv ausgeführt:

-   [**Copyfiletransagiert**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**"Kreatedirectoriytransagiert"**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**"Kreatefiletransagiert"**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**"Kreatehardlinktransagiert"**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**"Kreatesymboliclinktransagiert"**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**Deletefiletransagiert**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**Findfirstdateinametransactedw**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**Findfirstfiletransagiert**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**Findfirststreamtransactedw**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**Getcompressedfilesizetranshandelten**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**Getfileattributestransagiert**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**Getfullpathnametranshandelten**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**Getlongpathnametransagiert**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**"Muvefiletransagiert"**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**Removedirectoriytransagiert**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**Setfileattributestranshandelten**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

Beispielsweise verfügt die Funktion " [**fiatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " nun über eine transaktive Version: " [**kreatefiletransagiert**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)".

### <a name="file-io-functions-changed-by-txf"></a>Von TxF geänderte Datei-e/a-Funktionen

In der folgenden Tabelle sind die Funktionen aufgeführt, deren Verhalten von transaktionalen NTFS betroffen ist. Beispielsweise unterscheidet sich das Verhalten der Funktion "read [**File**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) " abhängig davon, ob der *hFile* -Parameter von der Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " [**oder der Funktion "-Funktion"**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) erstellt wurde.



| Funktion                                                                                                                                                                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Anwendungen sollten alle Handles schließen, die an eine Transaktion gebunden sind, bevor ein Commit für die Transaktion ausgeführt wird. Eine Anwendung muss ein transaktives handle schließen, das mit dem **\_ Dateiflag \_ Delete bei \_ \_ Close** geöffnet wurde, bevor ein Commit für die Transaktion ausgeführt wird, damit der Löschvorgang ausgeführt wird.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Wenn *hFile* eine Transaktion zugeordnet ist, wird das Datei Zuordnungs Objekt, das diese Funktion erstellt, derselben Transaktion zugeordnet. Änderungen, die Übersichten dieses Datei Zuordnungsobjekts vorgenommen wurden, werden transaktiv behandelt. Anwendungen müssen [**flushviewoffile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile)aufrufen, alle Sichten aufheben und alle Handles für das Datei Zuordnungs Objekt schließen, bevor Sie einen Commit für transaktive Änderungen ausführen.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Wenn eine Transaktion an das dateienumerationshandle gebunden ist, unterliegen die zurückgegebenen Dateien Transaktions Isolations Regeln.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**Komprimierung von ssctl- \_ Satz \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | Sie können den Komprimierungs Status einer Datei, die von " [**kreatefiletransfailed**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)" geöffnet wurde, nicht ändern.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**Getfileingeformationbyhandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) und [ **getfileingeformationbylenker Ex**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | Wenn eine Transaktion an das Datei Handle gebunden ist, gibt die Funktion Informationen für die isolierte Dateiansicht zurück.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) und [ **getfilesizeex**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | Wenn eine Transaktion an das Datei Handle gebunden ist, gibt die Funktion Informationen für die isolierte Dateiansicht zurück.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Wenn das Volume Dateisystem Transaktionen unterstützt, gibt die Funktion eine **Datei \_ unterstützt \_ Transaktionen** in *lpfilesystemflags* aus.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) und [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Wenn dem Datei Handle, das zum Erstellen des zugeordneten Datei zuordnenden Objekts verwendet wird, eine Transaktion zugeordnet ist, wird die zugeordnete Ansicht transaktiv dargestellt. Wenn die Ansicht verwendet wird, um transaktive Änderungen an einer Datei vorzunehmen, muss der Benutzer [**flushviewoffile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile)aufrufen, das Datei Zuordnungsobjekt schließen und das Datei Handle schließen, bevor ein Commit für die zugehörige Transaktion ausgeführt wird.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**"Read directoriychangesw"**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | Wenn eine Transaktion an das Verzeichnis Handle gebunden ist, spiegeln die Benachrichtigungen die isolierte Ansicht des Verzeichnisses wider. Änderungen an Dateien außerhalb der transaktiven Ansicht des Verzeichnisses sind nicht in den Benachrichtigungen enthalten.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>" [**Infofile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)", " [**infofileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)" und " [**infofilescatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) "<br/>                                                                                  | Wenn eine Transaktion an das Datei Handle gebunden ist, gibt die Funktion Daten aus der transaktiven Ansicht der Datei zurück. Ein transaktives Lese handle zeigt garantiert die gleiche Ansicht einer Datei für die Dauer des Handles an.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Wenn eine Transaktion an das Handle gebunden ist, wird die Änderung in der dateiendeposition transaktiv.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**Setfileingeformationbyhandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | Wenn eine Transaktion an das Handle gebunden ist, werden die vorgenommenen Änderungen für die Informations Klassen **filebasicinfo**, **filerenameinfo**, **filezucationinfo**, **fileendoffileinfo** und **filedispositioninfo** verarbeitet.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**Setfileshortname**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | Wenn eine Transaktion an das Handle gebunden ist, wird die Änderung im Kurznamen der Datei transaktiv.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | Wenn eine Transaktion an das Handle gebunden ist, wird die Änderung der Datei Zeit verarbeitet.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>" [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)", " [**Write fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)" und " [**Write filegather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) "<br/>                                                                              | Wenn eine Transaktion an das Datei Handle gebunden ist, wird der Datei Schreibvorgang verarbeitet.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

