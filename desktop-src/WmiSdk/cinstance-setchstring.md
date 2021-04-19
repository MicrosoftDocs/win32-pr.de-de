---
description: 'Die CInstance:: setchstring-Methode legt eine Zeichen folgen Eigenschaft fest.'
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: 'CInstance:: setchstring-Methoden (Instance. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 187c07b5cf0f867ee838f2f3725d6a82319d4634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362821"
---
# <a name="cinstancesetchstring-methods"></a><span data-ttu-id="b578b-103">CInstance:: setchstring-Methoden</span><span class="sxs-lookup"><span data-stu-id="b578b-103">CInstance::SetCHString methods</span></span>

<span data-ttu-id="b578b-104">\[Die [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="b578b-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b578b-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="b578b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b578b-106">Die **CInstance:: setchstring** -Methode legt eine Zeichen folgen Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b578b-106">The **CInstance::SetCHString** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b578b-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="b578b-107">Overload list</span></span>



| <span data-ttu-id="b578b-108">Methode</span><span class="sxs-lookup"><span data-stu-id="b578b-108">Method</span></span>                                                                                           | <span data-ttu-id="b578b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b578b-109">Description</span></span>                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="b578b-110">[**Setchstring (LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="b578b-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span></span>                   | <span data-ttu-id="b578b-111">Legt eine Zeichen folgen Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b578b-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="b578b-112">[**Setchstring (LPCWSTR, Konstanten chstring-&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span><span class="sxs-lookup"><span data-stu-id="b578b-112">[**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span></span> | <span data-ttu-id="b578b-113">Legt eine Zeichen folgen Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b578b-113">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b578b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b578b-114">Requirements</span></span>



| <span data-ttu-id="b578b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b578b-115">Requirement</span></span> | <span data-ttu-id="b578b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b578b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b578b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b578b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b578b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b578b-118">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b578b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b578b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b578b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b578b-120">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b578b-121">Header</span><span class="sxs-lookup"><span data-stu-id="b578b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b578b-122"><dt>Instance. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="b578b-122"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b578b-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b578b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b578b-124"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b578b-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="b578b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b578b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b578b-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b578b-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b578b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b578b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b578b-128">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="b578b-128">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

