---
title: HTTP-Sitzungen
description: Der Zugriff auf die Ressourcen auf dem www erfolgt über http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101866"
---
# <a name="http-sessions"></a>HTTP-Sitzungen

WinInet ermöglicht Ihnen den Zugriff auf Ressourcen auf dem World Wide Web (www). Der Zugriff auf diese Ressourcen erfolgt direkt über [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (Weitere Informationen finden Sie unter Direktes [Aufrufen von URLs](handling-uniform-resource-locators.md)).

Der Zugriff auf die Ressourcen auf dem www erfolgt über http. Die HTTP-Funktionen verarbeiten die zugrunde liegenden Protokolle und ermöglichen Ihrer Anwendung den Zugriff auf Informationen über das www. Wenn das HTTP-Protokoll weiterentwickelt wird, werden die zugrunde liegenden Protokolle aktualisiert, um das Funktionsverhalten aufrechtzuerhalten.

Das folgende Diagramm zeigt die Beziehungen der Funktionen, die mit dem HTTP-Protokoll verwendet werden. Die schattierten Felder stellen Funktionen dar, die [**hinternethandles**](appendix-a-hinternet-handles.md) zurückgeben, während die einfachen Felder Funktionen darstellen, die das **hinternethandle** verwenden, das von der Funktion erstellt wurde, von der Sie abhängig sind.

![für http verwendete WinInet-Funktionen](images/ax-wnt05.png)

Weitere Informationen finden Sie unter [HINTERNET Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-to-access-the-www"></a>Verwenden der WinInet-Funktionen für den Zugriff auf das www

-   [Initiieren einer Verbindung mit dem www](#initiating-a-connection-to-the-www)
-   [Öffnen einer Anforderung](#opening-a-request)
-   [Anforderungs Header werden hinzugefügt](#adding-request-headers)
-   [Senden einer Anforderung](#sending-a-request)
-   [Veröffentlichen von Daten auf dem Server](#posting-data-to-the-server)
-   [Informationen zu einer Anforderung erhalten](#getting-information-about-a-request)
-   [Herunterladen von Ressourcen aus dem www](#downloading-resources-from-the-www)

Die folgenden Funktionen werden während der HTTP-Sitzungen verwendet, um auf das www zuzugreifen.



| Funktion                                               | BESCHREIBUNG                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Httpadressquestheaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | Fügt dem HTTP-Anforderungs handle HTTP-Anforderungs Header hinzu. Diese Funktion erfordert ein Handle, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstellt wurde.                                                 |
| [**Httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | Öffnet ein HTTP-Anforderungs handle. Diese Funktion erfordert ein Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde.                                                                         |
| [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | Fragt Informationen über eine HTTP-Anforderung ab. Diese Funktion erfordert ein Handle, das von der [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion oder der [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion erstellt wird. |
| [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | Sendet die angegebene HTTP-Anforderung an den HTTP-Server. Diese Funktion erfordert ein Handle, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstellt wurde.                                                  |
| [**Internetzterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | Zeigt vordefinierte Dialogfelder für häufige Internet Fehlerbedingungen an. Diese Funktion erfordert das Handle, das im-Befehl von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)verwendet wird.                     |



 

### <a name="initiating-a-connection-to-the-www"></a>Initiieren einer Verbindung mit dem www

Zum Starten einer Verbindung mit dem www muss die Anwendung die [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion für das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)zurückgegebene Stamm- [**HINTERNET**](appendix-a-hinternet-handles.md) anrufen. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) muss eine HTTP-Sitzung einrichten, indem der \_ http-Diensttyp "Internet Dienst" deklariert wird \_ . Weitere Informationen zur Verwendung von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)finden Sie unter [Verwenden von InternetConnect](enabling-internet-functionality.md).

### <a name="opening-a-request"></a>Öffnen einer Anforderung

Die [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Funktion öffnet eine HTTP-Anforderung und gibt ein [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle zurück, das von den anderen HTTP-Funktionen verwendet werden kann. Anders als bei den anderen geöffneten Funktionen (z. b. [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)) sendet [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) die Anforderung nicht an das Internet, wenn aufgerufen wird. Die [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) -Funktion sendet die Anforderung und stellt eine Verbindung über das Netzwerk her.

[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) nimmt ein HTTP-Sitzungs handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, und ein HTTP-Verb, einen Objektnamen, eine Versions Zeichenfolge, einen referenrer, accept-Typen, Flags und einen Kontextwert

Das HTTP-Verb ist eine Zeichenfolge, die in der Anforderung verwendet werden soll. Allgemeine HTTP-Verben, die in Anforderungen verwendet werden, sind Get, Put und Post. Wenn dieser Wert auf **null** festgelegt ist, verwendet [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) den Standardwert Get.

Der Objektname ist eine Zeichenfolge, die den Namen des angegebenen Zielobjekts des HTTP-Verbs enthält. Dies ist im Allgemeinen ein Dateiname, ein ausführbares Modul oder ein suchspezifizierer. Wenn der angegebene Objektname eine leere Zeichenfolge ist, sucht [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) nach der Standardseite.

Die Versions Zeichenfolge sollte die HTTP-Version enthalten. Wenn dieser Parameter **null** ist, verwendet die Funktion "" http/1.1 "".

Der Verweiser gibt die Adresse des Dokuments an, aus dem der Objektname abgerufen wurde. Wenn dieser Parameter **null** ist, wird kein Verweiser angegeben.

Die **null**-terminierte Zeichenfolge, die die Accept-Typen enthält, gibt die von der Anwendung akzeptierten Inhaltstypen an. Durch Festlegen dieses Parameters auf **null** wird angegeben, dass von der Anwendung keine Inhaltstypen akzeptiert werden. Wenn eine leere Zeichenfolge angegeben wird, gibt die Anwendung an, dass nur Dokumente vom Typ "Text/" akzeptiert werden \* . Der Wert "" Text/ \* "" zeigt nur-Text-Dokumente an – nicht Bilder oder andere Binärdateien.

Die Flagwerte Steuern Zwischenspeicherung, Cookies und Sicherheitsprobleme. Legen Sie für Microsoft Network (MSN), NTLM und andere Authentifizierungs Typen das Flag [Internet \_ Flag \_ Keep \_ Connection](api-flags.md) fest.

Wenn das [Internet \_ Flag \_ Async](api-flags.md) -Flag im Aufrufen von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)festgelegt wurde, sollte für den ordnungsgemäßen asynchronen Vorgang ein Kontextwert ungleich NULL festgelegt werden.

Das folgende Beispiel ist ein Beispiel für [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>Anforderungs Header werden hinzugefügt

Die [**httpadressquestheaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) -Funktion ermöglicht Anwendungen das Hinzufügen eines oder mehrerer Anforderungs Header zur ursprünglichen Anforderung. Diese Funktion ermöglicht es einer Anwendung, zusätzliche Header mit freiem Format an das HTTP-Anforderungs handle anzufügen. Es ist für die Verwendung durch anspruchsvolle Anwendungen vorgesehen, die eine genaue Kontrolle über die an den HTTP-Server gesendete Anforderung erfordern.

[**Httpadressquestheaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) benötigt ein von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstelltes HTTP-Anforderungs handle, eine Zeichenfolge, die die Header, die Länge der Header und Modifizierer enthält.

### <a name="sending-a-request"></a>Senden einer Anforderung

[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) stellt eine Verbindung mit dem Internet her und sendet die Anforderung an den angegebenen Standort. Diese Funktion erfordert ein [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)erstellt wurde. Mit [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) können auch zusätzliche Header oder optionale Informationen gesendet werden. Die optionalen Informationen werden im Allgemeinen für Vorgänge verwendet, die Informationen auf dem Server schreiben, z. b. Put und Post.

Nachdem [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) die Anforderung gesendet hat, kann die Anwendung die Funktionen [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) für das [**hinternethandle**](appendix-a-hinternet-handles.md) verwenden, das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wurde, um die Ressourcen des Servers herunterzuladen.

### <a name="posting-data-to-the-server"></a>Veröffentlichen von Daten auf dem Server

Zum Bereitstellen von Daten auf einem Server muss das HTTP-Verb im [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) -Befehl entweder Post oder Put lauten. Die Adresse des Puffers, der die Post-Daten enthält, sollte dann in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)an den *lpoptional* -Parameter übergeben werden. Der Parameter " *dwoptionallength* " sollte auf die Größe der Daten festgelegt werden.

Sie können auch die [**internetwrite File**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) -Funktion verwenden, um Daten in einem [**hinternethandle**](appendix-a-hinternet-handles.md) zu veröffentlichen, das mit [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)gesendet wird.

### <a name="getting-information-about-a-request"></a>Informationen zu einer Anforderung erhalten

[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ermöglicht einer Anwendung das Abrufen von Informationen zu einer HTTP-Anforderung. Die Funktion erfordert ein [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) oder [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), einem Wert auf Informationsebene und einer Pufferlänge erstellt wurde. [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) akzeptiert auch einen Puffer, in dem die Informationen gespeichert sind, sowie einen NULL basierten Header Index, der mehrere Header mit demselben Namen auflistet.

### <a name="downloading-resources-from-the-www"></a>Herunterladen von Ressourcen aus dem www

Nachdem eine Anforderung mit [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) geöffnet und mit [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)an den Server gesendet wurde, kann die Anwendung die Funktionen " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)", " [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)" und " [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) " verwenden, um die Ressource vom HTTP-Server herunterzuladen.

Im folgenden Beispiel wird eine Ressource heruntergeladen. Die-Funktion akzeptiert das Handle für das aktuelle Fenster, die ID eines Bearbeitungs Felds und ein [**hinternethandle**](appendix-a-hinternet-handles.md) , das von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt und von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)gesendet wurde. Er verwendet [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) , um die Größe der Ressource zu ermitteln, und lädt Sie dann mithilfe von " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)" herunter. Der Inhalt wird dann im Bearbeitungsfeld angezeigt.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
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

    return TRUE;
}
```



> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 