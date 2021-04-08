---
title: Tasksettings. networksettings (Eigenschaft)
description: Ruft bei der Skripterstellung das Netzwerk Einstellungs Objekt ab, das einen Netzwerk Profil Bezeichner und-Namen enthält, oder legt dieses fest.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Die networksettings-Eigenschaft Taskplaner
- Networksettings-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, networksettings-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740425"
---
# <a name="tasksettingsnetworksettings-property"></a><span data-ttu-id="785cf-106">Tasksettings. networksettings (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="785cf-106">TaskSettings.NetworkSettings property</span></span>

<span data-ttu-id="785cf-107">Ruft bei der Skripterstellung das Netzwerk Einstellungs Objekt ab, das einen Netzwerk Profil Bezeichner und-Namen enthält, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="785cf-107">For scripting, gets or sets the network settings object that contains a network profile identifier and name.</span></span> <span data-ttu-id="785cf-108">Wenn die [**runonlyifnetworkavailable**](tasksettings-runonlyifnetworkavailable.md) -Eigenschaft von [**tasksettings**](tasksettings.md) den Wert **true** hat und in der **networksettings** -Eigenschaft eine Netzwerk-propfile angegeben ist, wird die Aufgabe nur ausgeführt, wenn das angegebene Netzwerk Profil verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="785cf-108">If the [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) property of [**TaskSettings**](tasksettings.md) is **True** and a network propfile is specified in the **NetworkSettings** property, then the task will run only if the specified network profile is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="785cf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="785cf-109">Syntax</span></span>


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a><span data-ttu-id="785cf-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="785cf-110">Property value</span></span>

<span data-ttu-id="785cf-111">Ein [**networksettings**](networksettings.md) -Objekt, das einen Netzwerk Profil Bezeichner und-Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="785cf-111">A [**NetworkSettings**](networksettings.md) object that contains a network profile identifier and name.</span></span>

## <a name="requirements"></a><span data-ttu-id="785cf-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="785cf-112">Requirements</span></span>



| <span data-ttu-id="785cf-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="785cf-113">Requirement</span></span> | <span data-ttu-id="785cf-114">Wert</span><span class="sxs-lookup"><span data-stu-id="785cf-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="785cf-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="785cf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="785cf-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="785cf-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="785cf-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="785cf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="785cf-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="785cf-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="785cf-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="785cf-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="785cf-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="785cf-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="785cf-121">DLL</span><span class="sxs-lookup"><span data-stu-id="785cf-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="785cf-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="785cf-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="785cf-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="785cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785cf-124">**Tasksettings**</span><span class="sxs-lookup"><span data-stu-id="785cf-124">**TaskSettings**</span></span>](tasksettings.md)
</dt> <dt>

[<span data-ttu-id="785cf-125">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="785cf-125">**NetworkSettings**</span></span>](networksettings.md)
</dt> </dl>

 

 





