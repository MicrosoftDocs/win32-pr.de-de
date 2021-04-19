---
description: Die Anbieter Klasse macht die folgenden Methoden verfügbar.
ms.assetid: AD0BCAC7-6B5C-4BAF-9641-37D315D3E7B1
ms.tgt_platform: multiple
title: Anbieter Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb4d8f5d012b5209519670562a7f735a34e6f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369853"
---
# <a name="provider-methods"></a><span data-ttu-id="47f33-103">Anbieter Methoden</span><span class="sxs-lookup"><span data-stu-id="47f33-103">Provider Methods</span></span>

<span data-ttu-id="47f33-104">\[Die [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider) Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="47f33-104">\[The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="47f33-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="47f33-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="47f33-106">Die [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider) Klasse macht die folgenden Methoden verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47f33-106">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="47f33-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="47f33-107">In this section</span></span>

-   [<span data-ttu-id="47f33-108">**Commit-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-108">**Commit method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-commit)
-   [<span data-ttu-id="47f33-109">**Methode "kreatenewinstance"**</span><span class="sxs-lookup"><span data-stu-id="47f33-109">**CreateNewInstance method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-createnewinstance)
-   <span data-ttu-id="47f33-110">[**Delta einstance-Methode**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="47f33-110">[**DeleteInstance method**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span></span>
-   [<span data-ttu-id="47f33-111">**Enumeraterhaltungen-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-111">**EnumerateInstances method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-enumerateinstances)
-   <span data-ttu-id="47f33-112">[**ExecMethod-Methode**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="47f33-112">[**ExecMethod method**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="47f33-113">**ExecQuery-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-113">**ExecQuery method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-execquery)
-   [<span data-ttu-id="47f33-114">**Flush-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-114">**Flush method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-flush)
-   [<span data-ttu-id="47f33-115">**Getlocalcomputername-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-115">**GetLocalComputerName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalcomputername)
-   [<span data-ttu-id="47f33-116">**Getlocalinstancepath-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-116">**GetLocalInstancePath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalinstancepath)
-   [<span data-ttu-id="47f33-117">**GetNamespace-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-117">**GetNamespace method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getnamespace)
-   <span data-ttu-id="47f33-118">[**GetObject-Methode**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span><span class="sxs-lookup"><span data-stu-id="47f33-118">[**GetObject method**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span></span>
-   [<span data-ttu-id="47f33-119">**GetProviderName-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-119">**GetProviderName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getprovidername)
-   [<span data-ttu-id="47f33-120">**Makelocalpath-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-120">**MakeLocalPath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-makelocalpath)
-   [<span data-ttu-id="47f33-121">**Provider-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-121">**Provider method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-provider)
-   <span data-ttu-id="47f33-122">[**PutInstance-Methode**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span><span class="sxs-lookup"><span data-stu-id="47f33-122">[**PutInstance method**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span></span>
-   [<span data-ttu-id="47f33-123">**Setkreationclassname-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-123">**SetCreationClassName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-setcreationclassname)
-   [<span data-ttu-id="47f33-124">**Validatedeletionflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-124">**ValidateDeletionFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatedeletionflags)
-   [<span data-ttu-id="47f33-125">**Validateenumerationflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-125">**ValidateEnumerationFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateenumerationflags)
-   [<span data-ttu-id="47f33-126">**Validateflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-126">**ValidateFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateflags)
-   [<span data-ttu-id="47f33-127">**Validategetobjflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-127">**ValidateGetObjFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validategetobjflags)
-   [<span data-ttu-id="47f33-128">**Validatemethodflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-128">**ValidateMethodFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatemethodflags)
-   [<span data-ttu-id="47f33-129">**Validateputinstanceflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-129">**ValidatePutInstanceFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateputinstanceflags)
-   [<span data-ttu-id="47f33-130">**Validatequeryflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="47f33-130">**ValidateQueryFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatequeryflags)

 

 
