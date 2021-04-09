---
description: Erstellt freigegebene Eigenschaften Gruppen und, um Zugriff auf vorhandene freigegebene Eigenschaften Gruppen zu erhalten.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: SharedPropertyGroupManager-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860976"
---
# <a name="sharedpropertygroupmanager-class"></a><span data-ttu-id="acb45-103">SharedPropertyGroupManager-Klasse</span><span class="sxs-lookup"><span data-stu-id="acb45-103">SharedPropertyGroupManager class</span></span>

<span data-ttu-id="acb45-104">Erstellt freigegebene Eigenschaften Gruppen und, um Zugriff auf vorhandene freigegebene Eigenschaften Gruppen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="acb45-104">Creates shared property groups and to obtain access to existing shared property groups.</span></span>

<span data-ttu-id="acb45-105">Weitere Informationen zum Verwenden der freigegebenen Eigenschaften-Manager in com+ finden Sie unter [com+ Shared Eigenschaften-Manager](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="acb45-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="acb45-106">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="acb45-106">When to implement</span></span>

<span data-ttu-id="acb45-107">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="acb45-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="acb45-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acb45-108">Requirement</span></span> | <span data-ttu-id="acb45-109">Wert</span><span class="sxs-lookup"><span data-stu-id="acb45-109">Value</span></span> |
|------------|--------------------------------------------------------------------|
| <span data-ttu-id="acb45-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="acb45-110">CLSID</span></span>      | <span data-ttu-id="acb45-111">CLSID \_ SharedPropertyGroupManager</span><span class="sxs-lookup"><span data-stu-id="acb45-111">CLSID\_SharedPropertyGroupManager</span></span>                                  |
| <span data-ttu-id="acb45-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="acb45-112">ProgID</span></span>     | <span data-ttu-id="acb45-113">L "mtxspm. SharedPropertyGroupManager"</span><span class="sxs-lookup"><span data-stu-id="acb45-113">L"MTxSpm.SharedPropertyGroupManager"</span></span>                               |
| <span data-ttu-id="acb45-114">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="acb45-114">Interfaces</span></span> | [<span data-ttu-id="acb45-115">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="acb45-115">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a><span data-ttu-id="acb45-116">Verwendung</span><span class="sxs-lookup"><span data-stu-id="acb45-116">When to use</span></span>

<span data-ttu-id="acb45-117">Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="acb45-117">Use this class to access the methods of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

## <a name="remarks"></a><span data-ttu-id="acb45-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acb45-118">Remarks</span></span>

<span data-ttu-id="acb45-119">Um dieses Objekt zu erstellen, rufen Sie [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="acb45-119">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="acb45-120">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="acb45-120">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="acb45-121">Ein SharedPropertyGroupManager-Objekt kann mithilfe von "COMSVCSLIB. SharedPropertyGroupManager" als Klassenname deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="acb45-121">A SharedPropertyGroupManager object can be declared using "COMSVCSLib.SharedPropertyGroupManager" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb45-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acb45-122">Requirements</span></span>



| <span data-ttu-id="acb45-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acb45-123">Requirement</span></span> | <span data-ttu-id="acb45-124">Wert</span><span class="sxs-lookup"><span data-stu-id="acb45-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="acb45-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acb45-125">Minimum supported client</span></span><br/> | <span data-ttu-id="acb45-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acb45-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="acb45-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acb45-127">Minimum supported server</span></span><br/> | <span data-ttu-id="acb45-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acb45-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="acb45-129">Header</span><span class="sxs-lookup"><span data-stu-id="acb45-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb45-130"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="acb45-130"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acb45-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acb45-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb45-132">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="acb45-132">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[<span data-ttu-id="acb45-133">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="acb45-133">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="acb45-134">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="acb45-134">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> </dl>

 

 




