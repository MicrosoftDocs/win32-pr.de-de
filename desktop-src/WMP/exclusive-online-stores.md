---
title: Exklusive Online Stores
description: Exklusive Online Stores
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player Online Stores, exklusiv
- Online Stores, exklusiv
- Geben Sie 1 Online Stores ein, exklusiv
- Typ 2 Online Stores, exklusiv
- exklusive Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338041"
---
# <a name="exclusive-online-stores"></a><span data-ttu-id="b7dfd-108">Exklusive Online Stores</span><span class="sxs-lookup"><span data-stu-id="b7dfd-108">Exclusive Online Stores</span></span>

<span data-ttu-id="b7dfd-109">Bei Windows Media Player 11 kann eine Anwendung, die das Player-Steuerelement Remote einbettet, einen exklusiven Online Store angeben.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-109">With Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store.</span></span> <span data-ttu-id="b7dfd-110">In diesem Fall ist der Dienst-Selector in Windows-Media Player deaktiviert, und nur der angegebene Onlinespeicher ist für den Benutzer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-110">In that case, the service selector in Windows Media Player is disabled, and only the specified online store is available to the user.</span></span> <span data-ttu-id="b7dfd-111">Außerdem übernimmt Windows Media Player die durch das **Color** -Element des exklusiven Online Store-Dokuments angegebene Farbe.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-111">Also, Windows Media Player adopts the color specified by the **Color** element of the exclusive online store's ServiceInfo document.</span></span>

<span data-ttu-id="b7dfd-112">Um einen exklusiven Online Store anzugeben, muss eine Anwendung exclusiveservice:*keyName* an das Ende der Zeichenfolge anfügen, die von [iwmpremotemediaservices:: getservicetype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-112">To specify an exclusive online store, an application must append ExclusiveService:*keyname* to the end of the string that it returns from [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span></span> <span data-ttu-id="b7dfd-113">Angenommen, Proseware ist der Schlüssel Name, der einem bestimmten Online Store zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-113">For example, suppose Proseware is the key name given to a particular online store.</span></span> <span data-ttu-id="b7dfd-114">Wenn **getservicetype** die Zeichenfolge "Remote exclusiveservice: Proseware" zurückgibt, ist Proseware der einzige Online Shop, der im Remote Embedded Player-Steuerelement verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-114">If **GetServiceType** returns the string "Remote ExclusiveService:Proseware", then Proseware will be the only online store available in the remotely embedded Player control.</span></span>

<span data-ttu-id="b7dfd-115">Eine Anwendung kann Windows Media Player nur dann auf einen exklusiven Online Store beschränken, wenn Windows Media Player nicht bereits ausgeführt wird, wenn die Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-115">An application can limit Windows Media Player to an exclusive online store only if Windows Media Player is not already running when the application is launched.</span></span> <span data-ttu-id="b7dfd-116">Die Anwendung ist dafür verantwortlich, den Benutzer darüber zu informieren, dass Sie Windows Media Player schließen muss, bevor die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-116">It is the application's responsibility to inform the user that he or she must close Windows Media Player before running the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7dfd-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7dfd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7dfd-118">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-118">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b7dfd-119">**Remoting des Windows Media Player-Steuerelements**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-119">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




