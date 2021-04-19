---
title: Abrufen von HTTP-Headern
description: In diesem Tutorial wird beschrieben, wie Header Informationen aus HTTP-Anforderungen abgerufen werden.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b31043940b8c2127d1cfa1696d2821641d0784
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340731"
---
# <a name="retrieving-http-headers"></a>Abrufen von HTTP-Headern

In diesem Tutorial wird beschrieben, wie Header Informationen aus HTTP-Anforderungen abgerufen werden.

## <a name="implementation-steps"></a>Implementierungs Schritte

Die Header Informationen können auf zwei Arten abgerufen werden:

-   Verwenden Sie eine der [**abfrageinfoflag**](query-info-flags.md) -Konstanten, die dem HTTP-Header zugeordnet sind, den Ihre Anwendung benötigt.
-   Verwenden Sie das \_ \_ benutzerdefinierte Attribut Flag für die HTTP-Abfrage, und übergeben Sie den Namen des HTTP-Headers.

Das Verwenden der dem HTTP-Header zugeordneten Konstante, die Ihre Anwendung benötigt, ist intern schneller, aber es können HTTP-Header vorhanden sein, denen keine Konstante zugeordnet ist. In diesen Fällen ist die-Methode verfügbar, die das \_ \_ benutzerdefinierte Flag für die HTTP-Abfrage verwendet.

Beide Methoden verwenden die [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Funktion. [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) übernimmt den [**HINTERNET**](appendix-a-hinternet-handles.md) -handle, für den die HTTP-Anforderung erfolgt ist, ein Attribut, einen Puffer, einen DWORD-Wert, der die Puffergröße enthält, und einen Indexwert. Ein Modifizierer kann auch dem an [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) übergebenen Attribut hinzugefügt werden, um anzugeben, in welchem Format die Daten zurückgegeben werden sollen.

### <a name="retrieving-headers-using-a-constant"></a>Abrufen von Headern mit einer Konstanten

Führen Sie die folgenden Schritte aus, um mithilfe der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Funktion einen HTTP-Header mit einer Konstanten abzurufen:

1.  [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mit einer Konstanten aus der [**Attribut**](query-info-flags.md) Liste, einem **null** -Puffer und der Variablen, die die Puffergröße enthält, auf 0 (null) festgelegt. Außerdem können Sie, wenn die Anwendung die Daten in einem bestimmten Format benötigt, eine Konstante aus der Liste [**Modifizierer**](query-info-flags.md) hinzufügen.
2.  Wenn der angeforderte HTTP-Header vorhanden ist, sollte der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl einen Fehler erzeugen, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) sollte fehlerhaften Puffer zurückgeben \_ \_ , und die für den *lpdwbufferlength* -Parameter übergebenen Variable sollte auf die erforderliche Anzahl von Bytes festgelegt werden.
3.  Weisen Sie einen Puffer mit der Anzahl der erforderlichen Bytes zu.
4.  Wiederholen Sie den [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)-Rückruf.

Das folgende Beispiel veranschaulicht einen [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl mithilfe der CRLF-Konstante für den HTTP- \_ Abfrage \_ \_ rohheader \_ , bei der es sich um einen speziellen Wert handelt, der alle zurückgegebenen HTTP-Header anfordert.


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a>Abrufen von Headern mithilfe \_ der \_ benutzerdefinierten HTTP-Abfrage

Führen Sie die folgenden Schritte aus, um mithilfe der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Funktion einen HTTP-Header mit \_ \_ benutzerdefiniertem HTTP-Abfrage abzurufen:

1.  Weisen Sie einen Puffer zu, der groß genug ist, um den Zeichen folgen Namen des HTTP-Headers aufzunehmen.
2.  Schreiben Sie den Zeichen folgen Namen des HTTP-Headers in den Puffer.
3.  Nennen Sie [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mit \_ der \_ benutzerdefinierten HTTP-Abfrage, dem Puffer, der den Zeichen folgen Namen des HTTP-Headers enthält, und der Variablen, die die Puffergröße enthält. Außerdem können Sie, wenn die Anwendung die Daten in einem bestimmten Format benötigt, eine Konstante aus der Liste [**Modifizierer**](query-info-flags.md) hinzufügen.
4.  Wenn der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl fehlschlägt und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fehlerhaften Puffer zurückgibt \_ \_ , ordnen Sie einen Puffer mit der erforderlichen Anzahl von Bytes neu zu.
5.  Schreiben Sie den Zeichen folgen Namen des HTTP-Headers erneut in den Puffer.
6.  Wiederholen Sie den [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)-Rückruf.

Das folgende Beispiel veranschaulicht einen [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl, indem die \_ \_ benutzerdefinierte HTTP-Abfrage-Konstante verwendet wird, um den Content-Type-HTTP-Header anzufordern.


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 