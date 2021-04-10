---
title: Einrichten von Befehlszeilen Parametern für Online Stores
description: Einrichten von Befehlszeilen Parametern für Online Stores
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player Online Stores, Setup-Befehlszeilenparameter
- Online Stores, Setup-Befehlszeilenparameter
- Typ 1 Online Stores, Setup Befehlszeilenparameter
- Typ 2 Online Stores, Setup Befehlszeilenparameter
- Setup-Befehlszeilenparameter
- Windows Media Player Online Stores, Befehlszeilenparameter
- Online Stores, Befehlszeilenparameter
- Typ 1 Online Stores, Befehlszeilenparameter
- Typ 2 Online Stores, Befehlszeilenparameter
- Befehlszeilenparameter
- Windows Media Player Online Stores, Parameter
- Online Stores, Parameter
- Typ 1 Online Stores, Parameter
- Typ 2 Online Stores, Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036895"
---
# <a name="setup-command-line-parameters-for-online-stores"></a><span data-ttu-id="6d6e0-117">Einrichten von Befehlszeilen Parametern für Online Stores</span><span class="sxs-lookup"><span data-stu-id="6d6e0-117">Setup Command-line Parameters for Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="6d6e0-118">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="6d6e0-118">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6d6e0-119">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-119">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6d6e0-120">Bei der Installation von Windows Media Player 10 oder Windows Media Player 11 unter Windows XP können Sie Befehlszeilenparameter anfügen, um den ersten Onlinespeicher anzugeben, der dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-120">When installing Windows Media Player 10 or Windows Media Player 11 on Windows XP, you can append command-line parameters to specify the first online store that the user sees.</span></span>

<span data-ttu-id="6d6e0-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d6e0-121">Syntax</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



<span data-ttu-id="6d6e0-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d6e0-122">Parameters</span></span>

<span data-ttu-id="6d6e0-123">Defaultservice (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="6d6e0-123">DefaultService (required)</span></span>

<span data-ttu-id="6d6e0-124">Der Schlüssel Name für den Online Shop.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-124">The key name for the online store.</span></span> <span data-ttu-id="6d6e0-125">Dieser Wert muss mit dem Schlüsselnamen im **Key** -Attribut des **serviceInfo** -Elements des serviceInfo-Dokuments übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-125">This value must match the key name in the **Key** attribute of the **ServiceInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="6d6e0-126">Serviceingefo (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="6d6e0-126">ServiceInfo (required)</span></span>

<span data-ttu-id="6d6e0-127">Der voll qualifizierte Pfad zu einem serviceInfo-Dokument, das auf dem Computer des Benutzers installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-127">The fully qualified path to a ServiceInfo document installed on the user's computer.</span></span>

<span data-ttu-id="6d6e0-128">Serviceextra (optional)</span><span class="sxs-lookup"><span data-stu-id="6d6e0-128">ServiceExtra (optional)</span></span>

<span data-ttu-id="6d6e0-129">Eine Abfrage Zeichenfolge, die von Windows Media Player 10 an die URL des serviceingefo-Dokuments angehängt wird, wenn das Dokument online abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-129">A query string that Windows Media Player 10 will append to the URL for the ServiceInfo document when it retrieves the document online.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6e0-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d6e0-130">Remarks</span></span>

<span data-ttu-id="6d6e0-131">Ausführliche Informationen zur Neuverteilung von Windows Media Player-Software mit Ihrer Anwendung finden Sie unter [Verteilen von Windows Media Player Software](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="6d6e0-131">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="6d6e0-132">Wenn der Computer des Benutzers nicht mit dem Internet verbunden ist, werden die im lokalen serviceInfo-Dokument enthaltenen Informationen verwendet, um Windows-Media Player für den ersten aktiven Dienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-132">When the user's computer is not connected to the Internet, the information contained in the local ServiceInfo document is used to configure Windows Media Player for the initial active service.</span></span>

<span data-ttu-id="6d6e0-133">Bei Befehlszeilen Parametern wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="6d6e0-133">Command-line parameters are case sensitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d6e0-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d6e0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d6e0-135">**Co-Branding von Online Stores**</span><span class="sxs-lookup"><span data-stu-id="6d6e0-135">**Co-Branding Online Stores**</span></span>](co-branding-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6d6e0-136">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="6d6e0-136">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6d6e0-137">**Install-Element**</span><span class="sxs-lookup"><span data-stu-id="6d6e0-137">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="6d6e0-138">**Festlegen des ersten Online Stores**</span><span class="sxs-lookup"><span data-stu-id="6d6e0-138">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




