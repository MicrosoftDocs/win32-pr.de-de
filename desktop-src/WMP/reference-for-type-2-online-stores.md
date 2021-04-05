---
title: Referenz für Typ 2-Onlineshops
description: Referenz für Typ 2-Onlineshops
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player Online Stores, Referenz
- Online Stores, Referenz
- Typ 2 Online Stores, Referenz
- Referenz für den Typ 2-Onlinespeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724188"
---
# <a name="reference-for-type-2-online-stores"></a><span data-ttu-id="86cd4-107">Referenz für Typ 2-Onlineshops</span><span class="sxs-lookup"><span data-stu-id="86cd4-107">Reference for Type 2 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="86cd4-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="86cd4-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="86cd4-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86cd4-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="86cd4-110">Windows Media Player 10 oder höher stellt Objekte, Schnittstellen, Eigenschaften und Methoden bereit, die den Typ 2 Online-Speicher unterstützen.</span><span class="sxs-lookup"><span data-stu-id="86cd4-110">Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores.</span></span> <span data-ttu-id="86cd4-111">In den folgenden Abschnitten werden diese ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="86cd4-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="86cd4-112">`Section`</span><span class="sxs-lookup"><span data-stu-id="86cd4-112">Section</span></span>                                                                                                        | <span data-ttu-id="86cd4-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86cd4-113">Description</span></span>                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86cd4-114">Iwmpabonneptionservice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="86cd4-114">IWMPSubscriptionService Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | <span data-ttu-id="86cd4-115">Stellt Methoden bereit, um Digital Rights Management (DRM) zu erweitern und Hintergrundprozesse zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="86cd4-115">Provides methods to augment digital rights management (DRM) and initiate background processes.</span></span>                                                                              |
| [<span data-ttu-id="86cd4-116">IWMPSubscriptionService2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="86cd4-116">IWMPSubscriptionService2 Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | <span data-ttu-id="86cd4-117">Stellt Methoden zum Initiieren von Hintergrundprozessen, zum Bereitstellen von Informationen über die Online Store-Aktivität und zum Bereitstellen eines Zeigers auf die Windows Media Player Core-Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="86cd4-117">Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface.</span></span> |
| [<span data-ttu-id="86cd4-118">Iwmpabonneptionservicecallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="86cd4-118">IWMPSubscriptionServiceCallback Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | <span data-ttu-id="86cd4-119">Definiert eine Methode, mit der Onlinespeicher Windows Media Player Benachrichtigen, wenn ein Hintergrundprozess abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="86cd4-119">Defines a method that online stores use to notify Windows Media Player when a background process is completed.</span></span>                                                              |
| [<span data-ttu-id="86cd4-120">Wmpnotifyabonptionpluginadressmove</span><span class="sxs-lookup"><span data-stu-id="86cd4-120">WMPNotifySubscriptionPluginAddRemove</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | <span data-ttu-id="86cd4-121">Eine Funktion, mit der Windows Media Player benachrichtigt wird, dass ein Plug-in installiert oder deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="86cd4-121">A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.</span></span>                                                                            |
| [<span data-ttu-id="86cd4-122">Download Collection-Objekt</span><span class="sxs-lookup"><span data-stu-id="86cd4-122">DownloadCollection Object</span></span>](downloadcollection-object.md)                                                     | <span data-ttu-id="86cd4-123">Stellt Methoden und Eigenschaften zum Verwalten von Auflistungen von Download Elementen bereit.</span><span class="sxs-lookup"><span data-stu-id="86cd4-123">Provides methods and properties to manage collections of download items.</span></span>                                                                                                    |
| [<span data-ttu-id="86cd4-124">Download Item-Objekt</span><span class="sxs-lookup"><span data-stu-id="86cd4-124">DownloadItem Object</span></span>](downloaditem-object.md)                                                                 | <span data-ttu-id="86cd4-125">Stellt Methoden und Eigenschaften für Download Anforderungen bereit.</span><span class="sxs-lookup"><span data-stu-id="86cd4-125">Provides methods and properties relating to download requests.</span></span>                                                                                                              |
| [<span data-ttu-id="86cd4-126">Download Manager-Objekt</span><span class="sxs-lookup"><span data-stu-id="86cd4-126">DownloadManager Object</span></span>](downloadmanager-object.md)                                                           | <span data-ttu-id="86cd4-127">Stellt Methoden zum Verwalten von Download Auflistungen bereit.</span><span class="sxs-lookup"><span data-stu-id="86cd4-127">Provides methods to manage download collections.</span></span>                                                                                                                            |
| [<span data-ttu-id="86cd4-128">Externes Objekt für den Typ 2-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="86cd4-128">External Object for Type 2 Online Stores</span></span>](external-object-for-type-2-online-stores.md)                       | <span data-ttu-id="86cd4-129">Stellt Eigenschaften, Methoden und ein Ereignis bereit, auf die über Webseiten im Online Store zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="86cd4-129">Provides properties, methods, and an event accessible from online store webpages.</span></span>                                                                                           |
| [<span data-ttu-id="86cd4-130">Enumerationen für den Typ 2-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="86cd4-130">Enumerations for Type 2 Online Stores</span></span>](enumerations-for-type-2-online-stores.md)                             | <span data-ttu-id="86cd4-131">Beschreibt Enumerationen, die von Online Stores verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86cd4-131">Describes enumerations used by online stores.</span></span>                                                                                                                               |
| [<span data-ttu-id="86cd4-132">Windows Media Player Bits-Auftrags Konvention</span><span class="sxs-lookup"><span data-stu-id="86cd4-132">Windows Media Player BITS Job Convention</span></span>](windows-media-player-bits-job-convention.md)                       | <span data-ttu-id="86cd4-133">Beschreibt eine Konvention für die Verwendung des Background Intelligent Transfer Service (Bits).</span><span class="sxs-lookup"><span data-stu-id="86cd4-133">Describes a convention for using the Background Intelligent Transfer Service (BITS).</span></span>                                                                                        |
| [<span data-ttu-id="86cd4-134">Registrierungsschlüssel und-Einträge für einen Typ 2-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="86cd4-134">Registry Keys and Entries for a Type 2 Online Store</span></span>](registry-keys-and-entries-for-a-type-2-online-store.md) | <span data-ttu-id="86cd4-135">Beschreibt Registrierungseinträge, die von einem Online Shop in der Registrierung auf dem Computer des Benutzers erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="86cd4-135">Describes registry entries that an online store must create in the registry on the user's computer.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="86cd4-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86cd4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86cd4-137">**Typ 2 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="86cd4-137">**Type 2 Online Stores**</span></span>](type-2-online-stores.md)
</dt> </dl>

 

 




