---
title: FTP-Sitzungen
description: WinInet ermöglicht es Anwendungen, Verzeichnisse und Dateien auf einem FTP-Server zu navigieren und zu bearbeiten. Da CERN-Proxys FTP nicht unterstützen, müssen Anwendungen, die einen CERN-Proxy verwenden, exklusiv die InternetOpenURL-Funktion verwenden.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039285"
---
# <a name="ftp-sessions"></a>FTP-Sitzungen

WinInet ermöglicht es Anwendungen, Verzeichnisse und Dateien auf einem FTP-Server zu navigieren und zu bearbeiten. Da CERN-Proxys FTP nicht unterstützen, müssen Anwendungen, die einen CERN-Proxy verwenden, exklusiv die [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion verwenden. Weitere Informationen zur Verwendung von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md).

Verwenden Sie zum Starten einer FTP-Sitzung [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , um das Sitzungs Handle zu erstellen.

Mit WinInet können Sie die folgenden Aktionen auf einem FTP-Server ausführen:

-   Navigieren zwischen Verzeichnissen.
-   Auflisten, erstellen, entfernen und Umbenennen von Verzeichnissen.
-   Umbenennen, hochladen, herunterladen und Löschen von Dateien.

Die Navigation wird von den Funktionen [**ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) und [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) bereitgestellt. Diese Funktionen verwenden das Sitzungs handle, das von einem vorherigen [**Internet Verbindungs**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) aufrufungstyp erstellt wurde, um zu bestimmen, in welchem Verzeichnis sich die Anwendung derzeit befindet, oder um in ein anderes Unterverzeichnis zu wechseln.

Die verzeichnisenumeration wird mithilfe der Funktionen [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) und [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) ausgeführt. [**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) verwendet das Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, um die erste Datei zu suchen, die den angegebenen Suchkriterien entspricht, und gibt ein Handle zurück, um die verzeichnisenumeration fortzusetzen. [**Internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) verwendet das von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) zurückgegebene Handle, um die nächste Datei zurückzugeben, die den ursprünglichen Suchkriterien entspricht. Die Anwendung sollte weiterhin [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) aufruft, bis keine weiteren Dateien mehr im Verzeichnis vorhanden sind.

Verwenden Sie die [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) -Funktion, um neue Verzeichnisse zu erstellen. Diese Funktion verwendet das Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, und erstellt das Verzeichnis, das durch die an die Funktion über gegebene Zeichenfolge angegeben wird. Die Zeichenfolge kann einen Verzeichnisnamen relativ zum aktuellen Verzeichnis oder einen voll qualifizierten Verzeichnispfad enthalten.

Zum Umbenennen von Dateien oder Verzeichnissen kann die Anwendung [**ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)aufruft. Diese Funktion ersetzt den ursprünglichen Namen durch den neuen Namen, der an die Funktion übermittelt wurde. Der Name der Datei oder des Verzeichnisses kann relativ zum aktuellen Verzeichnis oder ein voll qualifizierter Name sein.

Um Dateien auf einem FTP-Server hochzuladen oder zu platzieren, kann die Anwendung entweder [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) oder [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (zusammen mit [**internetschreitedatei**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)) verwenden. [**Ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) kann verwendet werden, wenn die Datei bereits lokal vorhanden ist, während [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**internetschreitefile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) verwendet werden können, wenn Daten in eine Datei auf dem FTP-Server geschrieben werden müssen.

Zum Herunterladen oder Herunterladen von Dateien kann die Anwendung entweder [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) oder [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (mit [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)) verwenden. [**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) wird verwendet, um eine Datei von einem FTP-Server abzurufen und lokal zu speichern, während [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) verwendet werden können, um zu steuern, wo die heruntergeladenen Informationen erfolgen (z. b. die Anwendung kann die Informationen in einem Bearbeitungsfeld anzeigen).

Löschen Sie Dateien auf einem FTP-Server mithilfe der [**ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) -Funktion. Diese Funktion entfernt einen Dateinamen, der entweder relativ zum aktuellen Verzeichnis oder zu einem voll qualifizierten Dateinamen vom FTP-Server ist. [**Ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) erfordert ein Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegeben wurde.

## <a name="ftp-function-handles"></a>FTP-Funktions Handles

Um ordnungsgemäß zu funktionieren, benötigen die FTP-Funktionen bestimmte Typen von [**hinternethandles**](appendix-a-hinternet-handles.md) . Diese Handles müssen in einer bestimmten Reihenfolge erstellt werden, beginnend mit dem Stamm handle, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)erstellt wurde. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) kann dann ein FTP-Sitzungs Handle erstellen.

