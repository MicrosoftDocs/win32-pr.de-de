---
description: Die getlocaloffsetfordate-Methode gibt den Offset in Minuten zurück (+ oder &\# 8211;) zwischen GMT und Ortszeit für die im-Argument angegebene Zeit.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Wbemtime:: getlocaloffsetfordate-Methode (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866860"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a><span data-ttu-id="a0464-103">Wbemtime:: getlocaloffsetfordate-Methoden</span><span class="sxs-lookup"><span data-stu-id="a0464-103">WBEMTime::GetLocalOffsetForDate methods</span></span>

<span data-ttu-id="a0464-104">\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="a0464-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="a0464-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="a0464-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="a0464-106">Die **getlocaloffsetfordate** -Methode gibt den Offset in Minuten (+ oder) zwischen GMT und Ortszeit für die im Argument angegebene Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="a0464-106">The **GetLocalOffsetForDate** method returns the offset in minutes (+ or �) between GMT and local time for the time supplied in the argument.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a0464-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="a0464-107">Overload list</span></span>



| <span data-ttu-id="a0464-108">Methode</span><span class="sxs-lookup"><span data-stu-id="a0464-108">Method</span></span>                                                                                           | <span data-ttu-id="a0464-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0464-109">Description</span></span>                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="a0464-110">[**Getlocaloffsetfordate (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="a0464-110">[**GetLocalOffsetForDate(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span></span>         | <span data-ttu-id="a0464-111">Das Argument ist ein Verweis auf eine **Uhrzeit \_ t**.</span><span class="sxs-lookup"><span data-stu-id="a0464-111">Argument is a reference to a **time\_t**.</span></span><br/>  |
| <span data-ttu-id="a0464-112">[**Getlocaloffsetfordate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span><span class="sxs-lookup"><span data-stu-id="a0464-112">[**GetLocalOffsetForDate(FILETIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span></span>     | <span data-ttu-id="a0464-113">Das Argument ist ein Zeiger auf eine **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="a0464-113">Argument is a pointer to a **FILETIME**.</span></span><br/>   |
| [<span data-ttu-id="a0464-114">**Getlocaloffsetfordate (struct TM \* )**</span><span class="sxs-lookup"><span data-stu-id="a0464-114">**GetLocalOffsetForDate(struct tm\*)**</span></span>](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | <span data-ttu-id="a0464-115">Das Argument ist ein Zeiger auf die **TM** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a0464-115">Argument is a pointer to **tm** structure.</span></span><br/> |
| <span data-ttu-id="a0464-116">[**Getlocaloffsetfordate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span><span class="sxs-lookup"><span data-stu-id="a0464-116">[**GetLocalOffsetForDate(SYSTEMTIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span></span> | <span data-ttu-id="a0464-117">Das Argument ist ein Zeiger auf eine **Systemzeit**.</span><span class="sxs-lookup"><span data-stu-id="a0464-117">Argument is a pointer to a **SYSTEMTIME**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a0464-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0464-118">Requirements</span></span>



| <span data-ttu-id="a0464-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0464-119">Requirement</span></span> | <span data-ttu-id="a0464-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a0464-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0464-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0464-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0464-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0464-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a0464-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0464-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0464-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0464-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="a0464-125">Header</span><span class="sxs-lookup"><span data-stu-id="a0464-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0464-126"><dt>Wbemtime. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0464-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="a0464-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a0464-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0464-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0464-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="a0464-129">�</span><span class="sxs-lookup"><span data-stu-id="a0464-129">�</span></span>

<span data-ttu-id="a0464-130">�</span><span class="sxs-lookup"><span data-stu-id="a0464-130">�</span></span>
