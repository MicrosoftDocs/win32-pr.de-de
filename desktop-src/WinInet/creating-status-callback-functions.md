---
title: Erstellen von Status Rückruf Funktionen
description: In diesem Tutorial wird beschrieben, wie Sie eine Status Rückruffunktion erstellen, die zum Überwachen des Status einer Internet Anforderung verwendet wird.
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106339305"
---
# <a name="creating-status-callback-functions"></a>Erstellen von Status Rückruf Funktionen

In diesem Tutorial wird beschrieben, wie Sie eine Status Rückruffunktion erstellen, die zum Überwachen des Status einer Internet Anforderung verwendet wird.

Status Rückruf Funktionen empfangen Status Rückrufe für alle Internet Anforderungen, die aus einer beliebigen Wininet-Funktion stammen, der ein Kontextwert ungleich NULL weitergegeben wurde.


Die folgenden Schritte sind erforderlich, um eine Status Rückruffunktion zu erstellen:

1.  [Hiermit wird der Kontextwert definiert.](#defining-the-context-value)
2.  [Erstellen Sie die Status Rückruffunktion.](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a>Definieren des Kontext Werts

Der Kontextwert kann ein beliebiger ganzzahliger Wert ohne Vorzeichen sein. Im Idealfall sollte der Kontextwert feststellen, welche Anforderung gerade abgeschlossen wurde, und den Speicherort der zugeordneten Ressourcen bei Bedarf ermitteln.

Eine der nützlichsten Möglichkeiten, den Kontextwert zu verwenden, besteht darin, die Adresse einer Struktur zu übergeben und in ein **DWORD- \_ ptr** umzuwandeln. Die-Struktur kann zum Speichern von Informationen über die Anforderung verwendet werden, damit diese an die Status Rückruffunktion übermittelt werden.

Die folgende Struktur ist ein Beispiel für einen möglichen Kontextwert. Die Member der Struktur werden mit der [**Internet OpenURL**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion ausgewählt.


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



In diesem Beispiel hätte die Status Rückruffunktion Zugriff auf das Fenster Handle, das es Ihnen ermöglicht, eine Benutzeroberfläche anzuzeigen. Das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellte [**HINTERNET**](appendix-a-hinternet-handles.md) Handle kann an eine andere Funktion übergeben werden, die die Ressource herunterladen kann, sowie ein Zeichen Array, das zum Übergeben von Informationen über die Anforderung verwendet werden kann.

Die Elemente der Struktur können so geändert werden, dass Sie den Anforderungen einer bestimmten Anwendung entsprechen. Deshalb ist dieses Beispiel nicht eingeschränkt.

### <a name="creating-the-status-callback-function"></a>Erstellen der Status Rückruffunktion

Die Status Rückruffunktion muss das Format " [*internetstatuscallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)" aufweisen. Gehen Sie dazu wie folgt vor:

1.  Schreiben Sie eine Funktionsdeklaration für die Status Rückruffunktion.

    Das folgende Beispiel zeigt eine Beispiel Deklaration.

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  Legen Sie fest, welche Aktion die Status Rückruffunktion durchführt. Bei Anwendungen, die asynchrone Aufrufe durchführen, muss die Status Rückruffunktion den Complete-Wert der Internet \_ Status \_ Anforderung verarbeiten, der \_ angibt, dass eine asynchrone Anforderung beendet wurde. Die Status Rückruffunktion kann auch verwendet werden, um den Fortschritt einer Internet Anforderung zu verfolgen.

    Im Allgemeinen funktioniert es am besten, wenn eine Switch-Anweisung mit *dwinternetstatus* als switchwert und die Statuswerte für die Case-Anweisungen verwendet werden. Abhängig von den Funktionstypen, die von der Anwendung aufgerufen werden, können Sie einige der Statuswerte ignorieren. Eine Definition der verschiedenen Statuswerte finden Sie in der Liste unter dem *dwinternetstatus* -Parameter von [*internetstatuscallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).

    Die folgende Switch-Anweisung ist ein Beispiel für das Behandeln von Status Rückrufen.

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  Erstellen Sie den Code, um die Statuswerte zu verarbeiten.

    Der Code zum Verarbeiten der einzelnen Statuswerte hängt stark von der vorgesehenen Verwendung der Status Rückruffunktion ab. Bei Anwendungen, die nur den Status einer Anforderung nachverfolgen, benötigen Sie möglicherweise nur eine Zeichenfolge in ein Listenfeld. Für asynchrone Vorgänge muss der Code einige der im Rückruf zurückgegebenen Daten verarbeiten.

    Die folgende Status Rückruffunktion verwendet eine Switch-Funktion, um den Statuswert zu bestimmen, und erstellt eine Zeichenfolge, die den Namen des Status Werts und die vorherige Funktion mit dem Namen enthält, die im szmemo-Member der Anforderungs \_ Kontext Struktur gespeichert wird.

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  Verwenden Sie die [**internetsetstatuscallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) -Funktion, um die Status Rückruffunktion für das [**hinternethandle**](appendix-a-hinternet-handles.md) festzulegen, für das Sie Status Rückrufe empfangen möchten.

    Im folgenden Beispiel wird veranschaulicht, wie eine Status Rückruffunktion festgelegt wird.

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Status Rückruf Funktionen](creating-status-callback-functions.md)
</dt> <dt>

[**Internetsetstatus Callback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[*Internetstatus Rückruf*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 