---
description: Die InsertAt-Methode fügt ein Element (oder mehrere Kopien eines Elements) oder alle Elemente eines anderen Arrays an einem angegebenen Index ein.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'Chstringarray:: InsertAt-Methoden (chstrarr. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4047b740778c8d0adf1f2b5981b2f3aac5ba9529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355426"
---
# <a name="chstringarrayinsertat-methods"></a><span data-ttu-id="4fc73-103">Chstringarray:: InsertAt-Methoden</span><span class="sxs-lookup"><span data-stu-id="4fc73-103">CHStringArray::InsertAt methods</span></span>

<span data-ttu-id="4fc73-104">\[Die [**chstringarray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="4fc73-104">\[The [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="4fc73-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="4fc73-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="4fc73-106">Die **InsertAt** -Methode fügt ein Element (oder mehrere Kopien eines Elements) oder alle Elemente eines anderen Arrays an einem angegebenen Index ein.</span><span class="sxs-lookup"><span data-stu-id="4fc73-106">The **InsertAt** method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4fc73-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="4fc73-107">Overload list</span></span>



| <span data-ttu-id="4fc73-108">Methode</span><span class="sxs-lookup"><span data-stu-id="4fc73-108">Method</span></span>                                                                               | <span data-ttu-id="4fc73-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fc73-109">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc73-110">[**InsertAt (int, LPCWSTR, int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4fc73-110">[**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span></span>       | <span data-ttu-id="4fc73-111">Fügt ein oder mehrere Elemente an einem angegebenen Index in ein Array ein.</span><span class="sxs-lookup"><span data-stu-id="4fc73-111">Inserts one or more elements at a specified index in an array.</span></span><br/>                                               |
| <span data-ttu-id="4fc73-112">[**InsertAt (int, chstringarray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="4fc73-112">[**InsertAt(int,CHStringArray\*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span> | <span data-ttu-id="4fc73-113">Fügt alle Elemente eines anderen [**chstringarray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) an einem angegebenen Index in einem Array ein.</span><span class="sxs-lookup"><span data-stu-id="4fc73-113">Inserts all the elements of another [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) at a specified index in an array.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4fc73-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fc73-114">Requirements</span></span>



| <span data-ttu-id="4fc73-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fc73-115">Requirement</span></span> | <span data-ttu-id="4fc73-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4fc73-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc73-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fc73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc73-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fc73-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4fc73-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fc73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc73-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fc73-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4fc73-121">Header</span><span class="sxs-lookup"><span data-stu-id="4fc73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc73-122"><dt>Chstrauarr. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="4fc73-122"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4fc73-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4fc73-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fc73-124"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fc73-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="4fc73-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4fc73-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fc73-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fc73-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc73-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fc73-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc73-128">**Chstringarray**</span><span class="sxs-lookup"><span data-stu-id="4fc73-128">**CHStringArray**</span></span>](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

<span data-ttu-id="4fc73-129">�</span><span class="sxs-lookup"><span data-stu-id="4fc73-129">�</span></span>

<span data-ttu-id="4fc73-130">�</span><span class="sxs-lookup"><span data-stu-id="4fc73-130">�</span></span>
