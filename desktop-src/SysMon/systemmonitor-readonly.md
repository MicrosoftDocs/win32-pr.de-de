---
title: Systemmonitor. Schreib only (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuer Elements ändern kann, oder legt diesen fest.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Schreibgeschützte Eigenschaft (Sysmon)
- Schreibgeschützte Eigenschaft "sysmon", Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", schreibgeschützte Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956427"
---
# <a name="systemmonitorreadonly-property"></a><span data-ttu-id="1f407-106">Systemmonitor. Schreib only (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f407-106">SystemMonitor.ReadOnly property</span></span>

<span data-ttu-id="1f407-107">Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuer Elements ändern kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="1f407-107">Retrieves or sets a value that determines whether a user can modify the property values of the control.</span></span>

<span data-ttu-id="1f407-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1f407-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f407-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f407-109">Syntax</span></span>


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a><span data-ttu-id="1f407-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1f407-110">Property value</span></span>

<span data-ttu-id="1f407-111">True, wenn der Benutzer die Eigenschaftswerte des Steuer Elements nicht ändern soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="1f407-111">True if you do not want the user to modify the property values of the control; otherwise, false.</span></span> <span data-ttu-id="1f407-112">Der Standardwert ist false. Dies bedeutet, dass Benutzer die Eigenschaftswerte des Steuer Elements ändern können.</span><span class="sxs-lookup"><span data-stu-id="1f407-112">The default value is false, meaning that users can modify the property values of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f407-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f407-113">Remarks</span></span>

<span data-ttu-id="1f407-114">Wenn der Wert dieser Eigenschaft true ist, sind die folgenden Bedingungen wirksam:</span><span class="sxs-lookup"><span data-stu-id="1f407-114">When the value of this property is True, the following conditions are in effect:</span></span>

-   <span data-ttu-id="1f407-115">Der Benutzer kann das Kontextmenü nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f407-115">The user cannot use the context menu.</span></span>
-   <span data-ttu-id="1f407-116">Die folgenden Symbolleisten Schaltflächen sind deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="1f407-116">The following toolbar buttons are disabled:</span></span>
    -   <span data-ttu-id="1f407-117">Neuen Indikatorensatz</span><span class="sxs-lookup"><span data-stu-id="1f407-117">New Counter Set</span></span>
    -   <span data-ttu-id="1f407-118">Aktuellen Vorgang anzeigen</span><span class="sxs-lookup"><span data-stu-id="1f407-118">View Current Activity</span></span>
    -   <span data-ttu-id="1f407-119">Protokolldateidaten anzeigen</span><span class="sxs-lookup"><span data-stu-id="1f407-119">View Log File Data</span></span>
    -   <span data-ttu-id="1f407-120">Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1f407-120">Add</span></span>
    -   <span data-ttu-id="1f407-121">Löschen</span><span class="sxs-lookup"><span data-stu-id="1f407-121">Delete</span></span>
    -   <span data-ttu-id="1f407-122">Leistungsindikatorliste einfügen</span><span class="sxs-lookup"><span data-stu-id="1f407-122">Paste Counter List</span></span>
    -   <span data-ttu-id="1f407-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f407-123">Properties</span></span>

<span data-ttu-id="1f407-124">Beachten Sie, dass sich diese Eigenschaft nur auf die Fähigkeit des Benutzers auswirkt, Eigenschaftswerte über die Benutzeroberfläche zu ändern. es hindert Sie nicht daran, Eigenschaftswerte oder-Indikatoren Programm gesteuert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1f407-124">Note that this property affects only the user's ability to modify property values through the user interface, it does not prevent you from programmatically modifying property values or counters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f407-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f407-125">Requirements</span></span>



| <span data-ttu-id="1f407-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f407-126">Requirement</span></span> | <span data-ttu-id="1f407-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1f407-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f407-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f407-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1f407-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f407-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1f407-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f407-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1f407-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f407-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f407-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1f407-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f407-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1f407-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f407-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f407-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f407-135">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="1f407-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





