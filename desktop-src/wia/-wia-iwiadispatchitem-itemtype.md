---
description: Der Typ dieses Elements. Schreibgeschützt.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Item. ItemType (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351694"
---
# <a name="itemitemtype-property"></a><span data-ttu-id="d7801-104">Item. ItemType (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d7801-104">Item.ItemType property</span></span>

<span data-ttu-id="d7801-105">Der Typ dieses Elements.</span><span class="sxs-lookup"><span data-stu-id="d7801-105">The type of this item.</span></span> <span data-ttu-id="d7801-106">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d7801-106">Read-only.</span></span>

<span data-ttu-id="d7801-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d7801-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7801-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7801-108">Syntax</span></span>


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a><span data-ttu-id="d7801-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d7801-109">Property value</span></span>

<span data-ttu-id="d7801-110">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="d7801-110">The following values are possible:</span></span>



| <span data-ttu-id="d7801-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d7801-111">Value</span></span>  | <span data-ttu-id="d7801-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7801-112">Description</span></span>                                     |
|--------|-------------------------------------------------|
| <span data-ttu-id="d7801-113">device</span><span class="sxs-lookup"><span data-stu-id="d7801-113">device</span></span> | <span data-ttu-id="d7801-114">Das Element ist ein WIA-Hardware Gerät.</span><span class="sxs-lookup"><span data-stu-id="d7801-114">The item is a WIA hardware device.</span></span>              |
| <span data-ttu-id="d7801-115">folder</span><span class="sxs-lookup"><span data-stu-id="d7801-115">folder</span></span> | <span data-ttu-id="d7801-116">Das Element ist ein Ordner, der andere Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="d7801-116">The item is a folder that contains other items.</span></span> |
| <span data-ttu-id="d7801-117">file</span><span class="sxs-lookup"><span data-stu-id="d7801-117">file</span></span>   | <span data-ttu-id="d7801-118">Das Element ist ein Bild oder eine Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="d7801-118">The item is an image or audio file.</span></span>             |
| <span data-ttu-id="d7801-119">Audio</span><span class="sxs-lookup"><span data-stu-id="d7801-119">audio</span></span>  | <span data-ttu-id="d7801-120">Das Element ist ein Audioclip.</span><span class="sxs-lookup"><span data-stu-id="d7801-120">The item is an audio clip.</span></span>                      |
| <span data-ttu-id="d7801-121">image</span><span class="sxs-lookup"><span data-stu-id="d7801-121">image</span></span>  | <span data-ttu-id="d7801-122">Das Element ist ein Bild.</span><span class="sxs-lookup"><span data-stu-id="d7801-122">The item is an image.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="d7801-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7801-123">Remarks</span></span>

<span data-ttu-id="d7801-124">Ein Element kann über mehr als einen Typ verfügen.</span><span class="sxs-lookup"><span data-stu-id="d7801-124">An item can have more than one type.</span></span> <span data-ttu-id="d7801-125">Beispielsweise ist jedes Image sowohl vom Typ "Image" als auch vom Typ "file".</span><span class="sxs-lookup"><span data-stu-id="d7801-125">For example, every image is of both "image" and "file" types.</span></span> <span data-ttu-id="d7801-126">**ItemType** gibt eine Zeichenfolge zurück, die alle gültigen Typen für das Element enthält, getrennt durch Semikolons.</span><span class="sxs-lookup"><span data-stu-id="d7801-126">**ItemType** returns a string that includes all valid types for the item, separated by semicolons.</span></span> <span data-ttu-id="d7801-127">Beispiel: "Image; File".</span><span class="sxs-lookup"><span data-stu-id="d7801-127">For example, "image;file".</span></span> <span data-ttu-id="d7801-128">Diese Zeichenfolge enthält keine Leerzeichen, und am Ende ist kein Semikolon vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d7801-128">There are no spaces in this string, and there is not a semicolon at the end.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7801-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7801-129">Requirements</span></span>



| <span data-ttu-id="d7801-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7801-130">Requirement</span></span> | <span data-ttu-id="d7801-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d7801-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7801-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7801-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d7801-133">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7801-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7801-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7801-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d7801-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7801-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d7801-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d7801-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7801-137"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d7801-137"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




