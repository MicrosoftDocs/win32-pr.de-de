---
description: Die Format-Methode formatiert und speichert eine Reihe von Zeichen und Werten in einer Zeichen folgen Zeichenfolge.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'Chstring:: Format-Methoden (chstring. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7187d2c691c6efb2054d766ae432c55be893cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362522"
---
# <a name="chstringformat-methods"></a><span data-ttu-id="59edb-103">Chstring:: Format-Methoden</span><span class="sxs-lookup"><span data-stu-id="59edb-103">CHString::Format methods</span></span>

<span data-ttu-id="59edb-104">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="59edb-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="59edb-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="59edb-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="59edb-106">Die **Format** -Methode formatiert und speichert eine Reihe von Zeichen und Werten in einer Zeichen [**folgen Zeichenfolge.**](chstring.md)</span><span class="sxs-lookup"><span data-stu-id="59edb-106">The **Format** method formats and stores a series of characters and values in a [**CHString**](chstring.md) string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="59edb-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="59edb-107">Overload list</span></span>



| <span data-ttu-id="59edb-108">Methode</span><span class="sxs-lookup"><span data-stu-id="59edb-108">Method</span></span>                                              | <span data-ttu-id="59edb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59edb-109">Description</span></span>                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59edb-110">[**Format (uint)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59edb-110">[**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span></span>       | <span data-ttu-id="59edb-111">Formatiert diese Zeichenfolge gemäß dem Ressourcen Bezeichner, der vom **uint** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="59edb-111">Formats this CHString according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="59edb-112">[**Format (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="59edb-112">[**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span></span> | <span data-ttu-id="59edb-113">Formatiert diese Zeichenfolge gemäß dem von **LPCWSTR** angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="59edb-113">Formats this CHString according to the format specified by the **LPCWSTR**.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="59edb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59edb-114">Requirements</span></span>



| <span data-ttu-id="59edb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59edb-115">Requirement</span></span> | <span data-ttu-id="59edb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="59edb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59edb-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59edb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59edb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59edb-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="59edb-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59edb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59edb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59edb-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="59edb-121">Header</span><span class="sxs-lookup"><span data-stu-id="59edb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="59edb-122"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="59edb-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="59edb-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59edb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="59edb-124"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59edb-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="59edb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="59edb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59edb-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59edb-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="59edb-127">�</span><span class="sxs-lookup"><span data-stu-id="59edb-127">�</span></span>

<span data-ttu-id="59edb-128">�</span><span class="sxs-lookup"><span data-stu-id="59edb-128">�</span></span>
