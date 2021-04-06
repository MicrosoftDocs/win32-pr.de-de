---
title: Remoteprozeduraufrufe mit dem RPC-über-HTTP-Proxy
description: Internet Browser Programme verwenden normalerweise das Hypertext Transport-Protokoll (http) als primäres Mittel zum Durchsuchen der World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Verwendung von RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947311"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a><span data-ttu-id="eae7d-104">Remoteprozeduraufrufe mit dem RPC-über-HTTP-Proxy</span><span class="sxs-lookup"><span data-stu-id="eae7d-104">Remote Procedure Calls Using RPC over HTTP</span></span>

<span data-ttu-id="eae7d-105">Internet Browser Programme verwenden normalerweise das Hypertext Transport-Protokoll (http) als primäres Mittel zum Durchsuchen der World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="eae7d-105">Internet browser programs commonly employ the Hypertext Transport Protocol (HTTP) as the primary means of browsing the World Wide Web.</span></span> <span data-ttu-id="eae7d-106">HTTP sieht daher auf den meisten Computern heute eine umfassende Nutzung vor.</span><span class="sxs-lookup"><span data-stu-id="eae7d-106">HTTP, therefore, sees extensive usage on most computers today.</span></span> <span data-ttu-id="eae7d-107">Microsoft hat die Funktionen seines Internet Informations Servers (IIS) erweitert, um Remote Prozedur Aufrufe mithilfe von http bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eae7d-107">Microsoft has extended the capabilities of its Internet Information Server (IIS) to provide remote procedure call services using HTTP.</span></span>

<span data-ttu-id="eae7d-108">Mit der Microsoft RPC-over-HTTP-Implementierung (RPC über HTTP) können RPC-Clients eine sichere und effiziente Internet Verbindung mit RPC-Serverprogrammen herstellen und Remote Prozedur Aufrufe ausführen.</span><span class="sxs-lookup"><span data-stu-id="eae7d-108">The Microsoft RPC-over-HTTP implementation (RPC over HTTP) allows RPC clients to securely and efficiently connect across the Internet to RPC server programs and execute remote procedure calls.</span></span> <span data-ttu-id="eae7d-109">Dies wird durch einen Vermittler, der als RPC-über-HTTP-Proxy bezeichnet wird, oder einfach durch den RPC-Proxy erreicht.</span><span class="sxs-lookup"><span data-stu-id="eae7d-109">This is accomplished with the help of an intermediary known as the RPC-over-HTTP Proxy, or simply the RPC Proxy.</span></span>

<span data-ttu-id="eae7d-110">Der RPC-Proxy wird auf einem IIS-Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eae7d-110">The RPC Proxy runs on an IIS computer.</span></span> <span data-ttu-id="eae7d-111">Er akzeptiert RPC-Anforderungen aus dem Internet, führt Authentifizierungs-, Validierungs-und Zugriffs Überprüfungen für diese Anforderungen aus. wenn die Anforderung alle Tests bestanden hat, leitet der RPC-Proxy die Anforderung an den RPC-Server weiter, der die tatsächliche Verarbeitung ausführt.</span><span class="sxs-lookup"><span data-stu-id="eae7d-111">It accepts RPC requests coming from the Internet, performs authentication, validation, and access checks on those requests, and if the request passes all tests, RPC Proxy forwards the request to the RPC server that performs the actual processing.</span></span> <span data-ttu-id="eae7d-112">Mit RPC über HTTP kommunizieren der RPC-Client und-Server nicht direkt. Stattdessen verwenden Sie den RPC-Proxy als Vermittler.</span><span class="sxs-lookup"><span data-stu-id="eae7d-112">With RPC over HTTP the RPC client and server do not communicate directly; rather, they use the RPC Proxy as intermediary.</span></span> <span data-ttu-id="eae7d-113">Dieses Modell wurde aus vielen Gründen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="eae7d-113">This model was chosen for many reasons.</span></span> <span data-ttu-id="eae7d-114">Weitere Informationen finden Sie unter [RPC-über-HTTP-Sicherheit](rpc-over-http-security.md).</span><span class="sxs-lookup"><span data-stu-id="eae7d-114">For more information, see [RPC over HTTP Security](rpc-over-http-security.md).</span></span>

<span data-ttu-id="eae7d-115">Dieser Abschnitt bietet eine Übersicht über RPC über http in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="eae7d-115">This section provides an overview of RPC over HTTP in the following topics:</span></span>

-   [<span data-ttu-id="eae7d-116">Verwenden von http als RPC-Transport</span><span class="sxs-lookup"><span data-stu-id="eae7d-116">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
-   [<span data-ttu-id="eae7d-117">RPC-über-HTTP-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="eae7d-117">RPC over HTTP Security</span></span>](rpc-over-http-security.md)
-   [<span data-ttu-id="eae7d-118">System Anforderungen und Interoperabilität für RPC über http</span><span class="sxs-lookup"><span data-stu-id="eae7d-118">System Requirements and Interoperability for RPC over HTTP</span></span>](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [<span data-ttu-id="eae7d-119">Konfigurieren von Computern für RPC über http</span><span class="sxs-lookup"><span data-stu-id="eae7d-119">Configuring Computers for RPC over HTTP</span></span>](configuring-computers-for-rpc-over-http.md)
-   [<span data-ttu-id="eae7d-120">Empfehlungen für RPC-over-HTTP</span><span class="sxs-lookup"><span data-stu-id="eae7d-120">RPC over HTTP Deployment Recommendations</span></span>](rpc-over-http-deployment-recommendations.md)

<span data-ttu-id="eae7d-121">Informationen zu großen RPC-über-HTTP-Szenarios finden Sie unter [Microsoft RPC-Lastenausgleich](rpc-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="eae7d-121">For information regarding high volume RPC over HTTP scenarios, please see [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span></span>

 

 




