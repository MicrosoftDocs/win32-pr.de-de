---
title: Dynamisches Erstellen des serviceingefo-Dokuments
description: Dynamisches Erstellen des serviceingefo-Dokuments
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player Online Stores, Erstellen eines serviceingefo-Dokuments
- Online Stores, Erstellen eines serviceingefo-Dokuments
- Typ 1 Online Stores, serviceInfo-Dokument wird erstellt
- Typ 2 Online Stores, Erstellen von serviceInfo-Dokumenten
- Windows Media Player Online Stores, Dynamisches Erstellen von servicabfo-Dokumenten
- Online Stores, Dynamisches Erstellen von serviceingefo-Dokumenten
- Typ 1 Online Stores, Dynamisches Erstellen von serviceInfo-Dokumenten
- Typ 2 Online Stores, Dynamisches Erstellen von serviceInfo-Dokumenten
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Dynamisches Erstellen von servicinfo-Dokumenten
- servicinfo-Dokument wird erstellt
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947427"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a><span data-ttu-id="e0cdf-118">Dynamisches Erstellen des serviceingefo-Dokuments</span><span class="sxs-lookup"><span data-stu-id="e0cdf-118">Creating the ServiceInfo Document Dynamically</span></span>

<span data-ttu-id="e0cdf-119">Sie können ASP zum Erstellen des serviceingefo-Dokuments verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0cdf-119">You can use ASP to create your ServiceInfo document.</span></span> <span data-ttu-id="e0cdf-120">Dadurch erhalten Sie mehr Flexibilität in Ihrem Online Store, indem Sie die folgenden Verfahren verwenden:</span><span class="sxs-lookup"><span data-stu-id="e0cdf-120">This can give you greater flexibility in your online store by using the following techniques:</span></span>

-   <span data-ttu-id="e0cdf-121">Dynamisches Erstellen des Host Namens für URLs.</span><span class="sxs-lookup"><span data-stu-id="e0cdf-121">Dynamically generating the host name for URLs.</span></span>
-   <span data-ttu-id="e0cdf-122">Ändern von URLs für die Lokalisierung basierend auf Gebiets Schema-und Geoid-Parametern.</span><span class="sxs-lookup"><span data-stu-id="e0cdf-122">Changing URLs for localization based on locale and geoid parameters.</span></span>
-   <span data-ttu-id="e0cdf-123">Dynamisches Anfügen von Abfrage Zeichen folgen Parametern aus der serviceingefo-URL an andere URLs, z. b. die URL der Navigationsseite.</span><span class="sxs-lookup"><span data-stu-id="e0cdf-123">Dynamically appending query string parameters from the ServiceInfo URL to other URLs, such as the navigate page URL.</span></span>

<span data-ttu-id="e0cdf-124">Der folgende Beispielcode zeigt eine einfache ASP-Seite, die ein servicanfo-Dokument dynamisch erstellt:</span><span class="sxs-lookup"><span data-stu-id="e0cdf-124">The following example code shows a simple ASP page that dynamically creates a ServiceInfo document:</span></span>


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



<span data-ttu-id="e0cdf-125">Der vorherige Beispielcode verwendet ASP zum Abrufen des Host namens vom Webserver und zum dynamischen Erstellen der URLs im Dokument.</span><span class="sxs-lookup"><span data-stu-id="e0cdf-125">The preceding example code uses ASP to retrieve the host name from the web server and dynamically create the URLs in the document.</span></span> <span data-ttu-id="e0cdf-126">Der Code ruft auch den Parameter für die *locale* -Abfrage Zeichenfolge aus der servicinfo-Anforderung ab und fügt ihn an die URL für die Navigationsseite an.</span><span class="sxs-lookup"><span data-stu-id="e0cdf-126">The code also retrieves the *locale* query string parameter from the ServiceInfo request and appends it to the URL for the navigate page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0cdf-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0cdf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0cdf-128">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="e0cdf-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e0cdf-129">**Navigation für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="e0cdf-129">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e0cdf-130">**ServiceInfo-Dokument für einen Typ-1-Online Store**</span><span class="sxs-lookup"><span data-stu-id="e0cdf-130">**ServiceInfo Document for a Type 1 Online Store**</span></span>](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e0cdf-131">**ServiceInfo-Dokument für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="e0cdf-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e0cdf-132">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="e0cdf-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




