---
title: Verarbeiten von Anforderungen
description: Verarbeitungsanforderungen umfassen vier Schritte.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "103869347"
---
# <a name="processing-requests"></a><span data-ttu-id="28f27-103">Verarbeiten von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28f27-103">Processing Requests</span></span>

<span data-ttu-id="28f27-104">Verarbeitungsanforderungen umfassen vier Schritte:</span><span class="sxs-lookup"><span data-stu-id="28f27-104">Processing requests includes four steps:</span></span>

-   <span data-ttu-id="28f27-105">Empfangen einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="28f27-105">Receiving a request</span></span>
-   <span data-ttu-id="28f27-106">Verarbeiten der Anforderung</span><span class="sxs-lookup"><span data-stu-id="28f27-106">Handling the request</span></span>
-   <span data-ttu-id="28f27-107">Senden der Antwort</span><span class="sxs-lookup"><span data-stu-id="28f27-107">Sending the response</span></span>
-   <span data-ttu-id="28f27-108">Abbrechen von Anforderungen, die nicht verarbeitet werden können</span><span class="sxs-lookup"><span data-stu-id="28f27-108">Canceling requests that cannot be processed</span></span>

![Diagramm, in dem die Prozess Anforderungs Schleife angezeigt wird.](images/processloop.png)

## <a name="receiving-a-request"></a><span data-ttu-id="28f27-110">Empfangen einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="28f27-110">Receiving a Request</span></span>

<span data-ttu-id="28f27-111">Die HTTP-Server-API stellt eine Anforderungs Struktur zum Speichern der analysierten eingehenden Anforderung bereit.</span><span class="sxs-lookup"><span data-stu-id="28f27-111">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="28f27-112">Diese Struktur wird von der Anwendung zugeordnet und initialisiert, wenn eine eingehende Anforderung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="28f27-112">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="28f27-113">Die Anwendung ruft die [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) -Funktion auf, um die Anforderung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="28f27-113">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="28f27-114">Wenn der Anforderungs Puffer zu klein ist, um die Anforderung zu empfangen, kann die Anwendung die Puffergröße erhöhen und **httpreceivehttprequest** erneut abrufen, um die gesamte Anforderung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="28f27-114">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="28f27-115">Wenn die Anforderung Entitäts Text Daten enthält, die empfangen werden sollen, ruft die Anwendung [**httpreceiverequestentitybody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) mit der Anforderungs-ID auf, die während des Aufrufs von [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)im *prequestbuffer* -Parameter zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="28f27-115">If the request includes entity body data to be received, the applications calls [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) with the request ID returned in the *pRequestBuffer* parameter during the call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span></span>

## <a name="handling-the-request"></a><span data-ttu-id="28f27-116">Verarbeiten der Anforderung</span><span class="sxs-lookup"><span data-stu-id="28f27-116">Handling the Request</span></span>

<span data-ttu-id="28f27-117">Die Anwendung führt die anwendungsspezifische Verarbeitung der Anforderung durch und formuliert eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="28f27-117">The application performs application-specific processing of the request and formulates a response.</span></span> <span data-ttu-id="28f27-118">Die HTTP-Server-API erzwingt keinen Timeout für diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="28f27-118">The HTTP Server API imposes no timeout on this process.</span></span>

## <a name="sending-the-response"></a><span data-ttu-id="28f27-119">Senden der Antwort</span><span class="sxs-lookup"><span data-stu-id="28f27-119">Sending the Response</span></span>

<span data-ttu-id="28f27-120">Wenn die Anwendung die Verarbeitung der Anforderung und das Formulieren der Antwort abgeschlossen hat, ruft Sie die [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) -Funktion auf, um die Antwort zu senden.</span><span class="sxs-lookup"><span data-stu-id="28f27-120">When the application is finished handling the request and formulating the response, it calls the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function to send the response.</span></span> <span data-ttu-id="28f27-121">Wenn die Antwort Entitäts Text Daten enthält, die gesendet werden sollen, ruft die Anwendung auch [httpsendresponseentitybody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)auf.</span><span class="sxs-lookup"><span data-stu-id="28f27-121">If the response includes entity body data to send, the application also calls [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

## <a name="canceling-requests"></a><span data-ttu-id="28f27-122">Abbrechen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28f27-122">Canceling Requests</span></span>

<span data-ttu-id="28f27-123">Nachdem die Anwendung eine Anforderungs-ID von Ihrem Aufruf an [**httpreceivehttprequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)erhalten hat, kann Sie die Anforderung jederzeit abbrechen, indem Sie [httpcancelhttprequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)aufruft.</span><span class="sxs-lookup"><span data-stu-id="28f27-123">After the application has received a request ID from its call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), it can at any time cancel the request by calling [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span></span>

 

 




