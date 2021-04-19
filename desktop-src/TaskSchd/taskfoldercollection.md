---
title: Taskfoldercollection-Objekt
description: Skript Objekt, das Informationen und Steuerelemente für eine Sammlung von Ordnern bereitstellt, die Tasks enthalten.
ms.assetid: 773d1c86-a539-478d-9e71-dc5b86c098c1
keywords:
- Taskfoldercollection-Objekt Taskplaner
- Taskfoldercollection-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskFolderCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c861322d6868ca7ec9ef861e2c3ea30f624db8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344698"
---
# <a name="taskfoldercollection-object"></a><span data-ttu-id="726ac-105">Taskfoldercollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="726ac-105">TaskFolderCollection object</span></span>

<span data-ttu-id="726ac-106">Skript Objekt, das Informationen und Steuerelemente für eine Sammlung von Ordnern bereitstellt, die Tasks enthalten.</span><span class="sxs-lookup"><span data-stu-id="726ac-106">Scripting object that provides information and control for a collection of folders that contain tasks.</span></span>

## <a name="members"></a><span data-ttu-id="726ac-107">Member</span><span class="sxs-lookup"><span data-stu-id="726ac-107">Members</span></span>

<span data-ttu-id="726ac-108">Das **taskfoldercollection** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="726ac-108">The **TaskFolderCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="726ac-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="726ac-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="726ac-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="726ac-110">Properties</span></span>

<span data-ttu-id="726ac-111">Das **taskfoldercollection** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="726ac-111">The **TaskFolderCollection** object has these properties.</span></span>



| <span data-ttu-id="726ac-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="726ac-112">Property</span></span>                                               | <span data-ttu-id="726ac-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="726ac-113">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="726ac-114">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="726ac-114">**Count**</span></span>](taskfoldercollection-count.md)<br/> | <span data-ttu-id="726ac-115">Ruft die Anzahl der Ordner in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="726ac-115">Gets the number of folders in the collection.</span></span><br/>   |
| [<span data-ttu-id="726ac-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="726ac-116">**Item**</span></span>](taskfoldercollection-item.md)<br/>   | <span data-ttu-id="726ac-117">Ruft den angegebenen Ordner aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="726ac-117">Gets the specified folder from the collection.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="726ac-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="726ac-118">Requirements</span></span>



| <span data-ttu-id="726ac-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="726ac-119">Requirement</span></span> | <span data-ttu-id="726ac-120">Wert</span><span class="sxs-lookup"><span data-stu-id="726ac-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="726ac-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="726ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="726ac-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="726ac-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="726ac-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="726ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="726ac-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="726ac-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="726ac-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="726ac-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="726ac-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="726ac-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="726ac-127">DLL</span><span class="sxs-lookup"><span data-stu-id="726ac-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="726ac-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="726ac-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726ac-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="726ac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726ac-130">**Taskfolder. GetFolders**</span><span class="sxs-lookup"><span data-stu-id="726ac-130">**TaskFolder.GetFolders**</span></span>](taskfolder-getfolders.md)
</dt> </dl>

 

 





