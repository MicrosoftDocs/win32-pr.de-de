---
description: 'Die CInstance:: GetWBEMINT64-Methode legt eine 64-Bit-Ganzzahl-Eigenschaft fest.'
audience: developer
ms.assetid: a1789091-ddb6-44f7-bc02-82e7c0209bf9
ms.tgt_platform: multiple
title: 'CInstance:: SetWBEMINT64-Methoden (Instance. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f83e39170125a07f28a25d594ad7203f44750a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960226"
---
# <a name="cinstancesetwbemint64-methods"></a><span data-ttu-id="e6468-103">CInstance:: SetWBEMINT64-Methoden</span><span class="sxs-lookup"><span data-stu-id="e6468-103">CInstance::SetWBEMINT64 methods</span></span>

<span data-ttu-id="e6468-104">\[Die [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="e6468-104">\[The [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="e6468-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="e6468-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="e6468-106">Die [**CInstance:: GetWBEMINT64**](cinstance-getwbemint64.md) -Methode legt eine 64-Bit-Ganzzahl-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e6468-106">The [**CInstance::GetWBEMINT64**](cinstance-getwbemint64.md) method sets a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e6468-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="e6468-107">Overload list</span></span>



| <span data-ttu-id="e6468-108">Methode</span><span class="sxs-lookup"><span data-stu-id="e6468-108">Method</span></span>                                                                                               | <span data-ttu-id="e6468-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6468-109">Description</span></span>                                |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------|
| <span data-ttu-id="e6468-110">[**SetWBEMINT64 (LPCWSTR, Konstanten Longlong-&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span><span class="sxs-lookup"><span data-stu-id="e6468-110">[**SetWBEMINT64(LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span></span>    | <span data-ttu-id="e6468-111">Legt eine 64-Bit-Ganzzahl Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e6468-111">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="e6468-112">[**SetWBEMINT64 (LPCWSTR, konstant WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="e6468-112">[**SetWBEMINT64(LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span> | <span data-ttu-id="e6468-113">Legt eine 64-Bit-Ganzzahl Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e6468-113">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="e6468-114">[**SetWBEMINT64 (LPCWSTR, Konstanten ULONGLONG-&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="e6468-114">[**SetWBEMINT64(LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span>  | <span data-ttu-id="e6468-115">Legt eine 64-Bit-Ganzzahl Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e6468-115">Sets a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e6468-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6468-116">Requirements</span></span>



| <span data-ttu-id="e6468-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6468-117">Requirement</span></span> | <span data-ttu-id="e6468-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e6468-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6468-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6468-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6468-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6468-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e6468-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6468-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6468-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6468-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e6468-123">Header</span><span class="sxs-lookup"><span data-stu-id="e6468-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6468-124"><dt>Instance. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="e6468-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e6468-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e6468-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6468-126"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6468-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="e6468-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e6468-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6468-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6468-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6468-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6468-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6468-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="e6468-130">**CInstance**</span></span>](/windows/win32/api/instance/nl-instance-cinstance)
</dt> </dl>

<span data-ttu-id="e6468-131">�</span><span class="sxs-lookup"><span data-stu-id="e6468-131">�</span></span>

<span data-ttu-id="e6468-132">�</span><span class="sxs-lookup"><span data-stu-id="e6468-132">�</span></span>
