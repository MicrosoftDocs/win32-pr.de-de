---
description: Erstellt und greift auf die freigegebenen Eigenschaften in einer freigegebenen Eigenschaften Gruppe zu.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: SharedPropertyGroup-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748169"
---
# <a name="sharedpropertygroup-class"></a><span data-ttu-id="cf9ab-103">SharedPropertyGroup-Klasse</span><span class="sxs-lookup"><span data-stu-id="cf9ab-103">SharedPropertyGroup class</span></span>

<span data-ttu-id="cf9ab-104">Erstellt und greift auf die freigegebenen Eigenschaften in einer freigegebenen Eigenschaften Gruppe zu.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-104">Creates and accesses the shared properties in a shared property group.</span></span>

<span data-ttu-id="cf9ab-105">Weitere Informationen zum Verwenden der freigegebenen Eigenschaften-Manager in com+ finden Sie unter [com+ Shared Eigenschaften-Manager](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ab-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="cf9ab-106">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="cf9ab-106">When to implement</span></span>

<span data-ttu-id="cf9ab-107">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="cf9ab-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf9ab-108">Requirement</span></span> | <span data-ttu-id="cf9ab-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cf9ab-109">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="cf9ab-110">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cf9ab-110">Interfaces</span></span> | [<span data-ttu-id="cf9ab-111">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-111">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a><span data-ttu-id="cf9ab-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="cf9ab-112">When to use</span></span>

<span data-ttu-id="cf9ab-113">Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-113">Use this class to access the methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf9ab-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf9ab-114">Remarks</span></span>

<span data-ttu-id="cf9ab-115">Sie können ein **SharedPropertyGroup** -Objekt mithilfe der Methode " [**kreatepropertygroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) " von [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-115">You can create a **SharedPropertyGroup** object using the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

<span data-ttu-id="cf9ab-116">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="cf9ab-117">Ein SharedPropertyGroup-Objekt wird erstellt, indem die [**createpropertygroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) -Methode des [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) -Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-117">A SharedPropertyGroup object is created by calling the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9ab-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf9ab-118">Requirements</span></span>



| <span data-ttu-id="cf9ab-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf9ab-119">Requirement</span></span> | <span data-ttu-id="cf9ab-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cf9ab-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9ab-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf9ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9ab-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf9ab-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cf9ab-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf9ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9ab-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf9ab-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cf9ab-125">Header</span><span class="sxs-lookup"><span data-stu-id="cf9ab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf9ab-126"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ab-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf9ab-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf9ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9ab-128">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-128">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[<span data-ttu-id="cf9ab-129">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-129">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="cf9ab-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




