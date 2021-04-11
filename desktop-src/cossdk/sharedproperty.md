---
description: Legt den Wert einer freigegebenen Eigenschaft fest oder ruft ihn ab.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: SharedProperty-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126578"
---
# <a name="sharedproperty-class"></a><span data-ttu-id="cc15d-103">SharedProperty-Klasse</span><span class="sxs-lookup"><span data-stu-id="cc15d-103">SharedProperty class</span></span>

<span data-ttu-id="cc15d-104">Legt den Wert einer freigegebenen Eigenschaft fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="cc15d-104">Sets or retrieves the value of a shared property.</span></span>

<span data-ttu-id="cc15d-105">Allgemeine Informationen zum Verwenden der freigegebenen Eigenschaften-Manager in com+ finden Sie unter [com+ Shared Eigenschaften-Manager](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="cc15d-105">For general information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="cc15d-106">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="cc15d-106">When to implement</span></span>

<span data-ttu-id="cc15d-107">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="cc15d-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="cc15d-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc15d-108">Requirement</span></span> | <span data-ttu-id="cc15d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cc15d-109">Value</span></span> |
|------------|--------------------------------------------|
| <span data-ttu-id="cc15d-110">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cc15d-110">Interfaces</span></span> | [<span data-ttu-id="cc15d-111">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="cc15d-111">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a><span data-ttu-id="cc15d-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="cc15d-112">When to use</span></span>

<span data-ttu-id="cc15d-113">Verwenden Sie diese Klasse, um auf die Methoden von [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cc15d-113">Use this class to access the methods of [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc15d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc15d-114">Remarks</span></span>

<span data-ttu-id="cc15d-115">Sie können ein **SharedProperty** -Objekt erstellen, indem Sie die Methoden " [**kreateproperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) " oder " [**kreatepropertybyposition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) " von " [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)" verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc15d-115">You can create a **SharedProperty** object by using the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

<span data-ttu-id="cc15d-116">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc15d-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="cc15d-117">Ein SharedProperty-Objekt wird erstellt, indem die [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) -Methode oder die [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) -Methode des [**SharedPropertyGroup**](sharedpropertygroup.md) -Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cc15d-117">A SharedProperty object is created by calling the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of the [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc15d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc15d-118">Requirements</span></span>



| <span data-ttu-id="cc15d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc15d-119">Requirement</span></span> | <span data-ttu-id="cc15d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cc15d-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc15d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc15d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc15d-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc15d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cc15d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc15d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc15d-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc15d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cc15d-125">Header</span><span class="sxs-lookup"><span data-stu-id="cc15d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc15d-126"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cc15d-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc15d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc15d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc15d-128">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="cc15d-128">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[<span data-ttu-id="cc15d-129">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="cc15d-129">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> <dt>

[<span data-ttu-id="cc15d-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="cc15d-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




