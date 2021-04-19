---
description: Die getemptyinstance-Methode ruft eine einzelne nicht aufgefüllte Instanz der angegebenen Klasse ab.
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: 'Cwbemproviderglue:: getemptyinstance-Methoden (wbemglue. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 853afbf3789969fbfca66d5f9cb40f41eadf7630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345274"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a><span data-ttu-id="99779-103">Cwbemproviderglue:: getemptyinstance-Methoden</span><span class="sxs-lookup"><span data-stu-id="99779-103">CWbemProviderGlue::GetEmptyInstance methods</span></span>

<span data-ttu-id="99779-104">\[Die [**cwbemproviderglue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="99779-104">\[The [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="99779-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="99779-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="99779-106">Die **getemptyinstance** -Methode ruft eine einzelne nicht aufgefüllte Instanz der angegebenen Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="99779-106">The **GetEmptyInstance** method retrieves a single unpopulated instance of the specified class.</span></span>

### <a name="overload-list"></a><span data-ttu-id="99779-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="99779-107">Overload list</span></span>



| <span data-ttu-id="99779-108">Methode</span><span class="sxs-lookup"><span data-stu-id="99779-108">Method</span></span>                                                                                                                                            | <span data-ttu-id="99779-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99779-109">Description</span></span>                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="99779-110">[**Getemptyinstance (LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="99779-110">[**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>                            | <span data-ttu-id="99779-111">Ruft eine einzelne nicht aufgefüllte Instanz der angegebenen Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="99779-111">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |
| <span data-ttu-id="99779-112">[**Getemptyinstance (methodcontext, LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="99779-112">[**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span> | <span data-ttu-id="99779-113">Ruft eine einzelne nicht aufgefüllte Instanz der angegebenen Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="99779-113">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="99779-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99779-114">Requirements</span></span>



| <span data-ttu-id="99779-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99779-115">Requirement</span></span> | <span data-ttu-id="99779-116">Wert</span><span class="sxs-lookup"><span data-stu-id="99779-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99779-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99779-117">Minimum supported client</span></span><br/> | <span data-ttu-id="99779-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99779-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="99779-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99779-119">Minimum supported server</span></span><br/> | <span data-ttu-id="99779-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99779-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="99779-121">Header</span><span class="sxs-lookup"><span data-stu-id="99779-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="99779-122"><dt>Wbemglue. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="99779-122"><dt>WbemGlue.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="99779-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99779-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="99779-124"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99779-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="99779-125">DLL</span><span class="sxs-lookup"><span data-stu-id="99779-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99779-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99779-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="99779-127">�</span><span class="sxs-lookup"><span data-stu-id="99779-127">�</span></span>

<span data-ttu-id="99779-128">�</span><span class="sxs-lookup"><span data-stu-id="99779-128">�</span></span>
