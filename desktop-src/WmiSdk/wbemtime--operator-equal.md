---
description: Die wbemtime-Klassen Zuweisungs Operatoren sind überladen, um Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten zu vereinfachen. Die verschiedenen überladenen Signaturen sind unten aufgeführt.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Wbemtime:: Operator =-Operatoren (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349609"
---
# <a name="wbemtimeoperator-operators"></a><span data-ttu-id="cbdc8-104">Wbemtime:: Operator =-Operatoren</span><span class="sxs-lookup"><span data-stu-id="cbdc8-104">WBEMTime::operator= operators</span></span>

<span data-ttu-id="cbdc8-105">\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-105">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="cbdc8-106">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="cbdc8-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="cbdc8-107">Die [**wbemtime**](wbemtime.md) -Klassen Zuweisungs Operatoren sind überladen, um Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-107">The [**WBEMTime**](wbemtime.md) class assignment operators are overloaded to facilitate conversions between various Windows and ANSI C run-time time formats.</span></span> <span data-ttu-id="cbdc8-108">Die verschiedenen überladenen Signaturen sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-108">The various overloaded signatures are listed below.</span></span>

### <a name="overload-list"></a><span data-ttu-id="cbdc8-109">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="cbdc8-109">Overload list</span></span>



| <span data-ttu-id="cbdc8-110">Operator</span><span class="sxs-lookup"><span data-stu-id="cbdc8-110">Operator</span></span>                                                                     | <span data-ttu-id="cbdc8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbdc8-111">Description</span></span>                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span data-ttu-id="cbdc8-112">[**Operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span><span class="sxs-lookup"><span data-stu-id="cbdc8-112">[**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span></span>               | <span data-ttu-id="cbdc8-113">Konvertiert ein **BSTR** -in ein **wbemtime** -Format.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-113">Converts a **BSTR** to **WBEMTime** format.</span></span><br/>         |
| <span data-ttu-id="cbdc8-114">[**Operator = (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="cbdc8-114">[**operator=(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span></span>        | <span data-ttu-id="cbdc8-115">Konvertiert **time \_ t** in das **wbemtime** -Format.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-115">Converts **time\_t** to **WBEMTime** format.</span></span><br/>        |
| <span data-ttu-id="cbdc8-116">[**Operator = (FILETIME-&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="cbdc8-116">[**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>     | <span data-ttu-id="cbdc8-117">Konvertiert **FILETIME** in das **wbemtime** -Format.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-117">Converts **FILETIME** to **WBEMTime** format.</span></span><br/>       |
| <span data-ttu-id="cbdc8-118">[**Operator = (struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span><span class="sxs-lookup"><span data-stu-id="cbdc8-118">[**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span></span>   | <span data-ttu-id="cbdc8-119">Konvertiert eine **TM** -Struktur in das **wbemtime** -Format.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-119">Converts a **tm** structure to **WBEMTime** format.</span></span><br/> |
| <span data-ttu-id="cbdc8-120">[**Operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="cbdc8-120">[**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span></span> | <span data-ttu-id="cbdc8-121">Konvertiert **SYSTEMTIME** in das **wbemtime** -Format.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-121">Converts **SYSTEMTIME** to **WBEMTime** format.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="cbdc8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbdc8-122">Requirements</span></span>



| <span data-ttu-id="cbdc8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbdc8-123">Requirement</span></span> | <span data-ttu-id="cbdc8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cbdc8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdc8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbdc8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cbdc8-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbdc8-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="cbdc8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbdc8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cbdc8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbdc8-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="cbdc8-129">Header</span><span class="sxs-lookup"><span data-stu-id="cbdc8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbdc8-130"><dt>Wbemtime. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc8-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="cbdc8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cbdc8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbdc8-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc8-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="cbdc8-133">�</span><span class="sxs-lookup"><span data-stu-id="cbdc8-133">�</span></span>

<span data-ttu-id="cbdc8-134">�</span><span class="sxs-lookup"><span data-stu-id="cbdc8-134">�</span></span>
