---
title: Inhalts Container
description: Inhalts Container
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player Online Stores, Inhalts Container
- Online Stores, Inhalts Container
- Typ 1 Online Stores, Inhalts Container
- Windows Media Player Online Stores, iwmpcontentcontainer-Schnittstelle
- Online Stores, iwmpcontentcontainer-Schnittstelle
- Typ 1 Online Stores, iwmpcontentcontainer-Schnittstelle
- Windows Media Player, Inhalts Container
- Windows Media Player, iwmpcontentcontainer-Schnittstelle
- Inhalts Container
- Iwmpcontentcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106342120"
---
# <a name="content-containers"></a><span data-ttu-id="a4b2c-113">Inhalts Container</span><span class="sxs-lookup"><span data-stu-id="a4b2c-113">Content Containers</span></span>

<span data-ttu-id="a4b2c-114">In Windows Media Player werden Inhalts Container verwendet, um digitale Medieninhalte in einer Abonnement Download-oder Kauftransaktion darzustellen.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-114">Windows Media Player uses content containers to represent digital media content in a subscription download or purchase transaction.</span></span> <span data-ttu-id="a4b2c-115">Ein Inhalts Container wird durch die **iwmpcontentcontainer** -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-115">A content container is represented by the **IWMPContentContainer** interface.</span></span> <span data-ttu-id="a4b2c-116">Ein Inhalts Container enthält möglicherweise eine Liste verwandter Inhalte, z. b. ein-Album oder einen Satz von nicht verknüpften Inhalts Elementen oder- *Spuren*.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-116">A content container might contain a list of related content, such as an album, or a set of unrelated content items, or *tracks*.</span></span> <span data-ttu-id="a4b2c-117">Sie können die **iwmpcontentcontainer** -Schnittstelle verwenden, um die Spuren des Inhalts Containers aufzulisten und den Preis für jede Spur abzurufen. Sie können auch Informationen zum Inhalts Container selbst abrufen, z. b. die Container-ID, den Typ des Inhalts im Container und den Gesamtpreis für die Spuren im Container (die sich von der Summe der Preise der einzelnen Spuren unterscheiden können, wie bei einem Album Kauf).</span><span class="sxs-lookup"><span data-stu-id="a4b2c-117">You can use the **IWMPContentContainer** interface to enumerate the tracks of the content container and retrieve the price of each track. You can also retrieve information about the content container itself, such as the container ID, the type of content in the container, and the total price for the tracks in the container (which might differ from the sum of the prices of the individual tracks, as in the case of an album purchase).</span></span>

<span data-ttu-id="a4b2c-118">Um einen Mechanismus zum Verpacken mehrerer Inhalts Container in einem einzelnen Objekt bereitzustellen, unterstützt Windows Media Player die **iwmpcontentcontainerlist** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-118">To provide a mechanism for packaging multiple content containers into a single object, Windows Media Player supports the **IWMPContentContainerList** interface.</span></span> <span data-ttu-id="a4b2c-119">**Iwmpcontentcontainerlist** stellt Methoden zum Aufzählen und Abrufen der Inhalts Container in der Liste bereit.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-119">**IWMPContentContainerList** provides methods to enumerate and retrieve the content containers in the list.</span></span> <span data-ttu-id="a4b2c-120">Um zu ermitteln, ob die Inhalts Container Liste einen Kauf oder einen Abonnement Download darstellt, rufen Sie [iwmpcontentcontainerlist:: gettransaktiontype](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) auf, um einen [wmptransaktionstyp](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) -Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-120">To discover whether the content container list represents a purchase or a subscription download, call [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) to retrieve a [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4b2c-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4b2c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4b2c-122">**Informationen zu Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="a4b2c-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a4b2c-123">**Iwmpcontentcontainer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a4b2c-123">**IWMPContentContainer Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[<span data-ttu-id="a4b2c-124">**Iwmpcontentcontainerlist-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a4b2c-124">**IWMPContentContainerList Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




