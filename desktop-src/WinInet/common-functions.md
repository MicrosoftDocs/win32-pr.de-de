---
title: Allgemeine Funktionen (Windows Internet)
description: Die verschiedenen Internetprotokolle (z. B. FTP und HTTP) verwenden mehrere der gleichen WinINet-Funktionen, um Informationen im Internet zu verarbeiten.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7b6a68c2633175eca793f48b2180b7212905762ca0f58290436aa17ae9a728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132893"
---
# <a name="common-functions-windows-internet"></a>Allgemeine Funktionen (Windows Internet)

Die verschiedenen Internetprotokolle (z. B. FTP und HTTP) verwenden mehrere der gleichen WinINet-Funktionen, um Informationen im Internet zu verarbeiten. Diese allgemeinen Funktionen verarbeiten ihre Aufgaben konsistent, unabhängig vom jeweiligen Protokoll, auf das sie angewendet werden. Anwendungen können diese Funktionen verwenden, um allgemeine Funktionen zu erstellen, die Aufgaben über die verschiedenen Protokolle hinweg verarbeiten (z. B. das Lesen von Dateien für FTP und HTTP).

Die allgemeinen Funktionen verarbeiten die folgenden Aufgaben:

-   Herunterladen von Ressourcen aus dem Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)und [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Einrichten asynchroner Vorgänge ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Anzeigen und Ändern von Optionen ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Schließen aller [**HINTERNET-Handles**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).
-   Platzieren und Entfernen von Sperren für Ressourcen ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) und [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).

## <a name="using-common-functions"></a>Verwenden von allgemeinen Funktionen

In der folgenden Tabelle sind die allgemeinen Funktionen aufgeführt, die in den WinINet-Funktionen enthalten sind. Die allgemeinen Funktionen können für verschiedene Typen von [**HINTERNET-Handles**](appendix-a-hinternet-handles.md) oder während verschiedener Sitzungstypen verwendet werden.



