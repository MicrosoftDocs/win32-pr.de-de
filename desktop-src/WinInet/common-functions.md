---
title: Allgemeine Funktionen (Windows Internet)
description: Bei den verschiedenen Internet Protokollen (z. b. FTP und http) werden mehrere der gleichen WinInet-Funktionen verwendet, um Informationen im Internet zu verarbeiten.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338513"
---
# <a name="common-functions-windows-internet"></a>Allgemeine Funktionen (Windows Internet)

Bei den verschiedenen Internet Protokollen (z. b. FTP und http) werden mehrere der gleichen WinInet-Funktionen verwendet, um Informationen im Internet zu verarbeiten. Diese gängigen Funktionen behandeln Ihre Aufgaben auf konsistente Weise, unabhängig vom jeweiligen Protokoll, auf das Sie angewendet werden. Anwendungen können diese Funktionen verwenden, um allgemeine Funktionen zu erstellen, die Tasks über die verschiedenen Protokolle hinweg verarbeiten (z. b. das Lesen von Dateien für FTP und http).

Die allgemeinen Funktionen behandeln die folgenden Aufgaben:

-   Herunterladen von Ressourcen aus dem Internet ([**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)und [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Einrichten von asynchronen Vorgängen ([**internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Anzeigen und Ändern von Optionen ([**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Alle Typen von [**hinternethandles**](appendix-a-hinternet-handles.md) ([**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)) werden geschlossen.
-   Platzieren und Entfernen von Sperren für Ressourcen ([**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) und [**internetunlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).

## <a name="using-common-functions"></a>Verwenden von gängigen Funktionen

In der folgenden Tabelle sind die allgemeinen Funktionen aufgeführt, die in den WinInet-Funktionen enthalten sind. Die allgemeinen Funktionen können für verschiedene Typen von [**hinternethandles**](appendix-a-hinternet-handles.md) verwendet werden oder können bei verschiedenen Sitzungs Typen verwendet werden.



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Setzt die Dateienumeration oder-Suche fort. Erfordert ein Handle, das von der [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)-Funktion oder der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion erstellt wird.                                                                            |
| [**Internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Ermöglicht es dem Benutzer, eine Sperre für die verwendete Datei zu platzieren. Diese Funktion erfordert ein Handle, das von der [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-, der [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)-oder der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion zurückgegeben wird. |
| [**Internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Ruft die Menge der verfügbaren Daten ab. Erfordert ein Handle, das von der [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-Funktion oder der [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion erstellt wird.                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Ruft die Einstellung einer Internet Option ab.                                                                                                                                                                                                            |
| [**Internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Liest URL-Daten. Erfordert ein Handle, das von der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)-, [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion erstellt wird.                                                                |
| [**Internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Legt die Position für den nächsten Lesevorgang in einer Datei fest. Erfordert ein Handle, das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (nur auf einer HTTP-URL) erstellt wird, oder ein Handle, das von [**httpoperrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) mithilfe des HTTP-Verbs Get erstellt wurde.                 |
| [**Internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Legt eine Internet Option fest.                                                                                                                                                                                                                                |
| [**Internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Legt eine Rückruffunktion fest, die Statusinformationen empfängt. Weist dem vorgesehenen [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle und allen davon abgeleiteten Handles eine Rückruffunktion zu.                                                      |
| [**Internetunlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Entsperrt eine Datei, die mithilfe der [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) -Funktion gesperrt wurde.                                                                                                                                           |



 

Das Lesen von Dateien, das Suchen der nächsten Datei, das Bearbeiten von Optionen und das Einrichten von asynchronen Vorgängen wird häufig von den Funktionen verwendet, die verschiedene Protokolle und [**HINTERNET**](appendix-a-hinternet-handles.md) -handle-Typen unterstützen.

### <a name="reading-files"></a>Lesen von Dateien

Die [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) -Funktion wird zum Herunterladen von Ressourcen von einem [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet, das von der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)-, [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)-oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion zurückgegeben wird.

[**Internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) akzeptiert eine void-Zeiger Variable, die die Adresse eines Puffers enthält, und einen Zeiger auf eine Variable, die die Länge des Puffers enthält. Die-Funktion gibt die Daten im Puffer und die Menge der Daten zurück, die in den Puffer heruntergeladen werden.

Die WinInet-Funktionen stellen zwei Verfahren zum Herunterladen einer vollständigen Ressource bereit:

-   Die [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) -Funktion.
-   Die Rückgabewerte von " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)".

[**Internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) übernimmt das [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde (nachdem [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) für das Handle aufgerufen wurde), und gibt die Anzahl der verfügbaren Bytes zurück. Die Anwendung muss einen Puffer zuordnen, der der Anzahl der verfügbaren Bytes entspricht, plus 1 für das abschließende **null** -Zeichen, und diesen Puffer mit [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)verwenden. Diese Methode funktioniert nicht immer, weil [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) die Dateigröße überprüft, die im Header und nicht in der eigentlichen Datei aufgeführt ist. Die Informationen in der Header Datei sind möglicherweise veraltet, oder die Header Datei fehlt, da Sie derzeit nicht unter allen Standards erforderlich ist.

Im folgenden Beispiel wird der Inhalt der Ressource gelesen, auf die über das hresource-handle zugegriffen wird, und wird im Bearbeitungsfeld angezeigt, das von intctrlid angegeben wird.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



" [**Internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " gibt NULL Bytes zurück und wird erfolgreich abgeschlossen, wenn alle verfügbaren Daten gelesen wurden. Dadurch kann eine Anwendung " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " in einer Schleife verwenden, um die Daten herunterzuladen und zu beenden, wenn NULL Bytes gelesen und erfolgreich abgeschlossen werden.

Das folgende Beispiel liest die Ressource aus dem Internet und zeigt die Ressource im Bearbeitungsfeld an, das von intctrlid angegeben wird. Das [**HINTERNET**](appendix-a-hinternet-handles.md) handle, HINTERNET, wurde von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**ftpopumfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) zurückgegeben (nach dem Senden durch [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a>Suchen der nächsten Datei

Die Funktion " [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) " wird verwendet, um die nächste Datei in einer Dateisuche mithilfe der Suchparameter und des [**hinternethandles**](appendix-a-hinternet-handles.md) aus [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)oder [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)zu suchen.

Um eine Dateisuche abzuschließen, wenden Sie weiterhin [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) mithilfe des [**hinternethandles**](appendix-a-hinternet-handles.md) , das von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)zurückgegeben wird, oder [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) an, bis die Funktion mit der erweiterten Fehlermeldung [ \_ nicht \_ mehr \_ Dateien](wininet-errors.md)fehlschlägt. Um die erweiterten Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.

Im folgenden Beispiel wird der Inhalt eines FTP-Verzeichnisses im Listenfeld angezeigt, das von lstdirectory angegeben wird. Das [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hconnect, ist ein Handle, das von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion zurückgegeben wird, nachdem eine FTP-Sitzung eingerichtet wurde.


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a>Bearbeiten von Optionen

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) werden verwendet, um die WinInet-Optionen zu bearbeiten.

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) akzeptiert eine Variable, die die festzulegende Option angibt, einen Puffer, der die Options Einstellung enthalten soll, und einen Zeiger, der die Adresse der Variablen enthält, die die Länge des Puffers enthält.

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) akzeptiert eine Variable, die die abzurufende Option, einen Puffer zum Speichern der Options Einstellung und einen Zeiger mit der Adresse der Variablen angibt, die die Länge des Puffers enthält.

### <a name="setting-up-asynchronous-operations"></a>Einrichten von asynchronen Vorgängen

Die WinInet-Funktionen werden standardmäßig synchron ausgeführt. Eine Anwendung kann einen asynchronen Vorgang anfordern, indem das [Internet \_ Flag \_ Async](api-flags.md) -Flag im Aufrufen der [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion festgelegt wird. Alle zukünftigen Aufrufe von Handles, die von dem von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) zurückgegebenen handle abgeleitet werden, werden asynchron durchgeführt.

Der Grund für den asynchronen und synchronen Betrieb besteht darin, dass eine Single Thread Anwendung die Auslastung der CPU maximieren kann, ohne dass auf den Abschluss der Netzwerk-e/a gewartet werden muss. Daher kann der Vorgang abhängig von der Anforderung synchron oder asynchron ausgeführt werden. Die Anwendung sollte den Rückgabecode überprüfen. Wenn eine Funktion " **false** " oder " **null**" zurückgibt und " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " eine ausstehende Fehler-e/a zurückgibt \_ \_ , wird die Anforderung asynchron durchgeführt, und die Anwendung wird mit dem Internet \_ Status \_ Request Complete aufgerufen, \_ Wenn die Funktion abgeschlossen ist.

Um mit dem asynchronen Vorgang zu beginnen, muss die Anwendung das [Internet \_ Flag \_ Async](api-flags.md) -Flag im Aufrufen von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)festlegen. Die Anwendung muss dann mithilfe von [**internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)eine gültige Rückruffunktion registrieren.

Nachdem eine Rückruffunktion für ein Handle registriert wurde, können alle Vorgänge für dieses Handle Status Hinweise generieren, vorausgesetzt, dass der beim Erstellen des Handles angegebene Kontextwert nicht 0 (null) war. Das Bereitstellen eines NULL-Kontext Werts erzwingt, dass ein Vorgang synchron ausgeführt wird, obwohl in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)das [Internet Kennzeichen \_ \_ Async](api-flags.md) angegeben wurde.

Status Hinweise geben der Anwendung Feedback zum Fortschritt von Netzwerk Vorgängen, z. b. zum Auflösen eines Host namens, zum Herstellen einer Verbindung mit einem Server und zum Empfangen von Daten. Für ein Handle können drei Status Hinweise zum besonderen Zweck erstellt werden:

-   \_ \_ \_ Das Schließen des Internet Status Handles ist die letzte Status Anzeige, die für ein Handle erfolgt.
-   \_ \_ Das erstellte Internet Status handle zeigt an, \_ wann das Handle erstmalig erstellt wird.
-   Der Internet \_ Status \_ Request \_ Complete gibt an, dass ein asynchroner Vorgang abgeschlossen wurde.

Die Anwendung muss die asynchrone [**Internet \_ \_ Ergebnis**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) Struktur überprüfen, um zu bestimmen, ob der Vorgang erfolgreich war oder fehlgeschlagen ist \_ \_ \_ .

Das folgende Beispiel zeigt ein Beispiel für eine Rückruffunktion und einen Aufrufen von [**internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) , um die Funktion als Rückruffunktion zu registrieren.


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a>Schließen von HINTERNET-Handles

Alle [**HINTERNET**](appendix-a-hinternet-handles.md) -Handles können mithilfe der [**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) -Funktion geschlossen werden. Client Anwendungen müssen alle **hinternethandles** schließen, die vom **HINTERNET** -handle abgeleitet sind, das Sie schließen möchten, bevor Sie [**internetclosehandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) für das Handle aufrufen.

Im folgenden Beispiel wird die Handle-Hierarchie veranschaulicht.


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a>Sperren und Entsperren von Ressourcen

Mit der [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) -Funktion kann eine Anwendung sicherstellen, dass die zwischengespeicherte Ressource, die dem an Sie über gebenden [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle zugeordnet ist, nicht aus dem Cache verschwindet. Wenn ein anderer Download versucht, einen Commit für eine Ressource durchzusetzen, die dieselbe URL wie die gesperrte Datei hat, vermeidet der Cache das Entfernen der Datei durch einen sicheren Löschvorgang. Nachdem die Anwendung die [**internetunlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) -Funktion aufgerufen hat, erhält der Cache die Berechtigung zum Löschen der Datei.

Wenn das Flag " [Internet \_ Flag \_ No \_ Cache \_ Write](api-flags.md) " oder " [Internet \_ Flag \_ Not \_ Cache](api-flags.md) " festgelegt wurde, erstellt [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) eine temporäre Datei mit der Erweiterung tmp, es sei denn, das Handle ist mit einer HTTPS-Ressource verbunden. Wenn die Funktion auf eine HTTPS-Ressource zugreift und das Internet \_ Flag \_ kein Cache \_ \_ Schreibvorgang (oder Internet \_ Flag nicht \_ \_ Cache) festgelegt wurde, schlägt [**internetlockrequestfile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fehl.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
