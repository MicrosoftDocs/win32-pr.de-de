---
title: Referenz für Typ 1-Onlineshops
description: Referenz für Typ 1-Onlineshops
ms.assetid: e6f45a50-029e-4347-9b25-10e9e32a56eb
keywords:
- Windows Media Player Online Stores, Referenz
- Online Stores, Referenz
- Typ 1 Online Stores, Referenz
- Referenz für den Typ 1-Onlinespeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475f7dee43f2f6152c3b3ebd0e6090a1efb33a72
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390051"
---
# <a name="reference-for-type-1-online-stores"></a><span data-ttu-id="6321c-107">Referenz für Typ 1-Onlineshops</span><span class="sxs-lookup"><span data-stu-id="6321c-107">Reference for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="6321c-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="6321c-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6321c-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6321c-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6321c-110">Windows Media Player 11 stellt einen Katalog Compiler, ein Objekt und mehrere Schnittstellen bereit, die den Typ 1 Online-Speicher unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6321c-110">Windows Media Player 11 provides a catalog compiler, an object, and several interfaces that support type 1 online stores.</span></span> <span data-ttu-id="6321c-111">In den folgenden Abschnitten werden diese ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6321c-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="6321c-112">`Section`</span><span class="sxs-lookup"><span data-stu-id="6321c-112">Section</span></span>                                                                                    | <span data-ttu-id="6321c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6321c-113">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6321c-114">Katalog Compiler für Typ 1-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="6321c-114">Catalog Compiler for Type 1 Online Stores</span></span>](catalog-compiler-for-type-1-online-stores.md) | <span data-ttu-id="6321c-115">Enthält Referenzmaterial für den Compiler, der von einem Online Shop zum Kompilieren seines musikkatalogs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6321c-115">Provides reference material for the compiler that an online store uses to compile its music catalog.</span></span>                                                                                                                               |
| [<span data-ttu-id="6321c-116">Iwmpcontentcontainer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6321c-116">IWMPContentContainer Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)                                 | <span data-ttu-id="6321c-117">Stellt Referenzseiten für Methoden bereit, die das Plug-in des Online Stores aufruft, um einen Inhalts Container zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6321c-117">Provides reference pages for methods that the online store's plug-in calls to inspect a content container.</span></span> <span data-ttu-id="6321c-118">Ein Inhalts Container stellt einen Satz von Medien Elementen dar, der heruntergeladen oder gekauft werden soll.</span><span class="sxs-lookup"><span data-stu-id="6321c-118">A content container represents a set of media items to be downloaded or purchased.</span></span> <span data-ttu-id="6321c-119">Implementiert von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6321c-119">Implemented by Windows Media Player.</span></span> |
| [<span data-ttu-id="6321c-120">Iwmpcontentcontainerlist-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6321c-120">IWMPContentContainerList Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)                         | <span data-ttu-id="6321c-121">Stellt Referenzseiten für Methoden bereit, die vom Plug-in des Online Stores aufgerufen werden, um eine Liste der Inhalts Container zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6321c-121">Provides reference pages for methods that the online store's plug-in calls to inspect a list of content containers.</span></span> <span data-ttu-id="6321c-122">Implementiert von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6321c-122">Implemented by Windows Media Player.</span></span>                                                                           |
| [<span data-ttu-id="6321c-123">Iwmpcontentpartner-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6321c-123">IWMPContentPartner Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)                                     | <span data-ttu-id="6321c-124">Stellt Referenzseiten für Methoden bereit, die von Windows Media Player aufgerufen werden, um Informationen aus dem Online Shop zu erhalten und den Online Shop über die Aktionen des Benutzers zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="6321c-124">Provides reference pages for methods that Windows Media Player calls to get information from the online store and to notify the online store about the user's actions.</span></span> <span data-ttu-id="6321c-125">Wird vom Plug-in des Online Stores implementiert.</span><span class="sxs-lookup"><span data-stu-id="6321c-125">Implemented by the online store's plug-in.</span></span>                  |
| [<span data-ttu-id="6321c-126">Iwmpcontentpartnercallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6321c-126">IWMPContentPartnerCallback Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)                     | <span data-ttu-id="6321c-127">Stellt Referenzseiten für Methoden bereit, die das Plug-in des Online Stores aufruft, um Windows Media Player über den Abschluss von asynchronen Vorgängen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="6321c-127">Provides reference pages for methods that the online store's plug-in calls to notify Windows Media Player about the completion of asynchronous operations.</span></span> <span data-ttu-id="6321c-128">Implementiert von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6321c-128">Implemented by Windows Media Player.</span></span>                                    |
| [<span data-ttu-id="6321c-129">Externes Objekt für den Typ 1-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="6321c-129">External Object for Type 1 Online Stores</span></span>](external-object-for-type-1-online-stores.md)   | <span data-ttu-id="6321c-130">Stellt Referenzseiten für Eigenschaften, Methoden und Ereignisse bereit, die von Skripts in Webseiten verwendet werden, die vom Online Store bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6321c-130">Provides reference pages for properties, methods, and events used by script in webpages provided by the online store.</span></span>                                                                                                              |
| [<span data-ttu-id="6321c-131">Enumerationen für den Typ 1-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="6321c-131">Enumerations for Type 1 Online Stores</span></span>](enumerations-for-type-1-online-stores.md)         | <span data-ttu-id="6321c-132">Bietet Referenzseiten für die Enumerationen, die bei der Kommunikation zwischen Windows Media Player und dem Online Store-Plug-in verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6321c-132">Provides reference pages for the enumerations used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                               |
| [<span data-ttu-id="6321c-133">Strukturen für Typ 1-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="6321c-133">Structures for Type 1 Online Stores</span></span>](structures-for-type-1-online-stores.md)             | <span data-ttu-id="6321c-134">Bietet Referenzseiten für die Strukturen, die bei der Kommunikation zwischen Windows Media Player und dem Online Store-Plug-in verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6321c-134">Provides reference pages for the structures used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="6321c-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6321c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6321c-136">**Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="6321c-136">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