| Funktion                                                         | Beschreibung                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Setzt die Dateienumeration oder -suche fort. Erfordert ein Handle, das von der [**FtpFindFirstFile-**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)oder [**InternetOpenUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellt wurde.                                                                            |
| [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Ermöglicht dem Benutzer, eine Sperre für die verwendete Datei zu erstellen. Diese Funktion erfordert ein Handle, das von der [**FtpOpenFile-,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**HttpOpenRequest-**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)oder [**InternetOpenUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) zurückgegeben wird. |
| [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Ruft die verfügbare Datenmenge ab. Erfordert ein handle, das von der [**FtpOpenFile-**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**HttpOpenRequest-Funktion**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde.                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Ruft die Einstellung einer Internetoption ab.                                                                                                                                                                                                            |
| [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Liest URL-Daten. Erfordert ein Handle, das von der [**Funktion InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde.                                                                |
| [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Legt die Position für den nächsten Lese- in einer Datei fest. Erfordert ein handle, das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellt wurde (nur für eine HTTP-URL) oder ein Handle, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) mithilfe des GET HTTP-Verbs erstellt wurde.                 |
| [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Legt eine Internetoption fest.                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Legt eine Rückruffunktion fest, die Statusinformationen empfängt. Weist dem angegebenen [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) und allen davon abgeleiteten Handles eine Rückruffunktion zu.                                                      |
| [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Entsperrt eine Datei, die mithilfe der [**InternetLockRequestFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) gesperrt wurde.                                                                                                                                           |



 

Das Lesen von Dateien, das Suchen der nächsten Datei, das Bearbeiten von Optionen und das Einrichten asynchroner Vorgänge sind für die Funktionen üblich, die verschiedene Protokolle und [**HINTERNET-Handletypen**](appendix-a-hinternet-handles.md) unterstützen.

### <a name="reading-files"></a>Lesen von Dateien

Die [**InternetReadFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) wird verwendet, um Ressourcen aus einem [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) herunterzuladen, das von der [**Funktion InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) zurückgegeben wird.

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) akzeptiert eine void-Zeigervariable, die die Adresse eines Puffers enthält, und einen Zeiger auf eine Variable, die die Länge des Puffers enthält. Die Funktion gibt die Daten im Puffer und die Menge der in den Puffer heruntergeladenen Daten zurück.

Die WinINet-Funktionen bieten zwei Verfahren zum Herunterladen einer gesamten Ressource:

-   Die [**InternetQueryDataAvailable-Funktion.**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)
-   Die Rückgabewerte von [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) verwendet das [**HINTERNET-Handle,**](appendix-a-hinternet-handles.md) das von [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde (nachdem [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) für das Handle aufgerufen wurde) und gibt die Anzahl der verfügbaren Bytes zurück. Die Anwendung sollte einen Puffer zuordnen, der der Anzahl der verfügbaren Bytes entspricht, plus 1 für das abschließende **NULL-Zeichen,** und diesen Puffer mit [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)verwenden. Diese Methode funktioniert nicht immer, da [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) die im Header aufgeführte Dateigröße und nicht die tatsächliche Datei überprüft. Die Informationen in der Headerdatei könnten veraltet sein, oder die Headerdatei könnte fehlen, da sie derzeit nicht unter allen Standards erforderlich ist.

Im folgenden Beispiel wird der Inhalt der Ressource gelesen, auf die vom hResource-Handle zugegriffen wird, und wird im Bearbeitungsfeld angezeigt, das durch intCtrlID angegeben wird.


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



[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) gibt 0 gelesene Bytes zurück und wird erfolgreich abgeschlossen, wenn alle verfügbaren Daten gelesen wurden. Dadurch kann eine Anwendung [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in einer Schleife verwenden, um die Daten herunterzuladen und zu beenden, wenn sie 0 (null) gelesene Bytes zurückgibt und erfolgreich abgeschlossen wird.

Im folgenden Beispiel wird die Ressource aus dem Internet gelesen und im Bearbeitungsfeld angezeigt, das durch intCtrlID angegeben wird. Das [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) hInternet wurde von [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) zurückgegeben (nachdem es von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)gesendet wurde).


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

Die [**InternetFindNextFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) wird verwendet, um die nächste Datei in einer Dateisuche zu suchen, indem die Suchparameter und das [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) von [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)oder [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

Um eine Dateisuche abzuschließen, rufen [**Sie weiterhin InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) mithilfe des von [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)oder [**InternetOpenUrl zurückgegebenen**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**HINTERNET-Handles**](appendix-a-hinternet-handles.md) auf, bis die Funktion mit der erweiterten Fehlermeldung [ERROR NO MORE \_ \_ \_ FILES](wininet-errors.md)fehlschlägt. Rufen Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um die erweiterten Fehlerinformationen abzurufen.

Im folgenden Beispiel wird der Inhalt eines FTP-Verzeichnisses im listenfeld angezeigt, das durch lstDirectory angegeben wird. Das [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) hConnect ist ein Handle, das von der [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) zurückgegeben wird, nachdem eine FTP-Sitzung eingerichtet wurde.


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

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) werden verwendet, um die WinINet-Optionen zu bearbeiten.

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) akzeptiert eine Variable, die die festzulegende Option angibt, einen Puffer für die Optionseinstellung und einen Zeiger, der die Adresse der Variablen enthält, die die Länge des Puffers enthält.

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) akzeptiert eine Variable, die die abzurufende Option angibt, einen Puffer für die Optionseinstellung und einen Zeiger, der die Adresse der Variablen enthält, die die Länge des Puffers enthält.

### <a name="setting-up-asynchronous-operations"></a>Einrichten asynchroner Vorgänge

Standardmäßig werden die WinINet-Funktionen synchron ausgeführt. Eine Anwendung kann einen asynchronen Vorgang anfordern, indem sie das [ \_ \_ ASYNC-Flag INTERNET FLAG](api-flags.md) im Aufruf der [**InternetOpen-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopena) festlegt. Alle zukünftigen Aufrufe an Handles, die von dem von [**InternetOpen zurückgegebenen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) Handle abgeleitet werden, werden asynchron ausgeführt.

Der Grund für asynchrone und synchrone Vorgänge besteht darin, einer Singlethreadanwendung zu ermöglichen, ihre CPU-Auslastung zu maximieren, ohne auf den Abschluss der Netzwerk-E/A warten zu müssen. Daher kann der Vorgang je nach Anforderung synchron oder asynchron abgeschlossen werden. Die Anwendung sollte den Rückgabecode überprüfen. Wenn eine Funktion **FALSE** oder **NULL** zurückgibt und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ERROR \_ IO PENDING zurückgibt, \_ wurde die Anforderung asynchron ausgeführt, und die Anwendung wird mit INTERNET STATUS REQUEST COMPLETE zurückgerufen, \_ wenn die Funktion abgeschlossen \_ \_ wurde.

Um den asynchronen Vorgang zu starten, muss die Anwendung das [ \_ \_ ASYNC-Flag INTERNET FLAG](api-flags.md) in ihrem Aufruf von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)festlegen. Die Anwendung muss dann mithilfe von [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)eine gültige Rückruffunktion registrieren.

Nachdem eine Rückruffunktion für ein Handle registriert wurde, können alle Vorgänge für dieses Handle Statusanzeigen generieren, vorausgesetzt, dass der beim Erstellen des Handles angegebene Kontextwert nicht 0 (null) war. Die Angabe eines Nullkontextwerts erzwingt, dass ein Vorgang synchron abgeschlossen wird, obwohl [INTERNET \_ FLAG \_ ASYNC](api-flags.md) in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)angegeben wurde.

Statusanzeigen geben der Anwendung Feedback zum Fortschritt von Netzwerkvorgängen, z. B. auflösen eines Hostnamens, Herstellen einer Verbindung mit einem Server und Empfangen von Daten. Für ein Handle können drei spezielle Statusanzeigen vorgenommen werden:

-   INTERNET \_ STATUS HANDLE CLOSING ist die letzte \_ \_ Statusanzeige, die für ein Handle vorgenommen wird.
-   INTERNETSTATUS \_ \_ HANDLE CREATED gibt \_ an, wann das Handle anfänglich erstellt wird.
-   INTERNET \_ STATUS REQUEST COMPLETE gibt \_ \_ an, dass ein asynchroner Vorgang abgeschlossen wurde.

Die Anwendung muss die [**INTERNET \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) überprüfen, um zu ermitteln, ob der Vorgang erfolgreich war oder fehlgeschlagen ist, nachdem eine \_ INTERNET STATUS REQUEST \_ \_ COMPLETE-Angabe empfangen wurde.

Das folgende Beispiel zeigt ein Beispiel für eine Rückruffunktion und einen Aufruf von [**InternetSetStatusCallback,**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) um die Funktion als Rückruffunktion zu registrieren.


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

Alle [**HINTERNET-Handles**](appendix-a-hinternet-handles.md) können mithilfe der [**InternetCloseHandle-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) geschlossen werden. Clientanwendungen müssen alle **HINTERNET-Handles** schließen, die von dem **HINTERNET-Handle** abgeleitet sind, das sie schließen möchten, bevor [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) für das Handle aufgerufen wird.

Das folgende Beispiel veranschaulicht die Handlehierarchie.


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

Mit der [**InternetLockRequestFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) kann eine Anwendung sicherstellen, dass die zwischengespeicherte Ressource, die dem an sie übergebenen [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) zugeordnet ist, nicht aus dem Cache verschwindet. Wenn ein anderer Download versucht, eine Ressource mit der gleichen URL wie die gesperrte Datei zu committen, vermeidet der Cache das Entfernen der Datei durch einen sicheren Löschversuch. Nachdem die Anwendung die [**InternetUnlockRequestFile-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) aufruft, erhält der Cache die Berechtigung zum Löschen der Datei.

Wenn das [FLAG INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE](api-flags.md) oder [INTERNET FLAG \_ \_ DONT \_ CACHE](api-flags.md) festgelegt wurde, erstellt [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) eine temporäre Datei mit der Erweiterung TMP, es sei denn, das Handle ist mit einer HTTPS-Ressource verbunden. Wenn die Funktion auf eine HTTPS-Ressource zugreift und INTERNET \_ FLAG NO CACHE WRITE \_ \_ \_ (oder INTERNET FLAG \_ \_ DONT \_ CACHE) festgelegt wurde, schlägt [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fehl.

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 
