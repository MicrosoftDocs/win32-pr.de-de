---
title: HTTP-Anforderungen für Bits-Downloads
description: Bits unterstützt HTTP-und HTTPS-Downloads und-Uploads und erfordert, dass der Server das HTTP/1.1-Protokoll unterstützt.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470965"
---
# <a name="http-requirements-for-bits-downloads"></a><span data-ttu-id="aeccf-103">HTTP-Anforderungen für Bits-Downloads</span><span class="sxs-lookup"><span data-stu-id="aeccf-103">HTTP Requirements for BITS Downloads</span></span>

<span data-ttu-id="aeccf-104">Bits unterstützt HTTP-und HTTPS-Downloads und-Uploads und erfordert, dass der Server das HTTP/1.1-Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aeccf-104">BITS supports HTTP and HTTPS downloads and uploads and requires that the server supports the HTTP/1.1 protocol.</span></span> <span data-ttu-id="aeccf-105">Für Downloads muss die **Head** -Methode des HTTP-Servers die Dateigröße zurückgeben, und die **Get** -Methode muss den Content-Range-Header und den Content-Length-Header unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aeccf-105">For downloads, the HTTP server's **Head** method must return the file size and its **Get** method must support the Content-Range and Content-Length headers.</span></span> <span data-ttu-id="aeccf-106">Folglich überträgt Bits nur den Inhalt statischer Dateien und generiert einen Fehler, wenn Sie versuchen, dynamischen Inhalt zu übertragen, es sei denn, das ASP-, ISAPI-oder CGI-Skript unterstützt den Content-Range-Header und den Content-Length-Header.</span><span class="sxs-lookup"><span data-stu-id="aeccf-106">As a result, BITS only transfers static file content and generates an error if you try to transfer dynamic content, unless the ASP, ISAPI, or CGI script supports the Content-Range and Content-Length headers.</span></span>

<span data-ttu-id="aeccf-107">Bits können einen HTTP/1.0-Server verwenden, sofern diese den Anforderungen an die **Head** -und **Get** -Methode erfüllen.</span><span class="sxs-lookup"><span data-stu-id="aeccf-107">BITS can use an HTTP/1.0 server as long as it meets the **Head** and **Get** method requirements.</span></span>

<span data-ttu-id="aeccf-108">Der Server muss die folgenden Anforderungen erfüllen, um das Herunterladen von Bereichen einer Datei zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="aeccf-108">To support downloading ranges of a file, the server must support the following requirements:</span></span>

-   <span data-ttu-id="aeccf-109">Ermöglicht MIME-Headern das Einschließen der Standard Header für Content-Range und Content-Type sowie von maximal 180 bytes anderer Header.</span><span class="sxs-lookup"><span data-stu-id="aeccf-109">Allow MIME headers to include the standard Content-Range and Content-Type headers, plus a maximum of 180 bytes of other headers.</span></span>
-   <span data-ttu-id="aeccf-110">Maximal zwei CR/LFS zwischen den HTTP-Headern und der ersten Begrenzungs Zeichenfolge zulassen.</span><span class="sxs-lookup"><span data-stu-id="aeccf-110">Allow a maximum of two CR/LFs between the HTTP headers and the first boundary string.</span></span>

 

 




