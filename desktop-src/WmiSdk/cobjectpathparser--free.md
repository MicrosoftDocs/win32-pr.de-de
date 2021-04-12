---
description: Eine überladene Methode, die den Speicher freigibt, der den Pfad enthält.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'Cobjectpathparser:: Free-Methoden (objpath. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 86494e569f68d8eff8b691c648ec5e221b28b39d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217132"
---
# <a name="cobjectpathparserfree-methods"></a><span data-ttu-id="c1c28-103">Cobjectpathparser:: Free-Methoden</span><span class="sxs-lookup"><span data-stu-id="c1c28-103">CObjectPathParser::Free methods</span></span>

<span data-ttu-id="c1c28-104">\[Die [**cobjectpathparser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="c1c28-104">\[The [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="c1c28-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="c1c28-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="c1c28-106">Eine überladene Methode, die den Speicher freigibt, der den Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="c1c28-106">An overloaded method that releases the memory that contains the path.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c1c28-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="c1c28-107">Overload list</span></span>



| <span data-ttu-id="c1c28-108">Methode</span><span class="sxs-lookup"><span data-stu-id="c1c28-108">Method</span></span>                                                                     | <span data-ttu-id="c1c28-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1c28-109">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c28-110">[**Free (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span><span class="sxs-lookup"><span data-stu-id="c1c28-110">[**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span></span>                     | <span data-ttu-id="c1c28-111">Gibt den Arbeitsspeicher frei, der den nicht analysierten Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="c1c28-111">Releases the memory that contains the unparsed path.</span></span><br/>                      |
| <span data-ttu-id="c1c28-112">[**Free (parametpfad)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span><span class="sxs-lookup"><span data-stu-id="c1c28-112">[**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span></span> | <span data-ttu-id="c1c28-113">Gibt den Arbeitsspeicher frei, der die Struktur mit dem analysierten Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="c1c28-113">Releases the memory that contains the structure that has the parsed path.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c1c28-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1c28-114">Requirements</span></span>



| <span data-ttu-id="c1c28-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1c28-115">Requirement</span></span> | <span data-ttu-id="c1c28-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c1c28-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c28-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1c28-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c28-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1c28-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c1c28-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1c28-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c28-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1c28-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="c1c28-121">Header</span><span class="sxs-lookup"><span data-stu-id="c1c28-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c28-122"><dt>Objpath. h ("objpath. h" einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c1c28-122"><dt>ObjPath.h (include ObjPath.h)</dt></span></span> </dl>                                                      |
| <span data-ttu-id="c1c28-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1c28-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1c28-124"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1c28-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="c1c28-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c28-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c28-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c28-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c28-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1c28-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c28-128">**Cobjectpathparser**</span><span class="sxs-lookup"><span data-stu-id="c1c28-128">**CObjectPathParser**</span></span>](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

<span data-ttu-id="c1c28-129">�</span><span class="sxs-lookup"><span data-stu-id="c1c28-129">�</span></span>

<span data-ttu-id="c1c28-130">�</span><span class="sxs-lookup"><span data-stu-id="c1c28-130">�</span></span>
