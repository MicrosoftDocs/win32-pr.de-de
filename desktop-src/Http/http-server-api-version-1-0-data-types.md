---
title: HTTP Server-API, Version 1,0, Datentypen
description: Die HTTP-Server-API verwendet verschiedene in der http. h-Header Datei deklarierte Typen von speziellen Zweck Bezeichnern als 64-Bit-Ganzzahlen ohne Vorzeichen.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID http-Typ
- HTTP_RAW_CONNECTION_ID http-Typ
- HTTP_REQUEST_ID http-Typ
- HTTP_URL_CONTEXT http-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338019"
---
# <a name="http-server-api-version-10-data-types"></a><span data-ttu-id="4f960-107">HTTP Server-API, Version 1,0, Datentypen</span><span class="sxs-lookup"><span data-stu-id="4f960-107">HTTP Server API Version 1.0 Data Types</span></span>

<span data-ttu-id="4f960-108">Die HTTP-Server-API verwendet verschiedene Typen von speziellen Zweck Bezeichnern, die in der http. h-Header Datei als 64-Bit-Ganzzahlen ohne Vorzeichen (**ulonglongs**) deklariert sind:</span><span class="sxs-lookup"><span data-stu-id="4f960-108">The HTTP Server API uses various special purpose identifier types declared in the Http.h header file as 64-bit unsigned integers (**ULONGLONGs**):</span></span>

-   <span data-ttu-id="4f960-109">HTTP- \_ Verbindungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="4f960-109">HTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="4f960-110">HTTP \_ - \_ rohverbindungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="4f960-110">HTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="4f960-111">HTTP- \_ Anforderungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="4f960-111">HTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="4f960-112">HTTP- \_ URL- \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="4f960-112">HTTP\_URL\_CONTEXT</span></span>

<span data-ttu-id="4f960-113">Eine Anwendung sollte nicht versuchen, einen Bezeichner zu generieren oder zu ändern, der zu einem dieser Typen gehört.</span><span class="sxs-lookup"><span data-stu-id="4f960-113">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




