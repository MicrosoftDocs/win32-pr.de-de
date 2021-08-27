---
description: Beschreibt verschiedene Programmierüberlegungen für transaktionales NTFS.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Programmierüberlegungen für transaktionales NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3150746b1cb34495178cc8318805587f3d08f17e04cb8227e95a9c52ddce3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047940"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Programmierüberlegungen für transaktionales NTFS

Eine Beschreibung der verschiedenen Programmierüberlegungen für transaktionales NTFS finden Sie in den folgenden Abschnitten:

-   [Welche Dateiänderungen werden durchgeführt?](#which-file-changes-are-transacted)
-   [Komprimierung](#compression)
-   [Erstellen einer Datei oder eines Verzeichnisses](#creating-a-file-or-directory)
-   [Löschen einer Datei](#deleting-a-file)
-   [Löschen eines Verzeichnisses](#deleting-a-directory)
-   [Probleme beim Sperren von Verzeichnissen](#directory-locking-issues)
-   [Verzeichnisenumeration](#directory-enumeration)
-   [Speicherzuordnungsdateien](#memory-mapped-files)
-   [Benannte Datenströme](#named-streams)
-   [Umbenennen einer Datei oder eines Verzeichnisses](#renaming-a-file-or-directory)
-   [Reparse Points](#reparse-points)
-   [Fehlercodes](#error-codes)
-   [Verschlüsseltes Dateisystem](#encrypted-file-system)
-   [Datei-E/A-Funktionen und transaktionales NTFS](#file-io-functions-and-transactional-ntfs)
    -   [Transaktive Funktionen](#transacted-functions)
    -   [Von TxF geänderte Datei-E/A-Funktionen](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Welche Dateiänderungen werden durchgeführt?

Die meisten Dateiänderungen, z. B. Änderungen an Dateiinhalten, Datenströmen, Wiederholungspunkten, Attributen und dem Dateisystemnamespace, werden durchgeführt. Wenn eine dieser Änderungen an einem Transaktionsdateihandle vorgenommen wird, wird die Änderung von anderen Transaktionen isoliert, und die Änderung wird rückgängig gemacht, wenn für die Transaktion ein Rollback ausgeführt wird.

Änderungen, die sich nicht auf Dateiinhalte, Metadaten oder den Dateisystemnamespace auswirken, z. B. Änderungen an der Komprimierung oder Defragmentierung, werden nicht transaktiv. Diese Änderungen sind nicht von anderen Transaktionen isoliert, und sie werden nicht rückgängig gemacht, wenn für die Transaktion ein Rollback ausgeführt wird.

## <a name="compression"></a>Komprimierung

Der Komprimierungsstatus einer in einer Transaktion geöffneten Datei kann nicht geändert werden.

## <a name="creating-a-file-or-directory"></a>Erstellen einer Datei oder eines Verzeichnisses

Eine Datei oder ein Verzeichnis, die bzw. das in einer Transaktion erstellt wird, ist außerhalb der aktuellen Transaktion nicht sichtbar. Außerhalb dieser Transaktion schlägt jeder Versuch, eine Datei mit dem gleichen Namen zu erstellen, mit dem Fehler **ERROR \_ TRANSACTIONAL \_ CONFLICT** fehl. Dadurch wird der Dateiname für reserviert, wenn für die Transaktion ein Commit ausgeführt wird oder ein Rollback ausgeführt wird.

## <a name="deleting-a-file"></a>Löschen einer Datei

Eine Datei oder ein Verzeichnis, die bzw. das durch Aufrufen der [**DeleteFileTransacted-Funktion**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) gelöscht wird, bleibt für alle externen Reader sichtbar.

> [!Note]  
> Alle transaktiven Handles für die Datei müssen vor dem Ende der Transaktion geschlossen werden. Wenn die Handles nicht ordnungsgemäß geschlossen sind, erfolgt der Löschfehler nicht. Alle geöffneten Handles für die Datei müssen geschlossen werden, bevor der Commit ausgeführt wird, damit der Löschvorgang als Teil der Transaktion betrachtet wird. Dies liegt daran, dass das System eine Datei erst dann löscht, wenn das letzte Handle geschlossen wird, selbst wenn der Vorgang nicht als Teil des Windows Datei-E/A-Subsystems ausgeführt wird.

 

## <a name="deleting-a-directory"></a>Löschen eines Verzeichnisses

Ein Verzeichnis, das durch Aufrufen der [**RemoveDirectoryTransacted-Funktion**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) gelöscht wird, bleibt für alle externen Reader sichtbar.

> [!Note]  
> Die gleichen Einschränkungen sind für geöffnete Handles für Transaktionsverzeichnisvorgänge wie für Dateien vorhanden. Weitere Informationen finden Sie unter [Löschen einer Datei.](#deleting-a-file)

 

## <a name="directory-locking-issues"></a>Probleme beim Sperren von Verzeichnissen

Wenn eine Datei in einer Transaktion geändert wird, werden alle Verzeichniskomponenten des Pfads zur Datei als *angeheftet gegen umbenennen* bezeichnet, bis die Transaktion endet. Das heißt, das System verhindert, dass Sie sie umbenennen, bis für die Transaktion ein Commit oder rollback ausgeführt wird. Der Versuch, ein Verzeichnis umzubenennen, das ein Vorgänger einer Datei ist, die in einer laufenden Transaktion geändert wurde, schlägt mit dem Fehler **\_ ERROR CANT BREAK \_ \_ TRANSACTIONAL \_ DEPENDENCY** fehl.

## <a name="directory-enumeration"></a>Verzeichnisenumeration

Der Inhalt eines Verzeichnisses kann geändert werden, während eine Enumeration ausgeführt wird, weil APIs verwendet werden, die aufzählen, z. B. die Funktionen [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) und [**FindNextFile.**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)

Änderungen an einem Verzeichnis außerhalb einer Transaktion sind nicht von der Transaktion isoliert und sofort innerhalb der Transaktion sichtbar. Wenn beispielsweise ein nicht transaktiver Writer einem Verzeichnis eine Datei hinzufügt, ist die neue Datei sofort innerhalb der Transaktion sichtbar, sodass der Aufruf der [**Funktion FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) oder [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) die neue Datei zurückgibt.

Änderungen, die an einem Verzeichnis innerhalb einer Transaktion vorgenommen werden, werden isoliert, bis ein Commit für die Transaktion ausgeführt wird. Beispielsweise eine Datei, die im Verzeichnis als Teil der Transaktion erstellt wurde. Ein nicht transaktiver Reader, der die [**FindFirstFile-**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) oder [**FindNextFile-Funktion aufruft,**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) sieht die neu erstellte Datei erst nach dem Commit der Transaktion.

## <a name="memory-mapped-files"></a>Speicherabbilddateien

Der Client muss die [**FlushViewOfFile-Funktion**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) aufrufen, das Dateizuordnungsobjekt schließen und das Dateihandle schließen, bevor die zugeordnete Transaktion für eine speicherabbildete Datei committet wird.

## <a name="named-streams"></a>Benannte Datenströme

Benannte Datenströme sind vollständig transaktional, aber das Sperren erfolgt auf Dateiebene und nicht auf Streamebene. Writer von außerhalb einer Transaktion, die versuchen, einen Stream innerhalb einer gesperrten Datei zu ändern, erhalten den Fehler **ERROR \_ SHARING \_ VIOLATION**.

Sie können einen sekundären Stream in einer Transaktion nicht umbenennen.

## <a name="renaming-a-file-or-directory"></a>Umbenennen einer Datei oder eines Verzeichnisses

Um eine Datei als transaktiven Vorgang umzubenennen, rufen [**Sie MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) auf, um die Datei zu verschieben.

## <a name="reparse-points"></a>Reparse Points

Änderungen an den Wiederholungspunkten werden transaktiviert, d. h., wenn einer Datei in einer Transaktion ein neuer Wiederholungspunkt zugewiesen wird, ist er für die anderen Transaktionen nicht sichtbar. Ebenso sind Änderungen oder das Entfernen eines vorhandenen Wiederholungspunkts erst nach dem Commit sichtbar.

## <a name="error-codes"></a>Fehlercodes

Der Kerneltransaktions-Manager (KERNEL Transaction Manager, CSV) verwendet die Systemfehlercodes im Bereich von 6700 bis 6799. Transaktionales NTFS (TxF) verwendet Windows Fehlercodes im Bereich von 6800 bis 6899. Weitere Informationen finden Sie unter WinError.h und Systemfehlercodes (6000-8199).

## <a name="encrypted-file-system"></a>Verschlüsseltes Dateisystem

TxF unterstützt keine Vorgänge für EFS-Dateien. Sie können keine EFS-verschlüsselte Datei für Transaktionen öffnen. Beim Aufrufen der [**CreateFileTransacted-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) für eine EFS-Datei tritt der Fehler **FEHLER \_ EFS \_ NOT ALLOWED \_ \_ IN \_ TRANSACTION** auf. Ebenso schlägt der Aufruf der [**EncryptFile-Funktion**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) für eine Datei in einer Transaktion mit dem **Fehler FEHLER \_ EFS NOT ALLOWED IN \_ \_ \_ \_ TRANSACTION** fehl.

## <a name="file-io-functions-and-transactional-ntfs"></a>Datei-E/A-Funktionen und transaktionales NTFS

TxF stellt neue transaktive Funktionen bereit, die einen Dateinamen annehmen und das Verhalten vorhandener Datei-E/A-API-Funktionen ändern, die ein Dateihandle annehmen.

### <a name="transacted-functions"></a>Transaktive Funktionen

Wenn Sie anstelle der nicht transaktiven Version keine der folgenden transaktiven Funktionen aufrufen, wird der Vorgang nicht transaktiv:

-   [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**CreateSymbolicLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**FindFirstFileNameTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**FindFirstStreamTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**GetFullPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**GetLongPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

Beispielsweise verfügt die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) jetzt über eine transaktive Version: [**CreateFileTransacted.**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)

### <a name="file-io-functions-changed-by-txf"></a>Von TxF geänderte Datei-E/A-Funktionen

In der folgenden Tabelle sind die Funktionen aufgeführt, deren Verhalten von Transaktions-NTFS beeinflusst wird. Das Verhalten der [**ReadFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) hängt beispielsweise davon ab, ob der *hFile-Parameter* von der [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) oder der [**CreateFileTransacted-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) erstellt wurde.



| Funktion                                                                                                                                                                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**Closehandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Anwendungen sollten alle Handles schließen, die an eine Transaktion gebunden sind, bevor ein Commit für die Transaktion ausgeführt wird. Eine Anwendung muss ein mit **FILE \_ FLAG DELETE ON \_ \_ \_ CLOSE** geöffnetes Transaktionshandle schließen, bevor ein Commit für die Transaktion ausgeführt wird, damit der Löschvorgang ausgeführt wird.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Wenn *hFile* eine Transaktion zugeordnet ist, wird das Dateizuordnungsobjekt, das von dieser Funktion erstellt wird, derselben Transaktion zugeordnet. Änderungen, die über Ansichten dieses Dateizuordnungsobjekts vorgenommen werden, werden durchgeführt. Anwendungen müssen [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile)aufrufen, die Zuordnung aller Ansichten aufheben und alle Handles für das Dateizuordnungsobjekt schließen, bevor transaktionsbezogene Änderungen committet werden.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Wenn eine Transaktion an das Dateienumerationshandle gebunden ist, unterliegen die zurückgegebenen Dateien den Transaktionsisolationsregeln.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | Sie können den Komprimierungsstatus einer Datei, die von [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)geöffnet wurde, nicht ändern.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) und [ **GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | Wenn eine Transaktion an das Dateihandle gebunden ist, gibt die Funktion Informationen für die isolierte Dateiansicht zurück.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) und [ **GetFileSizeEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | Wenn eine Transaktion an das Dateihandle gebunden ist, gibt die Funktion Informationen für die isolierte Dateiansicht zurück.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Wenn das Volume Dateisystemtransaktionen unterstützt, gibt die Funktion **FILE \_ SUPPORTS \_ TRANSACTIONS** in *lpFileSystemFlags* zurück.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) und [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Wenn dem Dateihandle, das zum Erstellen des zugeordneten Dateizuordnungsobjekts verwendet wird, eine Transaktion zugeordnet ist, wird die zugeordnete Sicht transaktiv. Wenn die Ansicht verwendet wird, um transaktive Änderungen an einer Datei vorzunehmen, muss der Benutzer [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile)aufrufen, das Dateizuordnungsobjekt schließen und das Dateihandle schließen, bevor die zugeordnete Transaktion committet wird.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | Wenn eine Transaktion an das Verzeichnishandle gebunden ist, spiegeln die Benachrichtigungen die isolierte Ansicht des Verzeichnisses wider. Änderungen an Dateien außerhalb der transaktiven Ansicht des Verzeichnisses sind nicht in den Benachrichtigungen enthalten.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile,**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)und [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | Wenn eine Transaktion an das Dateihandle gebunden ist, gibt die Funktion Daten aus der transaktiven Ansicht der Datei zurück. Ein transaktives Lesehandle zeigt für die Dauer des Handles garantiert die gleiche Ansicht einer Datei an.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Wenn eine Transaktion an das Handle gebunden ist, wird die Änderung an der End-of-File-Position durchgeführt.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | Wenn eine Transaktion an das Handle gebunden ist, werden die vorgenommenen Änderungen für die Informationsklassen **FileBasicInfo,** **FileRenameInfo,** **FileAllocationInfo,** **FileEndOfFileInfo** und **FileDispositionInfo** durchgeführt.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**SetFileShortName**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | Wenn eine Transaktion an das Handle gebunden ist, wird die Änderung des Kurznamens der Datei durchgeführt.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | Wenn eine Transaktion an das Handle gebunden ist, wird die Änderung der Dateizeit durchgeführt.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)und [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | Wenn eine Transaktion an das Dateihandle gebunden ist, wird der Dateischreibvorgang durchgeführt.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

