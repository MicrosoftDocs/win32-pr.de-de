---
title: Musikkatalog
description: Musikkatalog
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player Online Stores, Musikkataloge
- Online Stores, Musikkataloge
- Typ 1 Online Stores, Musikkataloge
- Windows Media Player Online Stores, Katalog Compiler
- Online Stores, Katalog Compiler
- Typ 1 Online Stores, Katalog Compiler
- Musikkataloge
- Katalog Compiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038526"
---
# <a name="music-catalog"></a><span data-ttu-id="55d59-111">Musikkatalog</span><span class="sxs-lookup"><span data-stu-id="55d59-111">Music Catalog</span></span>

<span data-ttu-id="55d59-112">Ein Onlinespeicher vom Typ 1 erstellt seinen Musikkatalog als Satz von TSV-Dateien (Registerkarten getrennte Werte).</span><span class="sxs-lookup"><span data-stu-id="55d59-112">A type 1 online store creates its music catalog as a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="55d59-113">Der Online Shop verwendet den [Katalog Compiler](catalog-compiler-for-type-1-online-stores.md) von Microsoft, um die TSV-Dateien in einen komprimierten Katalog zu kompilieren, der von Windows Media Player heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="55d59-113">Then the online store uses Microsoft's [catalog compiler](catalog-compiler-for-type-1-online-stores.md) to compile the TSV files into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="55d59-114">Windows Media Player können vollständige Katalogdateien oder Katalog Update Dateien herunterladen.</span><span class="sxs-lookup"><span data-stu-id="55d59-114">Windows Media Player can download full catalog files or catalog update files.</span></span> <span data-ttu-id="55d59-115">Katalog Updates enthalten nur die Katalog Informationen, die seit dem letzten Katalog Update geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="55d59-115">Catalog updates contain only the catalog information that has changed since the last catalog update.</span></span> <span data-ttu-id="55d59-116">Das Inhalts Partner-Plug-in kann feststellen, ob ein vollständiger Katalog oder ein Update heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="55d59-116">It is up to the content partner plug-in to determine whether to download a full catalog or an update.</span></span> <span data-ttu-id="55d59-117">In beiden Fällen wendet Windows Media Player die Änderungen auf den aktuellen Katalog an, wenn eine Benachrichtigung vom Plug-in vorliegt.</span><span class="sxs-lookup"><span data-stu-id="55d59-117">In either case, Windows Media Player applies the changes to the current catalog upon notification from the plug-in.</span></span>

<span data-ttu-id="55d59-118">Wenn für den Online Store ein neuer Katalog vorbereitet wurde, kann das Plug-in den Spieler Benachrichtigen, indem er [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) aufrufen und wmpcnnewcatalogavailable als Wert für den *Typparameter* übergibt.</span><span class="sxs-lookup"><span data-stu-id="55d59-118">If the online store has a new catalog prepared, the plug-in can notify the Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) and passing wmpcnNewCatalogAvailable as the value for the *type* parameter.</span></span>

<span data-ttu-id="55d59-119">Wenn Windows Media Player zum Herunterladen eines Katalogs oder Updates bereit ist, ruft der Player [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)auf.</span><span class="sxs-lookup"><span data-stu-id="55d59-119">When Windows Media Player is ready to download a catalog or update, the Player calls [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> <span data-ttu-id="55d59-120">Diese Methode stellt dem Plug-in Informationen zum aktuellen Katalog zur Verfügung, z. b. die Katalogversion und die Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="55d59-120">This method provides the plug-in with information about the current catalog, such as the catalog version and locale identifier.</span></span> <span data-ttu-id="55d59-121">Das Plug-in antwortet durch Bereitstellen der URL (Uniform Resource Serverlocatorpunkt) des korrekten vollständigen Katalogs oder Updates sowie einer aktualisierten Versionsnummer und Ablaufdatum.</span><span class="sxs-lookup"><span data-stu-id="55d59-121">The plug-in responds by supplying the uniform resource locator (URL) of the correct full catalog or update, as well as an updated version number and expiration date.</span></span> <span data-ttu-id="55d59-122">Windows Media Player fordert regelmäßig Katalog Updates basierend auf den Informationen an, die vom Plug-in in **getcatalogurl** bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="55d59-122">Windows Media Player will periodically request catalog updates based upon the information provided by the plug-in in **GetCatalogURL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55d59-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55d59-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55d59-124">**Informationen zu Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="55d59-124">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="55d59-125">**Katalog Compiler für Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="55d59-125">**Catalog Compiler for Type 1 Online Stores**</span></span>](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="55d59-126">**Iwmpcontentpartner-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="55d59-126">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




