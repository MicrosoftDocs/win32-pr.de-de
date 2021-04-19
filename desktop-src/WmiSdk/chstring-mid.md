---
description: Die Mid-Methode extrahiert eine Teil Zeichenfolge der Länge nCount-Zeichen aus einer Zeichenfolge Zeichenfolge, beginnend an der Position nfirst (null basiert). Die-Methode gibt eine Kopie der extrahierten Teil Zeichenfolge zurück.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'Chstring:: Mid-Methoden (chstring. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349915"
---
# <a name="chstringmid-methods"></a><span data-ttu-id="97ef6-104">Chstring:: Mid-Methoden</span><span class="sxs-lookup"><span data-stu-id="97ef6-104">CHString::Mid methods</span></span>

<span data-ttu-id="97ef6-105">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="97ef6-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="97ef6-106">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="97ef6-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="97ef6-107">Die **Mid** -Methode extrahiert eine Teil Zeichenfolge der Länge *nCount* -Zeichen [**aus einer Zeichenfolge Zeichenfolge**](chstring.md) , beginnend an der Position *nfirst* (null basiert).</span><span class="sxs-lookup"><span data-stu-id="97ef6-107">The **Mid** method extracts a substring of length *nCount* characters from a [**CHString**](chstring.md) string, starting at position *nFirst* (zero-based).</span></span> <span data-ttu-id="97ef6-108">Die-Methode gibt eine Kopie der extrahierten Teil Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="97ef6-108">The method returns a copy of the extracted substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="97ef6-109">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="97ef6-109">Overload list</span></span>



| <span data-ttu-id="97ef6-110">Methode</span><span class="sxs-lookup"><span data-stu-id="97ef6-110">Method</span></span>                                        | <span data-ttu-id="97ef6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97ef6-111">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="97ef6-112">[**Mid (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span><span class="sxs-lookup"><span data-stu-id="97ef6-112">[**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span></span> | <span data-ttu-id="97ef6-113">Extrahiert eine Teil Zeichenfolge mit der angegebenen Länge und dem angegebenen Anfangspunkt.</span><span class="sxs-lookup"><span data-stu-id="97ef6-113">Extracts a substring of specified length and beginning point.</span></span><br/> |
| <span data-ttu-id="97ef6-114">[**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="97ef6-114">[**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>         | <span data-ttu-id="97ef6-115">Extrahiert eine Teil Zeichenfolge, beginnend bei int.</span><span class="sxs-lookup"><span data-stu-id="97ef6-115">Extracts a substring beginning at int.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="97ef6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97ef6-116">Requirements</span></span>



| <span data-ttu-id="97ef6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97ef6-117">Requirement</span></span> | <span data-ttu-id="97ef6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="97ef6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ef6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97ef6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="97ef6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97ef6-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="97ef6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97ef6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="97ef6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97ef6-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="97ef6-123">Header</span><span class="sxs-lookup"><span data-stu-id="97ef6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ef6-124"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="97ef6-124"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="97ef6-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97ef6-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="97ef6-126"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97ef6-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="97ef6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="97ef6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97ef6-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97ef6-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="97ef6-129">�</span><span class="sxs-lookup"><span data-stu-id="97ef6-129">�</span></span>

<span data-ttu-id="97ef6-130">�</span><span class="sxs-lookup"><span data-stu-id="97ef6-130">�</span></span>
