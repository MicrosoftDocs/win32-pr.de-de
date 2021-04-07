---
title: Typ 1 Online Store-Plug-in
description: Typ 1 Online Store-Plug-in
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, iwmpcontentpartner-Schnittstelle
- Online Stores, iwmpcontentpartner-Schnittstelle
- Typ 1 Online Stores, iwmpcontentpartner-Schnittstelle
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, iwmpcontentpartner-Schnittstelle
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, iwmpcontentpartner-Schnittstelle
- Iwmpcontentpartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038690"
---
# <a name="type-1-online-store-plug-in"></a><span data-ttu-id="5ee9b-118">Typ 1 Online Store-Plug-in</span><span class="sxs-lookup"><span data-stu-id="5ee9b-118">Type 1 Online Store Plug-in</span></span>

<span data-ttu-id="5ee9b-119">Um die Funktionen der Bibliotheks Integration nutzen zu können, müssen Sie vom Typ 1 Online Store-Anbieter ein Plug-in erstellen, das die [iwmpcontentpartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5ee9b-119">To take advantage of library integration features, type 1 online store providers must create a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="5ee9b-120">Diese Schnittstelle stellt die Methoden bereit, die von Windows Media Player aufgerufen werden, um den Online Store über Aktivitäten zu benachrichtigen, die im Player stattfinden, und um bestimmte Informationen über Online Store-Inhalte, den Katalog oder den Speicher selbst abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ee9b-120">This interface provides the methods that Windows Media Player calls to notify the online store about activities taking place in the Player and to retrieve specific information about online store content, the catalog, or the store itself.</span></span>

<span data-ttu-id="5ee9b-121">Nachdem das Plug-in von Windows Media Player instanziiert wurde, ruft der Player [iwmpcontentpartner:: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)auf und stellt einen Zeiger auf die **iwmpcontentpartnercallback** -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="5ee9b-121">After Windows Media Player instantiates the plug-in, the Player calls [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback), and provides a pointer to the **IWMPContentPartnerCallback** interface.</span></span> <span data-ttu-id="5ee9b-122">Diese Schnittstelle ermöglicht dem Online Shop das Ausführen von Aufrufen an Windows Media Player, um Statusinformationen bereitzustellen oder bestimmte Prozesse, z. b. das Herunterladen eines Musiktitels, zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="5ee9b-122">This interface gives the online store a way to make calls into Windows Media Player to provide status information or to initiate specific processes, such as downloading a music track.</span></span>

<span data-ttu-id="5ee9b-123">Windows Media Player und das Plug-in werden in separaten Prozessen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ee9b-123">Windows Media Player and the plug-in run in separate processes.</span></span> <span data-ttu-id="5ee9b-124">Das Plug-in ist ein in-Process-Server, der im standardmäßigen dll-Ersatz dllhost.exe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ee9b-124">The plug-in is an in-process server that runs in the default DLL surrogate, dllhost.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ee9b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ee9b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee9b-126">**Informationen zu Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="5ee9b-126">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="5ee9b-127">**Iwmpcontentpartner-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5ee9b-127">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[<span data-ttu-id="5ee9b-128">**Iwmpcontentpartnercallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5ee9b-128">**IWMPContentPartnerCallback Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




