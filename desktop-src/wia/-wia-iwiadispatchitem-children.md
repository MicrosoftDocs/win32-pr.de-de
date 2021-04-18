---
description: Die Children-Eigenschaft des Item-Objekts Ruft eine Auflistung von Element Objekten ab. Die Elemente in dieser Auflistung stellen Elemente dar, die direkt untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind. Schreibgeschützt.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item. Children-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345159"
---
# <a name="itemchildren-property"></a><span data-ttu-id="7b8f0-105">Item. Children-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b8f0-105">Item.Children property</span></span>

<span data-ttu-id="7b8f0-106">Die **Children** -Eigenschaft des [**Item**](-wia-item.md) -Objekts Ruft eine Auflistung von **Element** Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-106">The **Children** property of the [**Item**](-wia-item.md) object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="7b8f0-107">Die Elemente in dieser Auflistung stellen Elemente dar, die direkt untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-107">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <span data-ttu-id="7b8f0-108">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-108">Read-only.</span></span>

<span data-ttu-id="7b8f0-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8f0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b8f0-110">Syntax</span></span>


```JScript
propVal = Item.Children
```



## <a name="property-value"></a><span data-ttu-id="7b8f0-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7b8f0-111">Property value</span></span>

<span data-ttu-id="7b8f0-112">Variable, die die-Objekte empfängt.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-112">Variable that receives the objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b8f0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b8f0-113">Remarks</span></span>

<span data-ttu-id="7b8f0-114">Verwenden Sie diese Eigenschaft, um in der hierarchischen Struktur von [**Element**](-wia-item.md) Objekten, die ein Gerät darstellen, die Ordner und Dateien, die sich auf dem Gerät befinden, zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-114">Use this property to navigate the hierarchical tree of [**Item**](-wia-item.md) objects that represent a device, the folders and the files that reside on the device.</span></span>

<span data-ttu-id="7b8f0-115">Die **Children** -Eigenschaft ist eine Auflistung von [**Item**](-wia-item.md) -Objekten, die sich nur von der Ebene direkt unterhalb dieses **Element** Objekts in der Struktur befindet.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-115">The **Children** property is a collection of [**Item**](-wia-item.md) objects only from the level directly beneath this **Item** object in the tree.</span></span> <span data-ttu-id="7b8f0-116">Verwenden Sie diese Eigenschaft rekursiv, um weitere Ebenen in der Struktur zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-116">To navigate further levels down the tree, use this property recursively.</span></span>

<span data-ttu-id="7b8f0-117">Wenn das Element über keine untergeordneten Elemente verfügt oder keine untergeordneten Elemente enthält, gibt diese Eigenschaft eine leere Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-117">If the item cannot or does not have any child items, this property returns an empty collection.</span></span>

> [!Note]  
> <span data-ttu-id="7b8f0-118">Diese Auflistung ist 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-118">This collection is 0-based.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7b8f0-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b8f0-119">Examples</span></span>

<span data-ttu-id="7b8f0-120">Im folgenden Beispiel wird die Verwendung der **Children** -Eigenschaft zum Abrufen und Auflisten einer Auflistung der untergeordneten Elemente eines Geräts veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-120">The following example demonstrates the use of the **Children** property to retrieve and enumerate a collection of the child items of a device.</span></span> <span data-ttu-id="7b8f0-121">Wenn das Gerät eine digitale Kamera ist, enthält die Sammlung normalerweise Ordner-und Bildelemente.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-121">If the device is a digital camera, the collection typically contains folder and image items.</span></span> <span data-ttu-id="7b8f0-122">Wenn es sich bei dem Gerät um einen Scanner handelt, enthält die Sammlung in der Regel Elemente, die das Scannen von Betten</span><span class="sxs-lookup"><span data-stu-id="7b8f0-122">If the device is a scanner, the collection typically contains items that represent scanning beds.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="7b8f0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b8f0-123">Requirements</span></span>



| <span data-ttu-id="7b8f0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b8f0-124">Requirement</span></span> | <span data-ttu-id="7b8f0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7b8f0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8f0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b8f0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7b8f0-127">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b8f0-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b8f0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b8f0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7b8f0-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b8f0-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7b8f0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7b8f0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b8f0-131"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7b8f0-131"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




