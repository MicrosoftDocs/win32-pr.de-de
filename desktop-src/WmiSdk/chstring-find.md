---
description: Mit der Find-Methode wird eine Zeichenfolge nach der ersten Entsprechung einer Teil Zeichenfolge durchsucht.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'Chstring:: Find-Methoden (chstring. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5996ca5c06e2101fad834ce2e37df31ee435fbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351138"
---
# <a name="chstringfind-methods"></a><span data-ttu-id="687b8-103">Chstring:: Find-Methoden</span><span class="sxs-lookup"><span data-stu-id="687b8-103">CHString::Find methods</span></span>

<span data-ttu-id="687b8-104">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="687b8-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="687b8-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="687b8-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="687b8-106">Mit der **Find** -Methode wird eine Zeichenfolge nach der ersten Entsprechung einer Teil Zeichenfolge durchsucht.</span><span class="sxs-lookup"><span data-stu-id="687b8-106">The **Find** method searches a string for the first match of a substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="687b8-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="687b8-107">Overload list</span></span>



| <span data-ttu-id="687b8-108">Methode</span><span class="sxs-lookup"><span data-stu-id="687b8-108">Method</span></span>                                          | <span data-ttu-id="687b8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="687b8-109">Description</span></span>                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| <span data-ttu-id="687b8-110">[**Suchen (WChar)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="687b8-110">[**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span>     | <span data-ttu-id="687b8-111">Sucht in dieser Zeichenfolge nach dem **WSTR** .</span><span class="sxs-lookup"><span data-stu-id="687b8-111">Searches for the **WSTR** in this string.</span></span><br/>    |
| <span data-ttu-id="687b8-112">[**Suchen (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="687b8-112">[**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span> | <span data-ttu-id="687b8-113">Sucht in dieser Zeichenfolge nach **LPCWSTR** .</span><span class="sxs-lookup"><span data-stu-id="687b8-113">Searches for the **LPCWSTR** in this string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="687b8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="687b8-114">Requirements</span></span>



| <span data-ttu-id="687b8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="687b8-115">Requirement</span></span> | <span data-ttu-id="687b8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="687b8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="687b8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="687b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="687b8-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="687b8-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="687b8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="687b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="687b8-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="687b8-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="687b8-121">Header</span><span class="sxs-lookup"><span data-stu-id="687b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="687b8-122"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="687b8-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="687b8-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="687b8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="687b8-124"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="687b8-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="687b8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="687b8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687b8-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="687b8-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="687b8-127">�</span><span class="sxs-lookup"><span data-stu-id="687b8-127">�</span></span>

<span data-ttu-id="687b8-128">�</span><span class="sxs-lookup"><span data-stu-id="687b8-128">�</span></span>
