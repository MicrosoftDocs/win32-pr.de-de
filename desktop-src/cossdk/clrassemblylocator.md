---
description: Ruft Informationen zu einer Assembly ab, wenn verwalteter Code in der .NET Framework Common Language Runtime verwendet wird.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Clrassemblylocator-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860879"
---
# <a name="clrassemblylocator-class"></a><span data-ttu-id="b0e2b-103">Clrassemblylocator-Klasse</span><span class="sxs-lookup"><span data-stu-id="b0e2b-103">ClrAssemblyLocator class</span></span>

<span data-ttu-id="b0e2b-104">Ruft Informationen zu einer Assembly ab, wenn verwalteter Code in der .NET Framework Common Language Runtime verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0e2b-104">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="b0e2b-105">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="b0e2b-105">When to implement</span></span>

<span data-ttu-id="b0e2b-106">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="b0e2b-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="b0e2b-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0e2b-107">Requirement</span></span> | <span data-ttu-id="b0e2b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b0e2b-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="b0e2b-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="b0e2b-109">CLSID</span></span>      | <span data-ttu-id="b0e2b-110">GUID \_ AssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="b0e2b-110">GUID\_AssemblyLocator</span></span>                                 |
| <span data-ttu-id="b0e2b-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="b0e2b-111">ProgID</span></span>     | <span data-ttu-id="b0e2b-112">L "System. EnterpriseServices. Internal. AssemblyLocator"</span><span class="sxs-lookup"><span data-stu-id="b0e2b-112">L"System.EnterpriseServices.Internal.AssemblyLocator"</span></span> |
| <span data-ttu-id="b0e2b-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b0e2b-113">Interfaces</span></span> | [<span data-ttu-id="b0e2b-114">**IAssemblyLocator**</span><span class="sxs-lookup"><span data-stu-id="b0e2b-114">**IAssemblyLocator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a><span data-ttu-id="b0e2b-115">Verwendung</span><span class="sxs-lookup"><span data-stu-id="b0e2b-115">When to use</span></span>

<span data-ttu-id="b0e2b-116">Verwenden Sie diese Klasse, um auf die Methoden von [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b0e2b-116">Use this class to access the methods of [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e2b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0e2b-117">Remarks</span></span>

<span data-ttu-id="b0e2b-118">Um dieses Objekt zu erstellen, rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="b0e2b-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="b0e2b-119">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-Diensttyp Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0e2b-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="b0e2b-120">Ein clrassemblylocator-Objekt kann mithilfe von "COMSVCSLIB. clrassemblylocator" als Klassenname deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="b0e2b-120">A ClrAssemblyLocator object can be declared using "COMSVCSLib.ClrAssemblyLocator" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e2b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0e2b-121">Requirements</span></span>



| <span data-ttu-id="b0e2b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0e2b-122">Requirement</span></span> | <span data-ttu-id="b0e2b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b0e2b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e2b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0e2b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e2b-125">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e2b-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b0e2b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0e2b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e2b-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e2b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b0e2b-128">Header</span><span class="sxs-lookup"><span data-stu-id="b0e2b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e2b-129"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b0e2b-129"><dt>ComSvcs.h</dt></span></span> </dl> |



 

