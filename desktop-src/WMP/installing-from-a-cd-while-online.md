---
title: Installation von einer CD während der Online Installation
description: Installation von einer CD während der Online Installation
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player Online Stores, Installation von CD, während Online
- Onlinespeicher, Installation von CD, während Online
- Geben Sie 1 Online Stores ein, während Online von CD installiert wird.
- Typ 2 Online Stores, Installation von CD, während Online
- Windows Media Player Online Stores, Online Installationen von CD
- Online-Stores, Online Installationen von CD
- Typ 1 Online Stores, Online Installationen von CD
- Typ 2 Online Stores, Online Installationen von CD
- Windows Media Player Online Stores, CD-Installationen im Online Modus
- Online Stores, CD-Installationen im Online Modus
- Geben Sie 1 Online Stores, CD-Installationen Online ein.
- Geben Sie 2 Online Stores, CD-Installationen Online ein.
- Online-Store von CD in Online Installation installieren
- CD-Installationen von Online Stores im Online Modus
- Online Installationen von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338393"
---
# <a name="installing-from-a-cd-while-online"></a><span data-ttu-id="604e7-118">Installation von einer CD während der Online Installation</span><span class="sxs-lookup"><span data-stu-id="604e7-118">Installing from a CD While Online</span></span>

<span data-ttu-id="604e7-119">Benutzer können Windows Media Player von einer CD installieren, während Sie mit dem Internet verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="604e7-119">Users can install Windows Media Player from a CD while connected to the Internet.</span></span> <span data-ttu-id="604e7-120">In diesem Fall findet das Windows Media Player-Setup das vom *serviceInfo* -Befehlszeilenparameter angegebene serviceInfo-Dokument.</span><span class="sxs-lookup"><span data-stu-id="604e7-120">When this happens, Windows Media Player setup locates the ServiceInfo document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="604e7-121">Wenn das **Schlüssel** Attribut mit dem *defaultservice* -Befehlszeilenparameter übereinstimmt, prüft Setup das install-Element, um den Setup Vorgang anzupassen.</span><span class="sxs-lookup"><span data-stu-id="604e7-121">If the **Key** attribute matches the *DefaultService* command line parameter, setup inspects the Install element to customize the setup process.</span></span> <span data-ttu-id="604e7-122">Wenn Sie die Attributwerte verwenden, werden Ihre Endbenutzer-Lizenzbedingungen (EULA) und ihre Datenschutzbestimmungen angezeigt. Außerdem wird die CAB-Datei auf dem Computer des Benutzers abgerufen und installiert.</span><span class="sxs-lookup"><span data-stu-id="604e7-122">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="604e7-123">Beispielsweise können Sie diese Funktion verwenden, um die neueste Version eines COM-Objekts zu installieren, das für den Online Shop erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="604e7-123">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

<span data-ttu-id="604e7-124">Nachdem es installiert wurde, legt Windows Media Player den anfänglichen Online Store mithilfe des Schlüssel namensfest, den Sie für den *defaultservice* -Befehlszeilenparameter angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="604e7-124">After it is installed, Windows Media Player sets the initial online store using the key name you specified for the *DefaultService* command line parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="604e7-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="604e7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="604e7-126">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="604e7-126">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="604e7-127">**Install-Element**</span><span class="sxs-lookup"><span data-stu-id="604e7-127">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="604e7-128">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="604e7-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="604e7-129">**Festlegen des ersten Online Stores**</span><span class="sxs-lookup"><span data-stu-id="604e7-129">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="604e7-130">**Einrichten von Befehlszeilen Parametern für Online Stores**</span><span class="sxs-lookup"><span data-stu-id="604e7-130">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




