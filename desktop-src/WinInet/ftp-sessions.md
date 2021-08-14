---
title: FTP-Sitzungen
description: WinINet ermöglicht Anwendungen das Navigieren und Bearbeiten von Verzeichnissen und Dateien auf einem FTP-Server. Da CERN-Proxys FTP nicht unterstützen, müssen Anwendungen, die ausschließlich einen CERN-Proxy verwenden, die InternetOpenUrl-Funktion verwenden.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70942fea5865fa96c9ee81ab996238e3f382471a701ac44969d1ff8797c8780d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113973"
---
# <a name="ftp-sessions"></a>FTP-Sitzungen

WinINet ermöglicht Anwendungen das Navigieren und Bearbeiten von Verzeichnissen und Dateien auf einem FTP-Server. Da CERN-Proxys FTP nicht unterstützen, müssen Anwendungen, die ausschließlich einen CERN-Proxy verwenden, die [**InternetOpenUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwenden. Weitere Informationen zur Verwendung von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)finden Sie unter Direktes Zugreifen [auf URLs.](handling-uniform-resource-locators.md)

Um eine FTP-Sitzung zu starten, verwenden [**Sie InternetConnect,**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) um das Sitzungshand handle zu erstellen.

Mit WinINet können Sie die folgenden Aktionen auf einem FTP-Server ausführen:

-   Navigieren Sie zwischen Verzeichnissen.
-   Aufzählen, Erstellen, Entfernen und Umbenennen von Verzeichnissen.
-   Umbenennen, Hochladen, Herunterladen und Löschen von Dateien.

Die Navigation wird von den [**Funktionen FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) und [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) bereitgestellt. Diese Funktionen verwenden das Sitzungshandchen, das durch einen vorherigen Aufruf von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, um zu bestimmen, in welchem Verzeichnis sich die Anwendung derzeit befindet, oder um in ein anderes Unterverzeichnis zu wechseln.