Das folgende Diagramm zeigt die Funktionen, die von dem von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegebenen FTP-Sitzungs handle abhängig sind. Die schattierten Felder stellen Funktionen dar, die [**hinternethandles**](appendix-a-hinternet-handles.md) zurückgeben, während die einfachen Felder Funktionen darstellen, die das hinternethandle verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.

![FTP-Funktionen, die vom von InternetConnect zurückgegebenen FTP-Sitzungs handle abhängen](images/ax-wnt06.png)

Das folgende Diagramm zeigt die beiden Funktionen, die [hinternethandles](appendix-a-hinternet-handles.md) und die von ihnen abhängigen Funktionen zurückgeben. Die schattierten Felder stellen Funktionen dar, die **hinternethandles** zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.

![FTP-Funktionen, die HINTERNET Handles zurückgeben](images/ax-wnt03.png)

Weitere Informationen finden Sie unter [HINTERNET Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Verwenden der WinInet-Funktionen für FTP-Sitzungen

Die folgenden Funktionen werden bei FTP-Sitzungen verwendet. Diese Funktionen werden von CERN-Proxys nicht erkannt. Anwendungen, die über CERN-Proxys funktionieren müssen, sollten [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwenden und direkt auf die Ressourcen zugreifen. Weitere Informationen zum direkten Zugriff auf Ressourcen finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md).



| Funktion                                                 | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Erstellt ein neues Verzeichnis auf dem Server. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                                  |
| [**Ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Löscht eine Datei vom Server. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                                         |
| [**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Startet die Dateienumeration oder die Dateisuche im aktuellen Verzeichnis. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.        |
| [**Ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Gibt das aktuelle Verzeichnis des Clients auf dem Server zurück. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                   |
| [**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Ruft eine Datei vom Server ab. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                                       |
| [**Ftpopumfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Initiiert den Zugriff auf eine Datei auf dem Server zum Lesen oder schreiben. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde. |
| [**Ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Schreibt eine Datei auf den Server. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                                            |
| [**Ftpremuvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Löscht ein Verzeichnis auf dem Server. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                                      |
| [**Ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Benennt eine Datei auf dem Server um. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                                           |
| [**Ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Ändert das aktuelle Verzeichnis des Clients auf dem Server. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                   |
| [**Internetschreibdatei**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Schreibt Daten in eine geöffnete Datei auf dem Server. Diese Funktion erfordert ein Handle, das von [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)erstellt wurde.                                      |



 

### <a name="starting-an-ftp-session"></a>Starten einer FTP-Sitzung

Die Anwendung richtet eine FTP-Sitzung ein, indem Sie [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) für ein Handle aufrufen, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)erstellt wurde. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) benötigt den Servernamen, die Portnummer, den Benutzernamen, das Kennwort und den Diensttyp (der auf Internet Dienst-FTP festgelegt sein muss \_ \_ ). Bei der passiven FTP-Semantik muss die Anwendung auch das [Internet \_ Flag \_ passiv](api-flags.md) -Flag festlegen.

Der Internet \_ \_ Standardftp \_ -Port und Internet- \_ ungültige \_ Port \_ Nummern Werte können für die Portnummer verwendet werden. Der Standardftp- \_ \_ \_ Port des Internets verwendet den Standardftp-Port, aber der Diensttyp muss noch festgelegt werden. Internet \_ ungültige \_ Port \_ Nummer verwendet den Standardwert für den bestimmten Diensttyp.

Die Werte für Benutzername und Kennwort können auf **null** festgelegt werden. Wenn beide Werte auf **null** festgelegt sind, verwendet [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) "Anonymous" als Benutzernamen und die e-Mail-Adresse des Benutzers für das Kennwort. Wenn nur das Kennwort auf **null** festgelegt ist, wird der an [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) über gegebene Benutzername als Benutzername verwendet, und für das Kennwort wird eine leere Zeichenfolge verwendet. Wenn kein Wert **null** ist, werden der Benutzername und das Kennwort für [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet.

### <a name="enumerating-directories"></a>Auflisten von Verzeichnissen

Die Enumeration eines Verzeichnisses auf einem FTP-Server erfordert die Erstellung eines Handles durch [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Dieses Handle ist eine Verzweigung des Sitzungs Handles, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde. [**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) sucht die erste Datei oder das erste Verzeichnis auf dem Server und gibt Sie in einer Win32-Such [**\_ \_ Daten**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Struktur zurück. Verwenden Sie [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , bis der [**Fehler \_ keine \_ weiteren \_ Dateien**](wininet-errors.md)zurückgibt. Diese Methode sucht alle nachfolgenden Dateien und Verzeichnisse auf dem Server. Weitere Informationen zu [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)finden Sie untersuchen [der nächsten Datei](common-functions.md).

Um festzustellen, ob es sich bei der von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) oder [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) abgerufenen Datei um ein Verzeichnis handelt, überprüfen Sie das Element **dwfileattribute** der [**Win32- \_ \_ Datenstruktur suchen**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) , um festzustellen, ob es gleich dem Datei \_ Attribut Verzeichnis ist \_ .

Wenn die Anwendung Änderungen am FTP-Server vornimmt oder sich der FTP-Server häufig ändert, sollten die Flags " [Internet \_ Flag \_ No \_ Cache \_ Write](api-flags.md) " und " [Internet \_ Flag neu \_ Laden](api-flags.md) " in [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)festgelegt werden. Diese Flags stellen sicher, dass die Verzeichnisinformationen, die vom FTP-Server abgerufen werden, aktuell sind.

Nachdem die Anwendung die verzeichnisenumeration abgeschlossen hat, muss die Anwendung den [**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) -Vorgang für das Handle ausführen, das von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)erstellt wurde. Bis das Handle geschlossen ist, kann die Anwendung [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) nicht mehr für das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellte Sitzungs handle abrufen. Wenn ein [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) -Befehl für das gleiche Sitzungs handle ausgeführt wird, bevor der vorherige-Befehl der gleichen Funktion geschlossen wird, schlägt die Funktion fehl, und es wird die [Fehler-FTP- \_ \_ Übertragung \_ in \_](wininet-errors.md)Bearbeitung zurückgegeben.

Im folgenden Beispiel wird der Inhalt eines FTP-Verzeichnisses in einem Listenfeld-Steuerelement aufgelistet. Der *hconnection* -Parameter ist ein Handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion zurückgegeben wird, nachdem eine FTP-Sitzung eingerichtet wurde. Beispiel Quell Code für die internetterrorout-Funktion, auf die in diesem Beispiel verwiesen wird, finden Sie im Thema [Behandlung von Fehlern](appendix-c-handling-errors.md).


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

Die Funktionen " [**ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) " und " [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) " behandeln die Verzeichnis Navigation.

[**Ftpgetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) gibt das aktuelle Verzeichnis der Anwendung auf dem FTP-Server zurück. Der Verzeichnispfad aus dem Stammverzeichnis auf dem FTP-Server ist enthalten.

[**Ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) ändert das Arbeitsverzeichnis auf dem Server. Bei den an [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) weiter gegebenen Verzeichnisinformationen kann es sich entweder um einen teilweise oder voll qualifizierten Pfadnamen handeln, der relativ zum aktuellen Verzeichnis ist. Wenn sich die Anwendung z. b. zurzeit im Verzeichnis "Public/Info" befindet und der Pfad "FTP/example" lautet, ändert [**ftpsetcurrentdirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) das aktuelle Verzeichnis in "Public/Info/FTP/example".

Im folgenden Beispiel wird das FTP-Sitzungs handle hconnection verwendet, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegeben wird. Der neue Verzeichnisname wird aus dem Bearbeitungsfeld des übergeordneten Dialog Felds übernommen, dessen IDC im *ndirnameid* -Parameter übergeben wird. Bevor die Verzeichnis Änderung vorgenommen wird, ruft die Funktion das aktuelle Verzeichnis ab und speichert es in demselben Bearbeitungsfeld. Der Quelle-Code für die displayftpdir-Funktion, die am Ende aufgerufen wird, ist oben aufgeführt.


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



### <a name="manipulating-directories-on-an-ftp-server"></a>Manipulieren von Verzeichnissen auf einem FTP-Server

WinInet bietet die Möglichkeit, Verzeichnisse auf einem FTP-Server zu erstellen und zu entfernen, auf dem die Anwendung über die erforderlichen Berechtigungen verfügt. Wenn sich die Anwendung bei einem Server mit einem bestimmten Benutzernamen und einem Kennwort anmelden muss, können die Werte beim Erstellen des FTP-Sitzungs Handles in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet werden.

Die [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) -Funktion nimmt ein gültiges FTP-Sitzungs Handle und eine auf **null** endenden Zeichenfolge, die entweder einen voll qualifizierten Pfad oder einen Namen relativ zum aktuellen Verzeichnis enthält, und erstellt ein Verzeichnis auf dem FTP-Server.

Das folgende Beispiel zeigt zwei separate Aufrufe von [**ftpkreatedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). In beiden Beispielen ist hftpsession das Sitzungs handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion erstellt wird, und das Stammverzeichnis ist das aktuelle Verzeichnis.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

Die Funktion [**ftpremuvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) nimmt ein Sitzungs Handle und eine auf **null** endenden Zeichenfolge, die entweder einen voll qualifizierten Pfad oder einen Namen relativ zum aktuellen Verzeichnis enthält, und entfernt dieses Verzeichnis vom FTP-Server.

Das folgende Beispiel zeigt zwei Beispiel Aufrufe von [**ftpremumuvedirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya). In beiden Aufrufen ist hftpsession das Sitzungs handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion erstellt wird, und das Stammverzeichnis ist das aktuelle Verzeichnis. Das Stammverzeichnis enthält ein Verzeichnis mit dem Namen "Test" und ein Verzeichnis mit dem Namen "example" im Verzeichnis "Test".

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



Im folgenden Beispiel wird ein neues Verzeichnis auf dem FTP-Server erstellt. Der neue Verzeichnisname wird aus dem Bearbeitungsfeld des übergeordneten Dialog Felds übernommen, dessen IDC im *ndirnameid* -Parameter übergeben wird. Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde. Der Quellcode für die displayftpdir-Funktion, die am Ende aufgerufen wird, ist oben aufgeführt.


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



Im folgenden Beispiel wird ein Verzeichnis vom FTP-Server gelöscht. Der Name des zu löschenden Verzeichnisses wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC an den *ndirnameid* -Parameter übergeben wird. Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde. Der Quellcode für die displayftpdir-Funktion, die am Ende aufgerufen wird, ist oben aufgeführt.


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



### <a name="getting-files-on-an-ftp-server"></a>Dateien werden auf einem FTP-Server erhalten.

Es gibt drei Methoden zum Abrufen von Dateien von einem FTP-Server:

-   Verwenden Sie [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Verwenden Sie " [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) " und " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)".
-   Verwenden Sie " [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)".

Weitere Informationen zum Verwenden der [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) -Funktion finden Sie unter [Lesen von Dateien](common-functions.md).

Wenn die URL der Datei verfügbar ist, kann die Anwendung [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) anrufen, um eine Verbindung mit dieser URL herzustellen, und dann mit [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) den Download der Datei steuern. Dies ermöglicht der Anwendung eine strengere Kontrolle über den Download und eignet sich ideal für Situationen, in denen keine anderen Vorgänge auf dem FTP-Server durchgeführt werden müssen. Weitere Informationen zum direkten Zugriff auf Ressourcen finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md).

Wenn die Anwendung ein FTP-Sitzungs Handle für den Server mit [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)eingerichtet hat, kann die Anwendung [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) mit dem vorhandenen Dateinamen und mit einem neuen Namen für die lokal gespeicherte Datei abrufen. Die Anwendung kann dann die Datei mit " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " herunterladen. Dies ermöglicht es der Anwendung, den Download zu verkürzen und die Verbindung mit dem FTP-Server aufrecht zu erhalten, sodass weitere Befehle ausgeführt werden können.

Wenn die Anwendung keine strenge Kontrolle über den Download benötigt, kann die Anwendung [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) mit dem FTP-Sitzungs handle, dem Remote Dateinamen und dem lokalen Dateinamen verwenden, um die Datei abzurufen. [**Ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) führt sämtliche Buchhaltungs-und Verwaltungsaufwand für das Lesen einer Datei von einem FTP-Server durch und speichert Sie lokal.

Das folgende Beispiel ruft eine Datei von einem FTP-Server ab und speichert Sie lokal. Der Name der Datei auf dem FTP-Server wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC im *nftpfileameid* -Parameter übergeben wird, und der lokale Name, unter dem die Datei gespeichert wird, wird aus dem Bearbeitungsfeld entnommen, dessen IDC im *nlocalfileameid* -Parameter übergeben wird. Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.


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

-   Verwenden Sie [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) mit [**internetschreibdatei**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).
-   Verwenden Sie [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).

Eine Anwendung, die Daten an einen FTP-Server senden muss, aber nicht über eine lokale Datei, die alle Daten enthält, sollte [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) verwenden, um eine Datei auf dem FTP-Server zu erstellen und zu öffnen. Die Anwendung kann dann [**internetschreibdatei**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) verwenden, um die Informationen in die Datei hochzuladen.

Wenn die Datei bereits lokal vorhanden ist, kann die Anwendung [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) verwenden, um die Datei auf den FTP-Server hochzuladen. [**Ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) führt den gesamten mehr Aufwand für das Hochladen einer lokalen Datei auf einen Remote-FTP-Server aus.

Im folgenden Beispiel wird eine lokale Datei auf den FTP-Server kopiert. Der lokale Name der Datei wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC im *nlocalfileameid* -Parameter übergeben wird, und der Name, unter dem die Datei auf dem FTP-Server gespeichert wird, wird aus dem Bearbeitungsfeld entnommen, dessen IDC im *nftpfileameid* -Parameter übergeben wird. Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde.


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

Um eine Datei von einem FTP-Server zu löschen, verwenden Sie die [**ftpdeletefile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) -Funktion. Die aufrufende Anwendung muss über die erforderlichen Berechtigungen zum Löschen einer Datei vom FTP-Server verfügen.

Im folgenden Beispiel wird eine Datei vom FTP-Server gelöscht. Der Name der zu löschenden Datei wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC int dem *nftpfileameid* -Parameter übergeben wird. Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde. Da diese Funktion keine Datei Auflistungen oder Verzeichnis Anzeige aktualisiert, sollte der aufrufenden Prozess nach erfolgreichem löschen Vorgehen.


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

Dateien und Verzeichnisse auf einem FTP-Server können mithilfe der [**ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) -Funktion umbenannt werden. [**Ftprenamefile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) akzeptiert zwei **null**-terminierte Zeichen folgen, die relativ zum aktuellen Verzeichnis entweder teilweise oder voll qualifizierte Namen enthalten. Die-Funktion ändert den Namen der von der ersten Zeichenfolge bezeichneten Datei in den von der zweiten Zeichenfolge bezeichneten Namen.

Im folgenden Beispiel wird eine Datei oder ein Verzeichnis auf dem FTP-Server umbenannt. Der aktuelle Name der Datei oder des Verzeichnisses wird aus dem Bearbeitungsfeld im übergeordneten Dialogfeld übernommen, dessen IDC im *noldfileameid* -Parameter übergeben wird, und der neue Name wird aus dem Bearbeitungsfeld übernommen, dessen IDC im *nnewfilename ameid* -Parameter übergeben wird. Das *hconnection* -Handle wurde von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt, nachdem eine FTP-Sitzung eingerichtet wurde. Da diese Funktion keine Datei Auflistungen oder Verzeichnis Anzeige aktualisiert, sollte der aufrufenden Prozess bei erfolgreicher Umbenennung Vorgehen.


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
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 