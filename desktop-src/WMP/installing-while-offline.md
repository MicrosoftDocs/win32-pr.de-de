---
title: Offline Installation
description: Offline Installation
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player Online Stores, Offline Installation
- Online Stores, Offline Installation
- Typ 1 Online Stores, Offline Installation
- Typ 2 Online Stores, Offline Installation
- Windows Media Player Online Stores, Offline Installationen
- Online Stores, Offline Installationen
- Typ 1 Online Stores, Offline Installationen
- Typ 2 Online Stores, Offline Installationen
- Offline Installation von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856364"
---
# <a name="installing-while-offline"></a><span data-ttu-id="140e6-112">Offline Installation</span><span class="sxs-lookup"><span data-stu-id="140e6-112">Installing While Offline</span></span>

<span data-ttu-id="140e6-113">Benutzer können Windows Media Player installieren, ohne mit dem Internet verbunden zu sein.</span><span class="sxs-lookup"><span data-stu-id="140e6-113">Users can install Windows Media Player while not connected to the Internet.</span></span> <span data-ttu-id="140e6-114">In diesem Fall findet das Windows-Media Player Setup das ServiceInfo.xml Dokument, das durch den *serviceInfo* -Befehlszeilenparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="140e6-114">When this happens, Windows Media Player setup locates the ServiceInfo.xml document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="140e6-115">Wenn das **Schlüssel** Attribut mit dem *defaultservice* -Befehlszeilenparameter übereinstimmt, wendet Setup Informationen aus den folgenden Elementen auf Windows Media Player an:</span><span class="sxs-lookup"><span data-stu-id="140e6-115">If the **Key** attribute matches the *DefaultService* command line parameter, setup applies information from the following elements to Windows Media Player:</span></span>

-   <span data-ttu-id="140e6-116">FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="140e6-116">FriendlyName.</span></span> <span data-ttu-id="140e6-117">Der Anzeige Name des Online-Stores wird auf der Windows Media Player-Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="140e6-117">The friendly name of the online store is shown in the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="140e6-118">Farbe</span><span class="sxs-lookup"><span data-stu-id="140e6-118">Color.</span></span> <span data-ttu-id="140e6-119">Die angegebenen Farben werden auf die Taskleiste und die Schaltflächen angewendet.</span><span class="sxs-lookup"><span data-stu-id="140e6-119">The specified colors are applied to the taskbar and buttons.</span></span>
-   <span data-ttu-id="140e6-120">ServiceTask1, ServiceTask2 und ServiceTask3.</span><span class="sxs-lookup"><span data-stu-id="140e6-120">ServiceTask1, ServiceTask2, and ServiceTask3.</span></span> <span data-ttu-id="140e6-121">Die untergeordneten Elemente ButtonText und buttontip werden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="140e6-121">The ButtonText and ButtonTip child elements are set.</span></span> <span data-ttu-id="140e6-122">Das URL-Attribut ist nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="140e6-122">The URL attribute is not set.</span></span> <span data-ttu-id="140e6-123">Die URL wird festgelegt, sobald der Benutzer eine Verbindung mit dem Internet herstellt und Windows Media Player die Liste der Online Stores auf normale Weise abruft.</span><span class="sxs-lookup"><span data-stu-id="140e6-123">URL is set once the user connects to the Internet and Windows Media Player retrieves its list of online stores in the normal fashion.</span></span>
-   <span data-ttu-id="140e6-124">Bild.</span><span class="sxs-lookup"><span data-stu-id="140e6-124">Image.</span></span> <span data-ttu-id="140e6-125">Die Attribute menuurl und servicelargeurl sind festgelegt.</span><span class="sxs-lookup"><span data-stu-id="140e6-125">The MenuURL and ServiceLargeURL attributes are set.</span></span> <span data-ttu-id="140e6-126">Diese URLs müssen auf Images verweisen, die Sie auf der Festplatte des Benutzers mithilfe des file://-Protokolls installiert haben.</span><span class="sxs-lookup"><span data-stu-id="140e6-126">These URLs must point to images you installed on the user's hard disk by using the file:// protocol.</span></span>

<span data-ttu-id="140e6-127">Wenn der Benutzer versucht, den Online Store anzuzeigen, zeigt Windows Media Player eine Meldung an, in der der Benutzer darüber informiert wird, dass eine Internet Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="140e6-127">When the user attempts to view the online store, Windows Media Player displays a message informing the user that an Internet connection is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="140e6-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="140e6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="140e6-129">**Color-Element**</span><span class="sxs-lookup"><span data-stu-id="140e6-129">**Color Element**</span></span>](color-element.md)
</dt> <dt>

[<span data-ttu-id="140e6-130">**FriendlyName-Element**</span><span class="sxs-lookup"><span data-stu-id="140e6-130">**FriendlyName Element**</span></span>](friendlyname-element.md)
</dt> <dt>

[<span data-ttu-id="140e6-131">**Image-Element**</span><span class="sxs-lookup"><span data-stu-id="140e6-131">**Image Element**</span></span>](image-element.md)
</dt> <dt>

[<span data-ttu-id="140e6-132">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="140e6-132">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="140e6-133">**Servicinput info-Element**</span><span class="sxs-lookup"><span data-stu-id="140e6-133">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> <dt>

[<span data-ttu-id="140e6-134">**ServiceTask1-Element**</span><span class="sxs-lookup"><span data-stu-id="140e6-134">**ServiceTask1 Element**</span></span>](servicetask1-element.md)
</dt> <dt>

[<span data-ttu-id="140e6-135">**ServiceTask2-Element**</span><span class="sxs-lookup"><span data-stu-id="140e6-135">**ServiceTask2 Element**</span></span>](servicetask2-element.md)
</dt> <dt>

[<span data-ttu-id="140e6-136">**ServiceTask3-Element**</span><span class="sxs-lookup"><span data-stu-id="140e6-136">**ServiceTask3 Element**</span></span>](servicetask3-element.md)
</dt> <dt>

[<span data-ttu-id="140e6-137">**Festlegen des ersten Online Stores**</span><span class="sxs-lookup"><span data-stu-id="140e6-137">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="140e6-138">**Einrichten von Befehlszeilen Parametern für Online Stores**</span><span class="sxs-lookup"><span data-stu-id="140e6-138">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