Die Verzeichnisenumeration wird mithilfe der [**Funktionen FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) und [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) ausgeführt. [**FtpFindFirstFile verwendet**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellte Sitzungshand handle, um die erste Datei zu finden, die den angegebenen Suchkriterien entspricht, und gibt ein Handle zurück, um die Verzeichnisenumeration fortzufahren. [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) verwendet das von [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) zurückgegebene Handle, um die nächste Datei zurückzukehren, die den ursprünglichen Suchkriterien entspricht. Die Anwendung sollte weiterhin [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) aufrufen, bis im Verzeichnis keine Dateien mehr vorhanden sind.

Verwenden Sie [**die FtpCreateDirectory-Funktion,**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) um neue Verzeichnisse zu erstellen. Diese Funktion verwendet das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellte Sitzungshand handle und erstellt das Verzeichnis, das durch die an die Funktion übergebene Zeichenfolge angegeben wird. Die Zeichenfolge kann einen Verzeichnisnamen relativ zum aktuellen Verzeichnis oder einen vollqualifizierten Verzeichnispfad enthalten.

Um Dateien oder Verzeichnisse umzubenennen, kann die Anwendung [**FtpRenameFile aufrufen.**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) Diese Funktion ersetzt den ursprünglichen Namen durch den neuen Namen, der an die Funktion übergeben wird. Der Name der Datei oder des Verzeichnisses kann relativ zum aktuellen Verzeichnis oder ein vollqualifizierter Name sein.

Zum Hochladen oder Platzieren von Dateien auf einem FTP-Server kann die Anwendung entweder [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) oder [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (zusammen [**mit InternetWriteFile) verwenden.**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) kann verwendet werden, wenn die Datei bereits lokal vorhanden ist, während [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) verwendet werden können, wenn Daten in eine Datei auf dem FTP-Server geschrieben werden müssen.

Zum Herunterladen oder Herunterladen von Dateien kann die Anwendung entweder [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) oder [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (mit [**InternetReadFile) verwenden.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) wird verwendet, um eine Datei von einem FTP-Server abzurufen und lokal zu speichern, während [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) verwendet werden können, um zu steuern, wohin die heruntergeladenen Informationen gehen (z. B. kann die Anwendung die Informationen in einem Bearbeitungsfeld anzeigen).

Löschen Sie Dateien auf einem FTP-Server mithilfe der [**FtpDeleteFile-Funktion.**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) Diese Funktion entfernt einen Dateinamen, der entweder relativ zum aktuellen Verzeichnis oder zu einem vollqualifizierten Dateinamen vom FTP-Server ist. [**FtpDeleteFile erfordert**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) ein Sitzungshandl, das von [**InternetConnect zurückgegeben wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

## <a name="ftp-function-handles"></a>FTP-Funktionshandles

Damit die FTP-Funktionen ordnungsgemäß funktionieren, benötigen sie bestimmte [**HINTERNET-Handles.**](appendix-a-hinternet-handles.md) Diese Handles müssen in einer bestimmten Reihenfolge erstellt werden, beginnend mit dem von InternetOpen erstellten [**Stammhandles.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) kann dann ein FTP-Sitzungshand handle erstellen.

Das folgende Diagramm zeigt die Funktionen, die vom FTP-Sitzungshand handle abhängig sind, das von [**InternetConnect zurückgegeben wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Die schattierten Felder stellen Funktionen dar, die [**HINTERNET-Handles**](appendix-a-hinternet-handles.md) zurückgeben, während die einfachen Felder Funktionen darstellen, die das HINTERNET-Handle verwenden, das von der Funktion erstellt wurde, von der sie abhängen.

![FTP-Funktionen, die vom ftp-Sitzungshand handle abhängig sind, das von internetconnect zurückgegeben wird](images/ax-wnt06.png)

Das folgende Diagramm zeigt die beiden Funktionen, die [HINTERNET-Handles](appendix-a-hinternet-handles.md) zurückgeben, und die Funktionen, die davon abhängig sind. Die schattierten Felder stellen Funktionen dar, die **HINTERNET-Handles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **HINTERNET-Handle** verwenden, das von der Funktion erstellt wurde, von der sie abhängen.

![FTP-Funktionen, die Hinternethandles zurückgeben](images/ax-wnt03.png)

Weitere Informationen finden Sie unter [HINTERNET Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Verwenden der WinINet-Funktionen für FTP-Sitzungen

Die folgenden Funktionen werden während FTP-Sitzungen verwendet. Diese Funktionen werden von CERN-Proxys nicht erkannt. Anwendungen, die über CERN-Proxys funktionieren müssen, sollten [**InternetOpenUrl verwenden**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und direkt auf die Ressourcen zugreifen. Weitere Informationen zum direkten Zugriff auf Ressourcen finden Sie unter [Direkter Zugriff auf URLs.](handling-uniform-resource-locators.md)



| Funktion                                                 | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Erstellt ein neues Verzeichnis auf dem Server. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                  |
| [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Löscht eine Datei vom Server. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                         |
| [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Startet die Dateienumeration oder Dateisuche im aktuellen Verzeichnis. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)        |
| [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Gibt das aktuelle Verzeichnis des Clients auf dem Server zurück. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Ruft eine Datei vom Server ab. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                       |
| [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Initiiert den Zugriff auf eine Datei auf dem Server zum Lesen oder Schreiben. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) |
| [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Schreibt eine Datei auf den Server. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                            |
| [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Löscht ein Verzeichnis auf dem Server. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                      |
| [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Benennt eine Datei auf dem Server um. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                           |
| [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Ändert das aktuelle Verzeichnis des Clients auf dem Server. Diese Funktion erfordert ein handle, das von [**InternetConnect erstellt wird.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Schreibt Daten in eine geöffnete Datei auf dem Server. Diese Funktion erfordert ein von [**FtpOpenFile erstelltes Handle.**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                                      |



 

### <a name="starting-an-ftp-session"></a>Starten einer FTP-Sitzung

Die Anwendung richtet eine FTP-Sitzung ein, indem [**sie InternetConnect für**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ein handle aufruft, das [**von InternetOpen erstellt wurde.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) benötigt den Servernamen, die Portnummer, den Benutzernamen, das Kennwort und den Diensttyp (muss auf INTERNET \_ SERVICE FTP festgelegt \_ werden). Für die passive FTP-Semantik muss die Anwendung auch das [INTERNET \_ FLAG \_ PASSIVE-Flag](api-flags.md) festlegen.

Die Werte INTERNET \_ DEFAULT FTP PORT und INTERNET INVALID PORT NUMBER können für die \_ \_ \_ \_ \_ Portnummer verwendet werden. INTERNET \_ DEFAULT FTP PORT verwendet den \_ \_ FTP-Standardport, der Diensttyp muss jedoch weiterhin festgelegt werden. INTERNET \_ INVALID PORT NUMBER verwendet den Standardwert für den \_ \_ angegebenen Diensttyp.

Die Werte für Benutzername und Kennwort können auf NULL festgelegt **werden.** Wenn beide Werte auf **NULL** festgelegt sind, verwendet [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) "anonymous" für den Benutzernamen und die E-Mail-Adresse des Benutzers für das Kennwort. Wenn nur das Kennwort auf **NULL festgelegt** ist, wird der an [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) übergebene Benutzername für den Benutzernamen und eine leere Zeichenfolge für das Kennwort verwendet. Wenn keiner der Werte **NULL ist,** werden der Benutzername und das Kennwort für [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet.

### <a name="enumerating-directories"></a>Aufzählen von Verzeichnissen

Die Enumeration eines Verzeichnisses auf einem FTP-Server erfordert die Erstellung eines Handles durch [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Dieses Handle ist eine Verzweigung des Sitzungshandges, das von [**InternetConnect erstellt wurde.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) sucht die erste Datei oder das erste Verzeichnis auf dem Server und gibt sie in einer [**WIN32 \_ FIND \_ DATA-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) zurück. Verwenden [**Sie InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) bis ERROR [**NO MORE FILES zurückgegeben \_ \_ \_ wird.**](wininet-errors.md) Diese Methode sucht alle nachfolgenden Dateien und Verzeichnisse auf dem Server. Weitere Informationen zu [**InternetFindNextFile finden**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)Sie unter [Suchen der nächsten Datei.](common-functions.md)

Um zu ermitteln, ob die von [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) oder [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) abgerufene Datei ein Verzeichnis ist, überprüfen Sie den **dwFileAttributes-Member** der [**WIN32 \_ FIND \_ DATA-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) um festzustellen, ob sie gleich FILE \_ ATTRIBUTE DIRECTORY \_ ist.

Wenn die Anwendung Änderungen auf dem FTP-Server vornimmt oder sich der FTP-Server häufig ändert, sollten die [FLAGs INTERNET \_ FLAG NO \_ CACHE \_ \_ WRITE](api-flags.md) und [INTERNET FLAG \_ \_ RELOAD](api-flags.md) in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)festgelegt werden. Diese Flags stellen sicher, dass die vom FTP-Server abgerufenen Verzeichnisinformationen aktuell sind.

Nachdem die Anwendung die Verzeichnisenumeration abgeschlossen hat, muss die Anwendung [**internetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) für das von [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)erstellte Handle aufrufen. Bis dieses Handle geschlossen ist, kann die Anwendung [**ftpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) für das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellte Sitzungshandle nicht erneut aufrufen. Wenn [**ftpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) auf dem gleichen Sitzungshandle aufgerufen wird, bevor der vorherige Aufruf derselben Funktion geschlossen wird, schlägt die Funktion fehl und gibt [ERROR FTP TRANSFER IN \_ \_ \_ \_ PROGRESS](wininet-errors.md)zurück.

Im folgenden Beispiel wird der Inhalt eines FTP-Verzeichnisses in ein Listenfeld-Steuerelement auflistet. Der *hConnection-Parameter* ist ein Handle, das von der [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) zurückgegeben wird, nachdem eine FTP-Sitzung eingerichtet wurde. Beispielquellcode für die InternetErrorOut-Funktion, auf die in diesem Beispiel verwiesen wird, finden Sie im Thema [Behandeln von Fehlern.](appendix-c-handling-errors.md)


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a>Navigieren in Verzeichnissen

Die Funktionen [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) und [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) verarbeiten die Verzeichnisnavigation.

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) gibt das aktuelle Verzeichnis der Anwendung auf dem FTP-Server zurück. Der Verzeichnispfad aus dem Stammverzeichnis auf dem FTP-Server ist enthalten.

[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) ändert das Arbeitsverzeichnis auf dem Server. Die an [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) übergebenen Verzeichnisinformationen können entweder ein teilweiser oder vollqualifizierte Pfadname relativ zum aktuellen Verzeichnis sein. Wenn sich die Anwendung beispielsweise derzeit im Verzeichnis "public/info" und der Pfad "ftp/example" befindet, ändert [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) das aktuelle Verzeichnis in "public/info/ftp/example".

Im folgenden Beispiel wird das FTP-Sitzungshandle hConnection verwendet, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegeben wird. Der neue Verzeichnisname wird aus dem Bearbeitungsfeld des übergeordneten Dialogfelds übernommen, dessen IDC im *nDirNameId-Parameter* übergeben wird. Bevor die Verzeichnisänderung vorgenommen wird, ruft die Funktion das aktuelle Verzeichnis ab und speichert es im gleichen Bearbeitungsfeld. Der Am Ende aufgerufene Souce-Code für die DisplayFtpDir-Funktion ist oben aufgeführt.


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a>Bearbeiten von Verzeichnissen auf einem FTP-Server

WinINet bietet die Möglichkeit, Verzeichnisse auf einem FTP-Server zu erstellen und zu entfernen, für den die Anwendung über die erforderlichen Berechtigungen verfügt. Wenn sich die Anwendung bei einem Server mit einem bestimmten Benutzernamen und Kennwort anmelden muss, können die Werte beim Erstellen des FTP-Sitzungshandle in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet werden.

Die [**FtpCreateDirectory-Funktion**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) verwendet ein gültiges FTP-Sitzungshandle und eine **auf NULL** endende Zeichenfolge, die entweder einen vollqualifizierten Pfad oder einen Namen relativ zum aktuellen Verzeichnis enthält und ein Verzeichnis auf dem FTP-Server erstellt.

Das folgende Beispiel zeigt zwei separate Aufrufe von [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). In beiden Beispielen ist hFtpSession das Sitzungshandle, das von der [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, und das Stammverzeichnis ist das aktuelle Verzeichnis.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

Die [**FtpRemoveDirectory-Funktion**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) verwendet ein Sitzungshandle und eine **mit NULL** endende Zeichenfolge, die entweder einen vollqualifizierten Pfad oder einen Namen relativ zum aktuellen Verzeichnis enthält und dieses Verzeichnis vom FTP-Server entfernt.

Das folgende Beispiel zeigt zwei Beispielaufrufe von [**FtpRemoveDirectory.**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) Bei beiden Aufrufen ist hFtpSession das Sitzungshandle, das von der [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, und das Stammverzeichnis ist das aktuelle Verzeichnis. Das Stammverzeichnis enthält das Verzeichnis "test" und im Verzeichnis "test" das Verzeichnis "example".

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



Im folgenden Beispiel wird ein neues Verzeichnis auf dem FTP-Server erstellt. Der neue Verzeichnisname wird aus dem Bearbeitungsfeld des übergeordneten Dialogfelds übernommen, dessen IDC im *nDirNameId-Parameter* übergeben wird. Das *hConnection-Handle* wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) nach dem Einrichten einer FTP-Sitzung erstellt. Der Quellcode für die Funktion DisplayFtpDir, die am Ende aufgerufen wird, ist oben aufgeführt.


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



Im folgenden Beispiel wird ein Verzeichnis vom FTP-Server gelöscht. Der Name des zu löschenden Verzeichnisses wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC an den *nDirNameId-Parameter* übergeben wird. Das *hConnection-Handle* wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) nach dem Einrichten einer FTP-Sitzung erstellt. Der Quellcode für die Funktion DisplayFtpDir, die am Ende aufgerufen wird, ist oben aufgeführt.


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a>Abrufen von Dateien auf einem FTP-Server

Es gibt drei Methoden zum Abrufen von Dateien von einem FTP-Server:

-   Verwenden Sie [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Verwenden Sie [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)
-   Verwenden Sie [**FtpGetFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)

Weitere Informationen zur Verwendung der [**InternetReadFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) finden Sie unter [Lesen von Dateien.](common-functions.md)

Wenn die URL der Datei verfügbar ist, kann die Anwendung [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) aufrufen, um eine Verbindung mit dieser URL herzustellen, und dann [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) verwenden, um den Download der Datei zu steuern. Dies ermöglicht der Anwendung eine strengere Kontrolle über den Download und eignet sich ideal für Situationen, in denen keine anderen Vorgänge auf dem FTP-Server ausgeführt werden müssen. Weitere Informationen zum direkten Zugriff auf Ressourcen finden Sie unter [Direktes Zugreifen auf URLs.](handling-uniform-resource-locators.md)

Wenn die Anwendung ein FTP-Sitzungshandle für den Server mit [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)eingerichtet hat, kann die Anwendung [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) mit dem vorhandenen Dateinamen und mit einem neuen Namen für die lokal gespeicherte Datei aufrufen. Die Anwendung kann dann [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) verwenden, um die Datei herunterzuladen. Dies ermöglicht der Anwendung eine strengere Kontrolle über den Download und behält die Verbindung mit dem FTP-Server bei, sodass weitere Befehle ausgeführt werden können.

Wenn die Anwendung keine strenge Kontrolle über den Download benötigt, kann die Anwendung [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) mit dem FTP-Sitzungshandle, dem Remotedateinamen und dem lokalen Dateinamen verwenden, um die Datei abzurufen. [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) führt die gesamte Buchhaltung und den Mehraufwand aus, die mit dem Lesen einer Datei von einem FTP-Server und dem lokalen Speichern verbunden sind.

Im folgenden Beispiel wird eine Datei von einem FTP-Server abgerufen und lokal gespeichert. Der Name der Datei auf dem FTP-Server stammt aus dem Bearbeitungsfeld im übergeordneten Dialogfeld, dessen IDC im *nFtpFileNameId-Parameter* übergeben wird, und der lokale Name, unter dem die Datei gespeichert wird, stammt aus dem Bearbeitungsfeld, dessen IDC im *nLocalFileNameId-Parameter* übergeben wird. Das *hConnection-Handle* wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) nach dem Einrichten einer FTP-Sitzung erstellt.


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a>Platzieren von Dateien auf einem FTP-Server

Es gibt zwei Methoden zum Platzieren einer Datei auf einem FTP-Server:

-   Verwenden Sie [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) mit [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).
-   Verwenden Sie [**FtpPutFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)

Eine Anwendung, die Daten an einen FTP-Server senden muss, aber nicht über eine lokale Datei verfügt, die alle Daten enthält, sollte [**ftpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) verwenden, um eine Datei auf dem FTP-Server zu erstellen und zu öffnen. Die Anwendung kann dann [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) verwenden, um die Informationen in die Datei hochzuladen.

Wenn die Datei bereits lokal vorhanden ist, kann die Anwendung [**ftpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) verwenden, um die Datei auf den FTP-Server hochzuladen. [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) führt den gesamten Mehraufwand aus, der mit dem Hochladen einer lokalen Datei auf einen FTP-Remoteserver verbunden ist.

Im folgenden Beispiel wird eine lokale Datei auf den FTP-Server kopiert. Der lokale Name der Datei stammt aus dem Bearbeitungsfeld im übergeordneten Dialogfeld, dessen IDC im *nLocalFileNameId-Parameter* übergeben wird, und der Name, unter dem die Datei auf dem FTP-Server gespeichert wird, wird aus dem Bearbeitungsfeld übernommen, dessen IDC im *nFtpFileNameId-Parameter* übergeben wird. Das *hConnection-Handle* wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) nach dem Einrichten einer FTP-Sitzung erstellt.


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a>Löschen von Dateien von einem FTP-Server

Verwenden Sie die [**FtpDeleteFile-Funktion,**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) um eine Datei von einem FTP-Server zu löschen. Die aufrufende Anwendung muss über die erforderlichen Berechtigungen zum Löschen einer Datei vom FTP-Server verfügen.

Im folgenden Beispiel wird eine Datei vom FTP-Server gelöscht. Der Name der zu löschenden Datei wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC im *nFtpFileNameId-Parameter* übergeben wird. Das *hConnection-Handle* wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) nach dem Einrichten einer FTP-Sitzung erstellt. Da diese Funktion keine Dateiauflistungen oder Verzeichnisanzeigen aktualisiert, sollte der aufrufende Prozess dies nach erfolgreichem Löschen tun.


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a>Umbenennen von Dateien und Verzeichnissen auf einem FTP-Server

Dateien und Verzeichnisse auf einem FTP-Server können mithilfe der [**FtpRenameFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) umbenannt werden. [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) akzeptiert zwei **mit NULL** endende Zeichenfolgen, die entweder teilweise oder vollqualifizierte Namen relativ zum aktuellen Verzeichnis enthalten. Die Funktion ändert den Namen der Datei, die von der ersten Zeichenfolge angegeben wird, in den Namen, der von der zweiten Zeichenfolge angegeben wird.

Im folgenden Beispiel wird eine Datei oder ein Verzeichnis auf dem FTP-Server umbenannt. Der aktuelle Name der Datei oder des Verzeichnisses stammt aus dem Bearbeitungsfeld im übergeordneten Dialogfeld, dessen IDC im *nOldFileNameId-Parameter* übergeben wird, und der neue Name wird aus dem Bearbeitungsfeld übernommen, dessen IDC im *nNewFileNameId-Parameter* übergeben wird. Das *hConnection-Handle* wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) nach dem Einrichten einer FTP-Sitzung erstellt. Da diese Funktion keine Dateiauflistungen oder Verzeichnisanzeigen aktualisiert, sollte der aufrufende Prozess dies nach erfolgreicher Umbenennung tun.


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 