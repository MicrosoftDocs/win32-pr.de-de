---
description: Die cwbemproviderglue-Klasse stellt die folgenden Methoden zur Verfügung.
ms.assetid: E09290AF-1C2E-458A-811E-5357D470D3DF
ms.tgt_platform: multiple
title: Cwbemproviderglue-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea54ffdeaa6b74cda3b830ea65fdc17f8ffa129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959909"
---
# <a name="cwbemproviderglue-methods"></a><span data-ttu-id="da402-103">Cwbemproviderglue-Methoden</span><span class="sxs-lookup"><span data-stu-id="da402-103">CWbemProviderGlue Methods</span></span>

<span data-ttu-id="da402-104">\[Die [**cwbemproviderglue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="da402-104">\[The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="da402-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="da402-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="da402-106">Die [**cwbemproviderglue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="da402-106">The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="da402-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="da402-107">In this section</span></span>

-   <span data-ttu-id="da402-108">[**Frameworklogindll-Methode**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="da402-108">[**FrameworkLoginDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="da402-109">[**Frameworklogoffdll-Methode**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="da402-109">[**FrameworkLogoffDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="da402-110">[**Getallderivedinhaltungen-Methode**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="da402-110">[**GetAllDerivedInstances method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="da402-111">**Getallderivedinstancesasynch-Methode**</span><span class="sxs-lookup"><span data-stu-id="da402-111">**GetAllDerivedInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstancesasynch)
-   [<span data-ttu-id="da402-112">**Getallinstance-Methode**</span><span class="sxs-lookup"><span data-stu-id="da402-112">**GetAllInstances method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstances)
-   [<span data-ttu-id="da402-113">**Getallinstancesasynch-Methode**</span><span class="sxs-lookup"><span data-stu-id="da402-113">**GetAllInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstancesasynch)
-   <span data-ttu-id="da402-114">[**Getemptyinstance-Methoden**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="da402-114">[**GetEmptyInstance methods**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>
-   <span data-ttu-id="da402-115">[**Getinstancebypath-Methode**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="da402-115">[**GetInstanceByPath method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="da402-116">**Getinstancekeysbypath-Methode**</span><span class="sxs-lookup"><span data-stu-id="da402-116">**GetInstanceKeysByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancekeysbypath)
-   [<span data-ttu-id="da402-117">**Getinstancepropertiesbypath-Methode**</span><span class="sxs-lookup"><span data-stu-id="da402-117">**GetInstancePropertiesByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancepropertiesbypath)
-   <span data-ttu-id="da402-118">[**Getinstancesbyquery-Methode**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="da402-118">[**GetInstancesByQuery method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="da402-119">**Getinstancesbyqueryasynch-Methode**</span><span class="sxs-lookup"><span data-stu-id="da402-119">**GetInstancesByQueryAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyqueryasynch)
-   <span data-ttu-id="da402-120">[**Getnamespaceconnetction-Methode**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="da402-120">[**GetNameSpaceConnection method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span></span>
-   <span data-ttu-id="da402-121">[**IsDerivedFrom-Methode**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="da402-121">[**IsDerivedFrom method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="da402-122">**SetStatus usobject-Methode**</span><span class="sxs-lookup"><span data-stu-id="da402-122">**SetStatusObject method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-setstatusobject)

 

 
