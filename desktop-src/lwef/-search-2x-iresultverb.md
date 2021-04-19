---
title: Iresultverb-Schnittstelle (wdssharedidl. h)
description: Macht Verb Eigenschaften verfügbar.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Iresultverb Interface Legacy Windows-Umgebungs Features
- Iresultverb Interface Legacy Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339991"
---
# <a name="iresultverb-interface"></a><span data-ttu-id="1a6a7-105">Iresultverb-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1a6a7-105">IResultVerb interface</span></span>

> [!NOTE]
> <span data-ttu-id="1a6a7-106">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="1a6a7-107">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6a7-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="1a6a7-108">Macht Verb Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-108">Exposes verb properties.</span></span>

## <a name="members"></a><span data-ttu-id="1a6a7-109">Member</span><span class="sxs-lookup"><span data-stu-id="1a6a7-109">Members</span></span>

<span data-ttu-id="1a6a7-110">Die **iresultverb** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-110">The **IResultVerb** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1a6a7-111">**Iresultverb** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1a6a7-111">**IResultVerb** also has these types of members:</span></span>

-   [<span data-ttu-id="1a6a7-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a6a7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a6a7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a6a7-113">Properties</span></span>

<span data-ttu-id="1a6a7-114">Die **iresultverb** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-114">The **IResultVerb** interface has these properties.</span></span>



| <span data-ttu-id="1a6a7-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1a6a7-115">Property</span></span>                                                             | <span data-ttu-id="1a6a7-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1a6a7-116">Access type</span></span>           | <span data-ttu-id="1a6a7-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a6a7-117">Description</span></span>                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a6a7-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="1a6a7-118">**DisplayName**</span></span>](-search-2x-iresultverb-displayname.md)<br/> | <span data-ttu-id="1a6a7-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a6a7-119">Read-only</span></span><br/>  | <span data-ttu-id="1a6a7-120">Diese Eigenschaft gibt einen Zeiger auf den lokalisierten anzeigen Amen für das Verb zurück.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-120">This property returns a pointer to the localized display name for the verb.</span></span> <br/>                           |
| [<span data-ttu-id="1a6a7-121">**Doit**</span><span class="sxs-lookup"><span data-stu-id="1a6a7-121">**DoIt**</span></span>](-search-2x-iresultverb-doit.md)<br/>               | <span data-ttu-id="1a6a7-122">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="1a6a7-122">Write-only</span></span><br/> | <span data-ttu-id="1a6a7-123">Führt das Verb aus.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-123">Executes the verb.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="1a6a7-124">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="1a6a7-124">**Enabled**</span></span>](-search-2x-iresultverb-enabled.md)<br/>         | <span data-ttu-id="1a6a7-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a6a7-125">Read-only</span></span><br/>  | <span data-ttu-id="1a6a7-126">Diese Eigenschaft gibt true zurück, wenn das Verb aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-126">This property returns TRUE if the verb is enabled.</span></span> <br/>                                                    |
| [<span data-ttu-id="1a6a7-127">**HelpText**</span><span class="sxs-lookup"><span data-stu-id="1a6a7-127">**HelpText**</span></span>](-search-2x-iresultverb-helptext.md)<br/>       | <span data-ttu-id="1a6a7-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a6a7-128">Read-only</span></span><br/>  | <span data-ttu-id="1a6a7-129">Diese Eigenschaft gibt einen Zeiger auf die lokalisierte Hilfe Zeichenfolge für das Verb zurück.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-129">This property returns a pointer to the localized help string for the verb.</span></span> <br/>                            |
| [<span data-ttu-id="1a6a7-130">**Symbol**</span><span class="sxs-lookup"><span data-stu-id="1a6a7-130">**Icon**</span></span>](-search-2x-iresultverb-icon.md)<br/>               | <span data-ttu-id="1a6a7-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a6a7-131">Read-only</span></span><br/>  | <span data-ttu-id="1a6a7-132">Diese Eigenschaft gibt einen Zeiger auf das Handle des optionalen Symbols zurück, das dem Verb zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-132">This property returns a pointer to handle of the optional icon associated with the verb.</span></span> <br/>              |
| [<span data-ttu-id="1a6a7-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="1a6a7-133">**Name**</span></span>](-search-2x-iresultverb-name.md)<br/>               | <span data-ttu-id="1a6a7-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a6a7-134">Read-only</span></span><br/>  | <span data-ttu-id="1a6a7-135">Diese Eigenschaft gibt einen Zeiger auf den Kontonamen für das Verb zurück, z. b. "Drucken", "Öffnen" usw.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-135">This property returns a pointer to the cononical name for the verb such as print, open, and so forth.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="1a6a7-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a6a7-136">Remarks</span></span>

<span data-ttu-id="1a6a7-137">Diese Methoden machen Eigenschaften und Aktionen verfügbar, die auf Verben anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="1a6a7-137">These methods expose properties and actions applicable to verbs.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6a7-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a6a7-138">Requirements</span></span>



| <span data-ttu-id="1a6a7-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a6a7-139">Requirement</span></span> | <span data-ttu-id="1a6a7-140">Wert</span><span class="sxs-lookup"><span data-stu-id="1a6a7-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6a7-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a6a7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6a7-142">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a6a7-142">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1a6a7-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a6a7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6a7-144">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a6a7-144">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1a6a7-145">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1a6a7-145">Redistributable</span></span><br/>          | <span data-ttu-id="1a6a7-146">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="1a6a7-146">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="1a6a7-147">Header</span><span class="sxs-lookup"><span data-stu-id="1a6a7-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a6a7-148"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a6a7-148"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

