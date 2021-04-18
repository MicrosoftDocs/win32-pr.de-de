---
title: HTTP Server-API, Version 2,0, Datentypen
description: HTTP Server-API, Version 2,0, Datentypen
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340443"
---
# <a name="http-server-api-version-20-data-types"></a><span data-ttu-id="e0ab1-103">HTTP Server-API, Version 2,0, Datentypen</span><span class="sxs-lookup"><span data-stu-id="e0ab1-103">HTTP Server API Version 2.0 Data Types</span></span>

<span data-ttu-id="e0ab1-104">Die HTTP-Server-API verwendet verschiedene im http. h-Header deklarierte Typen von speziellen Zweck Bezeichnern wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e0ab1-104">The HTTP Server API uses various special purpose identifier types declared in the Http.h header as follows:</span></span>

-   <span data-ttu-id="e0ab1-105">**UShort** Timeout für HTTP- \_ Dienst \_ Konfigurations \_ Timeout \_ , \* Phttp- \_ Dienst \_ Konfigurations \_ Timeout \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="e0ab1-105">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>
-   <span data-ttu-id="e0ab1-106">**ULONGLONG** HTTP \_ - \_ opop-ID, nicht transparente \* Phttp- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="e0ab1-106">**ULONGLONG** HTTP\_OPAQUE\_ID, \*PHTTP\_OPAQUE\_ID</span></span>
-   <span data-ttu-id="e0ab1-107">**Http \_ nicht transparente \_ ID** HTTP-Anforderungs- \_ \_ ID, \* Phttp- \_ Anforderungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="e0ab1-107">**HTTP\_OPAQUE\_ID** HTTP\_REQUEST\_ID, \*PHTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="e0ab1-108">**Http \_ nicht transparente \_ ID** HTTP-Verbindungs- \_ \_ ID, \* Phttp- \_ Verbindungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="e0ab1-108">**HTTP\_OPAQUE\_ID** HTTP\_CONNECTION\_ID, \*PHTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="e0ab1-109">**Http \_ nicht transparente \_ ID** http- \_ \_ rohverbindungs- \_ ID, \* Phttp- \_ \_ rohverbindungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="e0ab1-109">**HTTP\_OPAQUE\_ID** HTTP\_RAW\_CONNECTION\_ID, \*PHTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="e0ab1-110">**UShort** Timeout für HTTP- \_ Dienst \_ Konfigurations \_ Timeout \_ , \* Phttp- \_ Dienst \_ Konfigurations \_ Timeout \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="e0ab1-110">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>

<span data-ttu-id="e0ab1-111">Eine Anwendung sollte nicht versuchen, einen Bezeichner zu generieren oder zu ändern, der zu einem dieser Typen gehört.</span><span class="sxs-lookup"><span data-stu-id="e0ab1-111">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




