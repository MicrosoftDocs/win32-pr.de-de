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
# <a name="retrieving-http-headers"></a><span data-ttu-id="1f4f2-103">Abrufen von HTTP-Headern</span><span class="sxs-lookup"><span data-stu-id="1f4f2-103">Retrieving HTTP Headers</span></span>

<span data-ttu-id="1f4f2-104">In diesem Tutorial wird beschrieben, wie Header Informationen aus HTTP-Anforderungen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-104">This tutorial describes how to retrieve header information from HTTP requests.</span></span>

## <a name="implementation-steps"></a><span data-ttu-id="1f4f2-105">Implementierungs Schritte</span><span class="sxs-lookup"><span data-stu-id="1f4f2-105">Implementation Steps</span></span>

<span data-ttu-id="1f4f2-106">Die Header Informationen können auf zwei Arten abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="1f4f2-106">There are two ways to retrieve the header information:</span></span>

-   <span data-ttu-id="1f4f2-107">Verwenden Sie eine der [**abfrageinfoflag**](query-info-flags.md) -Konstanten, die dem HTTP-Header zugeordnet sind, den Ihre Anwendung benötigt.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-107">Use one of the [**Query Info Flag**](query-info-flags.md) constants associated with the HTTP header that your application needs.</span></span>
-   <span data-ttu-id="1f4f2-108">Verwenden Sie das \_ \_ benutzerdefinierte Attribut Flag für die HTTP-Abfrage, und übergeben Sie den Namen des HTTP-Headers.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-108">Use the HTTP\_QUERY\_CUSTOM attribute flag and pass the name of the HTTP header.</span></span>

<span data-ttu-id="1f4f2-109">Das Verwenden der dem HTTP-Header zugeordneten Konstante, die Ihre Anwendung benötigt, ist intern schneller, aber es können HTTP-Header vorhanden sein, denen keine Konstante zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-109">Using the constant associated with the HTTP header that your application needs is faster internally, but there might be HTTP headers that do not have a constant associated with them.</span></span> <span data-ttu-id="1f4f2-110">In diesen Fällen ist die-Methode verfügbar, die das \_ \_ benutzerdefinierte Flag für die HTTP-Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-110">For those cases, the method using the HTTP\_QUERY\_CUSTOM attribute flag is available.</span></span>

<span data-ttu-id="1f4f2-111">Beide Methoden verwenden die [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-111">Both methods use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function.</span></span> <span data-ttu-id="1f4f2-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) übernimmt den [**HINTERNET**](appendix-a-hinternet-handles.md) -handle, für den die HTTP-Anforderung erfolgt ist, ein Attribut, einen Puffer, einen DWORD-Wert, der die Puffergröße enthält, und einen Indexwert.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle on which the HTTP request was made, one attribute, a buffer, a DWORD value that contains the buffer size, and an index value.</span></span> <span data-ttu-id="1f4f2-113">Ein Modifizierer kann auch dem an [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) übergebenen Attribut hinzugefügt werden, um anzugeben, in welchem Format die Daten zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-113">A modifier can also be added to the attribute passed to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to indicate in what format the data should be returned.</span></span>

### <a name="retrieving-headers-using-a-constant"></a><span data-ttu-id="1f4f2-114">Abrufen von Headern mit einer Konstanten</span><span class="sxs-lookup"><span data-stu-id="1f4f2-114">Retrieving Headers Using a Constant</span></span>

<span data-ttu-id="1f4f2-115">Führen Sie die folgenden Schritte aus, um mithilfe der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Funktion einen HTTP-Header mit einer Konstanten abzurufen:</span><span class="sxs-lookup"><span data-stu-id="1f4f2-115">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using a constant, follow these steps:</span></span>

