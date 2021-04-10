---
title: Idschreitefontfallbackbuilder-Schnittstelle
description: Ermöglicht das Erstellen von Unicode-Schriftart-Fall Back-Zuordnungen und das Erstellen eines Schriftart-Fall Back-Objekts aus diesen Zuordnungen.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Idwrite-fontfallbackbuilder-Schnittstelle direkt schreiben
- Direkter Schreibvorgang für idschreitefontfallbackbuilder-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956704"
---
# <a name="idwritefontfallbackbuilder-interface"></a><span data-ttu-id="2fcb7-105">Idschreitefontfallbackbuilder-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2fcb7-105">IDWriteFontFallbackBuilder interface</span></span>

<span data-ttu-id="2fcb7-106">Ermöglicht das Erstellen von Unicode-Schriftart-Fall Back-Zuordnungen und das Erstellen eines Schriftart-Fall Back-Objekts aus diesen Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="2fcb7-106">Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.</span></span>

## <a name="members"></a><span data-ttu-id="2fcb7-107">Member</span><span class="sxs-lookup"><span data-stu-id="2fcb7-107">Members</span></span>

<span data-ttu-id="2fcb7-108">Die **idschreitefontfallbackbuilder** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2fcb7-108">The **IDWriteFontFallbackBuilder** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2fcb7-109">**Idschreitefontfallbackbuilder** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2fcb7-109">**IDWriteFontFallbackBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="2fcb7-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="2fcb7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2fcb7-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="2fcb7-111">Methods</span></span>

<span data-ttu-id="2fcb7-112">Die **idschreitefontfallbackbuilder** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2fcb7-112">The **IDWriteFontFallbackBuilder** interface has these methods.</span></span>



| <span data-ttu-id="2fcb7-113">Methode</span><span class="sxs-lookup"><span data-stu-id="2fcb7-113">Method</span></span>                                                                      | <span data-ttu-id="2fcb7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fcb7-114">Description</span></span>                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fcb7-115">**AddMapping**</span><span class="sxs-lookup"><span data-stu-id="2fcb7-115">**AddMapping**</span></span>](idwritefontfallbackbuilder-addmapping.md)                 | <span data-ttu-id="2fcb7-116">Fügt eine einzelne Zuordnung an die Liste an.</span><span class="sxs-lookup"><span data-stu-id="2fcb7-116">Appends a single mapping to the list.</span></span> <span data-ttu-id="2fcb7-117">Dies wird einmal für jede weitere Zuordnung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2fcb7-117">Call this once for each additional mapping.</span></span><br/> |
| [<span data-ttu-id="2fcb7-118">**Addmappings**</span><span class="sxs-lookup"><span data-stu-id="2fcb7-118">**AddMappings**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | <span data-ttu-id="2fcb7-119">Fügen Sie alle Zuordnungen von einem vorhandenen Schriftart Fall Back Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="2fcb7-119">Add all the mappings from an existing font fallback object.</span></span><br/>                       |
| [<span data-ttu-id="2fcb7-120">**"Kreatefontfallback"**</span><span class="sxs-lookup"><span data-stu-id="2fcb7-120">**CreateFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | <span data-ttu-id="2fcb7-121">Erstellt das fertige Fall Back Objekt aus den hinzugefügten Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="2fcb7-121">Creates the finalized fallback object from the mappings added.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="2fcb7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fcb7-122">Requirements</span></span>



| <span data-ttu-id="2fcb7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fcb7-123">Requirement</span></span> | <span data-ttu-id="2fcb7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2fcb7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcb7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fcb7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcb7-126">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2fcb7-126">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="2fcb7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fcb7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcb7-128">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2fcb7-128">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2fcb7-129">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="2fcb7-129">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2fcb7-130">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="2fcb7-130">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="2fcb7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2fcb7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fcb7-132"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fcb7-132"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2fcb7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcb7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fcb7-134"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcb7-134"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

