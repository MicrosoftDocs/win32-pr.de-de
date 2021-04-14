---
description: Bindet ein verwaltetes Objekt an eine Anwendungsdomäne. Hierbei handelt es sich um eine isolierte Umgebung, in der Anwendungen ausgeführt werden.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: AppDomainHelper-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523443"
---
# <a name="appdomainhelper-class"></a><span data-ttu-id="d39e1-103">AppDomainHelper-Klasse</span><span class="sxs-lookup"><span data-stu-id="d39e1-103">AppDomainHelper class</span></span>

<span data-ttu-id="d39e1-104">Bindet ein verwaltetes Objekt an eine Anwendungsdomäne. Hierbei handelt es sich um eine isolierte Umgebung, in der Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d39e1-104">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="d39e1-105">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="d39e1-105">When to implement</span></span>

<span data-ttu-id="d39e1-106">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="d39e1-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="d39e1-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d39e1-107">Requirement</span></span> | <span data-ttu-id="d39e1-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d39e1-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="d39e1-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="d39e1-109">CLSID</span></span>      | <span data-ttu-id="d39e1-110">GUID \_ AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="d39e1-110">GUID\_AppDomainHelper</span></span>                                 |
| <span data-ttu-id="d39e1-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="d39e1-111">ProgID</span></span>     | <span data-ttu-id="d39e1-112">L "System. EnterpriseServices. Internal. AppDomainHelper"</span><span class="sxs-lookup"><span data-stu-id="d39e1-112">L"System.EnterpriseServices.Internal.AppDomainHelper"</span></span> |
| <span data-ttu-id="d39e1-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d39e1-113">Interfaces</span></span> | [<span data-ttu-id="d39e1-114">**Iappdomainhelper**</span><span class="sxs-lookup"><span data-stu-id="d39e1-114">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a><span data-ttu-id="d39e1-115">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d39e1-115">When to use</span></span>

<span data-ttu-id="d39e1-116">Verwenden Sie diese Klasse, um auf die Methoden von [**iappdomainhelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d39e1-116">Use this class to access the methods of [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span></span>

## <a name="remarks"></a><span data-ttu-id="d39e1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d39e1-117">Remarks</span></span>

<span data-ttu-id="d39e1-118">Um dieses Objekt zu erstellen, rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="d39e1-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="d39e1-119">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="d39e1-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="d39e1-120">Ein AppDomainHelper-Objekt kann mithilfe von "COMSVCSLIB. AppDomainHelper" als Klassenname deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="d39e1-120">An AppDomainHelper object can be declared using "COMSVCSLib.AppDomainHelper" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="d39e1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d39e1-121">Requirements</span></span>



| <span data-ttu-id="d39e1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d39e1-122">Requirement</span></span> | <span data-ttu-id="d39e1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d39e1-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d39e1-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d39e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d39e1-125">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d39e1-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d39e1-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d39e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d39e1-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d39e1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d39e1-128">Header</span><span class="sxs-lookup"><span data-stu-id="d39e1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d39e1-129"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d39e1-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39e1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d39e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39e1-131">**Iappdomainhelper**</span><span class="sxs-lookup"><span data-stu-id="d39e1-131">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

