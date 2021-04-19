---
title: Session.Batchitems-Eigenschaft (WSManDisp. h)
description: Legt die Anzahl der Elemente in jedem enumerationsbatch fest und ruft Sie ab.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Batchitems-Eigenschaft Windows-Remoteverwaltung
- Batchitems-Eigenschaft Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, batchitems (Eigenschaft)
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342651"
---
# <a name="sessionbatchitems-property"></a><span data-ttu-id="73181-106">Session.Batchitems (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73181-106">Session.BatchItems property</span></span>

<span data-ttu-id="73181-107">Legt die Anzahl der Elemente in jedem enumerationsbatch fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="73181-107">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="73181-108">Dieser Wert kann während einer Enumeration nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="73181-108">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="73181-109">Der Ressourcenanbieter kann ein Limit festlegen.</span><span class="sxs-lookup"><span data-stu-id="73181-109">The resource provider may set a limit.</span></span>

<span data-ttu-id="73181-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="73181-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73181-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="73181-111">Syntax</span></span>


```VB
Session.BatchItems As long
```



## <a name="property-value"></a><span data-ttu-id="73181-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="73181-112">Property value</span></span>

<span data-ttu-id="73181-113">Gibt die maximale Anzahl von Elementen an, die für die einzelnen zugrunde liegenden Netzwerk Aufrufe an den Dienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73181-113">Specifies the maximum number of elements returned for each underlying network call to the service.</span></span> <span data-ttu-id="73181-114">Der Standardwert ist 20.</span><span class="sxs-lookup"><span data-stu-id="73181-114">The default is 20.</span></span>

## <a name="remarks"></a><span data-ttu-id="73181-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73181-115">Remarks</span></span>

<span data-ttu-id="73181-116">Dies ist ein Optimierungs Feature, das steuert, wie oft Netzwerk Aufrufe zwischen dem Client und dem Server durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="73181-116">This is an optimization feature that controls how often network calls are made between the client and the server.</span></span> <span data-ttu-id="73181-117">Derzeit wird Sie nur für Enumerationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="73181-117">Currently, it is used only for enumerations.</span></span> <span data-ttu-id="73181-118">Weitere Informationen zum Auflisten von Ressourcen finden Sie unter [**Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="73181-118">For more information about enumerating resources, see [**Enumerate**](session-enumerate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73181-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73181-119">Requirements</span></span>



| <span data-ttu-id="73181-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73181-120">Requirement</span></span> | <span data-ttu-id="73181-121">Wert</span><span class="sxs-lookup"><span data-stu-id="73181-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73181-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73181-122">Minimum supported client</span></span><br/> | <span data-ttu-id="73181-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73181-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="73181-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73181-124">Minimum supported server</span></span><br/> | <span data-ttu-id="73181-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73181-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="73181-126">Header</span><span class="sxs-lookup"><span data-stu-id="73181-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="73181-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="73181-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="73181-128">IDL</span><span class="sxs-lookup"><span data-stu-id="73181-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73181-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73181-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="73181-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73181-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="73181-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73181-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73181-132">DLL</span><span class="sxs-lookup"><span data-stu-id="73181-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73181-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73181-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73181-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73181-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73181-135">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="73181-135">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="73181-136">**Aufzählen**</span><span class="sxs-lookup"><span data-stu-id="73181-136">**Enumerate**</span></span>](session-enumerate.md)
</dt> <dt>

[<span data-ttu-id="73181-137">**Enumerator. ReadItem**</span><span class="sxs-lookup"><span data-stu-id="73181-137">**Enumerator.ReadItem**</span></span>](enumerator-readitem.md)
</dt> </dl>

 

 





