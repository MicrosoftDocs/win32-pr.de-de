---
description: Sammlungsklasse
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345599"
---
# <a name="collection-object"></a><span data-ttu-id="c0926-103">Collection-Objekt</span><span class="sxs-lookup"><span data-stu-id="c0926-103">Collection object</span></span>

<span data-ttu-id="c0926-104">Sammlungsklasse</span><span class="sxs-lookup"><span data-stu-id="c0926-104">Collection Class</span></span>

## <a name="members"></a><span data-ttu-id="c0926-105">Member</span><span class="sxs-lookup"><span data-stu-id="c0926-105">Members</span></span>

<span data-ttu-id="c0926-106">Das **Sammlungs** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c0926-106">The **Collection** object has these types of members:</span></span>

-   [<span data-ttu-id="c0926-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0926-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0926-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0926-108">Properties</span></span>

<span data-ttu-id="c0926-109">Das **Sammlungs** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c0926-109">The **Collection** object has these properties.</span></span>



| <span data-ttu-id="c0926-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c0926-110">Property</span></span>                                           | <span data-ttu-id="c0926-111">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="c0926-111">Access type</span></span>          | <span data-ttu-id="c0926-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0926-112">Description</span></span>                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="c0926-113">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="c0926-113">**Count**</span></span>](-wia-icollection-count.md)<br/> | <span data-ttu-id="c0926-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0926-114">Read-only</span></span><br/> | <span data-ttu-id="c0926-115">Gibt die Anzahl der Elemente in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="c0926-115">Returns the number of members in the collection</span></span><br/> |
| [<span data-ttu-id="c0926-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0926-116">**Item**</span></span>](-wia-icollection-item.md)<br/>   | <span data-ttu-id="c0926-117">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0926-117">Read-only</span></span><br/> | <span data-ttu-id="c0926-118">Gibt das angegebene Element in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="c0926-118">Returns the specified item in the collection</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="c0926-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0926-119">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="c0926-120">Zugriffs Funktionen für die Erstellung \\</span><span class="sxs-lookup"><span data-stu-id="c0926-120">Creation\\Access Functions</span></span>

<span data-ttu-id="c0926-121">Verwenden Sie eine der folgenden Informationen, um einen Verweis auf das-Objekt abzurufen:</span><span class="sxs-lookup"><span data-stu-id="c0926-121">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="c0926-122">**Getitemsfromui**</span><span class="sxs-lookup"><span data-stu-id="c0926-122">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md)

[<span data-ttu-id="c0926-123">**Children**</span><span class="sxs-lookup"><span data-stu-id="c0926-123">**Children**</span></span>](-wia-iwiadispatchitem-children.md)

[<span data-ttu-id="c0926-124">**Geräte**</span><span class="sxs-lookup"><span data-stu-id="c0926-124">**Devices**</span></span>](-wia-iwia-devices.md)



 

## <a name="requirements"></a><span data-ttu-id="c0926-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0926-125">Requirements</span></span>



| <span data-ttu-id="c0926-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0926-126">Requirement</span></span> | <span data-ttu-id="c0926-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c0926-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0926-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0926-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c0926-129">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0926-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0926-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0926-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c0926-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0926-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c0926-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c0926-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0926-133"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c0926-133"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




