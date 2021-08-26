---
title: Abrufen von HTTP-Headern
description: In diesem Tutorial wird beschrieben, wie Headerinformationen aus HTTP-Anforderungen abgerufen werden.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9c1dbae3447d5ae44c8d348394f2dc802ed9d7b4af7d99fde19d0b5d2c3d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955510"
---
# <a name="retrieving-http-headers"></a>Abrufen von HTTP-Headern

In diesem Tutorial wird beschrieben, wie Headerinformationen aus HTTP-Anforderungen abgerufen werden.

## <a name="implementation-steps"></a>Implementierungsschritte

Es gibt zwei Möglichkeiten, die Headerinformationen abzurufen:

-   Verwenden Sie eine der Konstanten des [**Abfrageinformationsflags,**](query-info-flags.md) die dem HTTP-Header zugeordnet sind, den Ihre Anwendung benötigt.
-   Verwenden Sie das ATTRIBUTFlag HTTP QUERY CUSTOM, und übergeben Sie \_ den Namen des \_ HTTP-Headers.

Die Verwendung der Konstanten, die dem HTTP-Header zugeordnet ist, den Ihre Anwendung benötigt, ist intern schneller, aber es können HTTP-Header vorhanden sein, denen keine Konstante zugeordnet ist. In diesen Fällen ist die Methode verfügbar, die das \_ ATTRIBUTFlag HTTP QUERY \_ CUSTOM verwendet.

Beide Methoden verwenden die [**HttpQueryInfo-Funktion.**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) verwendet das [**HINTERNET-Handle,**](appendix-a-hinternet-handles.md) für das die HTTP-Anforderung gestellt wurde, ein Attribut, einen Puffer, einen DWORD-Wert, der die Puffergröße enthält, und einen Indexwert. Dem an [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) übergebenen Attribut kann auch ein Modifizierer hinzugefügt werden, um anzugeben, in welchem Format die Daten zurückgegeben werden sollen.

### <a name="retrieving-headers-using-a-constant"></a>Abrufen von Headern mithilfe einer Konstante

Führen Sie die folgenden Schritte aus, um die [**HttpQueryInfo-Funktion**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) zum Abrufen eines HTTP-Headers mithilfe einer Konstante zu verwenden:

1.  Rufen Sie [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mit einer Konstante aus der [**Liste Attribute,**](query-info-flags.md) einem **NULL-Puffer** und der Variablen auf, die die Puffergröße auf 0 (null) festgelegt hat. Wenn Ihre Anwendung die Daten in einem bestimmten Format benötigt, können Sie außerdem eine Konstante aus der Liste [**Modifizierer**](query-info-flags.md) hinzufügen.
2.  Wenn der angeforderte HTTP-Header vorhanden ist, sollte der Aufruf von [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fehlschlagen, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) sollte ERROR \_ INSUFFICIENT BUFFER \_ zurückgeben, und die für den *lpdwBufferLength-Parameter übergebene* Variable sollte auf die erforderliche Anzahl von Bytes festgelegt werden.
3.  Zuordnen eines Puffers mit der erforderlichen Anzahl von Bytes.
4.  Wiederholen Sie den Aufruf von [**HttpQueryInfo.**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)

Im folgenden Beispiel wird ein Aufruf von [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mithilfe der CRLF-Konstante HTTP QUERY RAW HEADERS veranschaulicht. Dabei handelt es sich um \_ einen speziellen \_ \_ \_ Wert, der alle zurückgegebenen HTTP-Header anfordert.


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



### <a name="retrieving-headers-using-http_query_custom"></a>Abrufen von Headern mit HTTP \_ QUERY \_ CUSTOM

Führen Sie die folgenden Schritte aus, um die [**HttpQueryInfo-Funktion**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) zum Abrufen eines HTTP-Headers mit HTTP QUERY CUSTOM zu \_ \_ verwenden:

1.  Ordnen Sie einen Puffer zu, der groß genug ist, um den Zeichenfolgennamen des HTTP-Headers zu speichern.
2.  Schreiben Sie den Zeichenfolgennamen des HTTP-Headers in den Puffer.
3.  Rufen Sie [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mit HTTP \_ QUERY CUSTOM \_ auf, dem Puffer, der den Zeichenfolgennamen des HTTP-Headers enthält, und der Variablen, die die Puffergröße enthält. Wenn Ihre Anwendung die Daten in einem bestimmten Format benötigt, können Sie außerdem eine Konstante aus der Liste [**Modifizierer**](query-info-flags.md) hinzufügen.
4.  Wenn beim Aufruf von [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ein Fehler auftritt und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ERROR INSUFFICIENT BUFFER zurückgibt, können \_ Sie einen Puffer mit der erforderlichen Anzahl von Bytes neu \_ verteilen.
5.  Schreiben Sie den Zeichenfolgennamen des HTTP-Headers erneut in den Puffer.
6.  Wiederholen Sie den Aufruf von [**HttpQueryInfo.**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)

Im folgenden Beispiel wird ein Aufruf von [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mithilfe der \_ BENUTZERDEFINIERTEN HTTP-ABFRAGEkonstante \_ veranschaulicht, um den CONTENT-Type-HTTP-Header anzufordern.


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
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 