1.  <span data-ttu-id="1f4f2-116">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mit einer Konstanten aus der [**Attribut**](query-info-flags.md) Liste, einem **null** -Puffer und der Variablen, die die Puffergröße enthält, auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-116">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with a constant from the [**Attributes**](query-info-flags.md) list, a **NULL** buffer, and the variable that holds the buffer size set to zero.</span></span> <span data-ttu-id="1f4f2-117">Außerdem können Sie, wenn die Anwendung die Daten in einem bestimmten Format benötigt, eine Konstante aus der Liste [**Modifizierer**](query-info-flags.md) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-117">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
2.  <span data-ttu-id="1f4f2-118">Wenn der angeforderte HTTP-Header vorhanden ist, sollte der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl einen Fehler erzeugen, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) sollte fehlerhaften Puffer zurückgeben \_ \_ , und die für den *lpdwbufferlength* -Parameter übergebenen Variable sollte auf die erforderliche Anzahl von Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-118">If the requested HTTP header exists, the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) should fail, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should return ERROR\_INSUFFICIENT\_BUFFER, and the variable passed for the *lpdwBufferLength* parameter should be set to the number of bytes required.</span></span>
3.  <span data-ttu-id="1f4f2-119">Weisen Sie einen Puffer mit der Anzahl der erforderlichen Bytes zu.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-119">Allocate a buffer with the number of bytes required.</span></span>
4.  <span data-ttu-id="1f4f2-120">Wiederholen Sie den [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-120">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="1f4f2-121">Das folgende Beispiel veranschaulicht einen [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl mithilfe der CRLF-Konstante für den HTTP- \_ Abfrage \_ \_ rohheader \_ , bei der es sich um einen speziellen Wert handelt, der alle zurückgegebenen HTTP-Header anfordert.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-121">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_RAW\_HEADERS\_CRLF constant, which is a special value that requests all of the returned HTTP headers.</span></span>


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



### <a name="retrieving-headers-using-http_query_custom"></a><span data-ttu-id="1f4f2-122">Abrufen von Headern mithilfe \_ der \_ benutzerdefinierten HTTP-Abfrage</span><span class="sxs-lookup"><span data-stu-id="1f4f2-122">Retrieving Headers Using HTTP\_QUERY\_CUSTOM</span></span>

<span data-ttu-id="1f4f2-123">Führen Sie die folgenden Schritte aus, um mithilfe der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Funktion einen HTTP-Header mit \_ \_ benutzerdefiniertem HTTP-Abfrage abzurufen:</span><span class="sxs-lookup"><span data-stu-id="1f4f2-123">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using HTTP\_QUERY\_CUSTOM, follow these steps:</span></span>

1.  <span data-ttu-id="1f4f2-124">Weisen Sie einen Puffer zu, der groß genug ist, um den Zeichen folgen Namen des HTTP-Headers aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-124">Allocate a buffer that is large enough to hold the string name of the HTTP header.</span></span>
2.  <span data-ttu-id="1f4f2-125">Schreiben Sie den Zeichen folgen Namen des HTTP-Headers in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-125">Write the string name of the HTTP header into the buffer.</span></span>
3.  <span data-ttu-id="1f4f2-126">Nennen Sie [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) mit \_ der \_ benutzerdefinierten HTTP-Abfrage, dem Puffer, der den Zeichen folgen Namen des HTTP-Headers enthält, und der Variablen, die die Puffergröße enthält.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-126">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with HTTP\_QUERY\_CUSTOM, the buffer that contains the string name of the HTTP header, and the variable that holds the buffer size.</span></span> <span data-ttu-id="1f4f2-127">Außerdem können Sie, wenn die Anwendung die Daten in einem bestimmten Format benötigt, eine Konstante aus der Liste [**Modifizierer**](query-info-flags.md) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-127">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
4.  <span data-ttu-id="1f4f2-128">Wenn der [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl fehlschlägt und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fehlerhaften Puffer zurückgibt \_ \_ , ordnen Sie einen Puffer mit der erforderlichen Anzahl von Bytes neu zu.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-128">If the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, reallocate a buffer with the number of bytes required.</span></span>
5.  <span data-ttu-id="1f4f2-129">Schreiben Sie den Zeichen folgen Namen des HTTP-Headers erneut in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-129">Write the string name of the HTTP header into the buffer again.</span></span>
6.  <span data-ttu-id="1f4f2-130">Wiederholen Sie den [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-130">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="1f4f2-131">Das folgende Beispiel veranschaulicht einen [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) -Befehl, indem die \_ \_ benutzerdefinierte HTTP-Abfrage-Konstante verwendet wird, um den Content-Type-HTTP-Header anzufordern.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-131">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_CUSTOM constant to request the Content-Type HTTP header.</span></span>


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
> <span data-ttu-id="1f4f2-132">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="1f4f2-133">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f4f2-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="1f4f2-134">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="1f4f2-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 