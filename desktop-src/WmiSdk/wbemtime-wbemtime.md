---
description: Der wbemtime-Klassenkonstruktor vereinfacht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Wbemtime:: wbemtime-Konstruktoren (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350151"
---
# <a name="wbemtimewbemtime-constructors"></a><span data-ttu-id="0ab67-103">Wbemtime:: wbemtime-Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="0ab67-103">WBEMTime::WBEMTime constructors</span></span>

<span data-ttu-id="0ab67-104">\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="0ab67-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0ab67-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="0ab67-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0ab67-106">Der **wbemtime** -Klassenkonstruktor vereinfacht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten.</span><span class="sxs-lookup"><span data-stu-id="0ab67-106">The **WBEMTime** class constructor facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0ab67-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="0ab67-107">Overload list</span></span>



| <span data-ttu-id="0ab67-108">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="0ab67-108">Constructor</span></span>                                                                 | <span data-ttu-id="0ab67-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ab67-109">Description</span></span>                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span data-ttu-id="0ab67-110">[**Wbemtime ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="0ab67-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                                   | <span data-ttu-id="0ab67-111">Erstellt ein nicht initialisiertes Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="0ab67-111">Creates an uninitialized time object.</span></span><br/>                          |
| <span data-ttu-id="0ab67-112">[**Wbemtime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="0ab67-112">[**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                           | <span data-ttu-id="0ab67-113">Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ab67-113">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="0ab67-114">[**Wbemtime (Konstante Zeit \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="0ab67-114">[**WBEMTime(const time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span></span>        | <span data-ttu-id="0ab67-115">Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ab67-115">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="0ab67-116">[**Wbemtime (Konstante struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span><span class="sxs-lookup"><span data-stu-id="0ab67-116">[**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span></span>    | <span data-ttu-id="0ab67-117">Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ab67-117">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="0ab67-118">[**Wbemtime (Konstante FILETIME-&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="0ab67-118">[**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span></span>     | <span data-ttu-id="0ab67-119">Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ab67-119">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="0ab67-120">[**Wbemtime (konstant Systemzeit&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="0ab67-120">[**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span></span> | <span data-ttu-id="0ab67-121">Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ab67-121">Initializes the new time object to the value in the parameter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0ab67-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ab67-122">Requirements</span></span>



| <span data-ttu-id="0ab67-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ab67-123">Requirement</span></span> | <span data-ttu-id="0ab67-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0ab67-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab67-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ab67-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0ab67-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ab67-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="0ab67-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ab67-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0ab67-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ab67-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="0ab67-129">Header</span><span class="sxs-lookup"><span data-stu-id="0ab67-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ab67-130"><dt>Wbemtime. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab67-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="0ab67-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0ab67-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ab67-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ab67-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="0ab67-133">�</span><span class="sxs-lookup"><span data-stu-id="0ab67-133">�</span></span>

<span data-ttu-id="0ab67-134">�</span><span class="sxs-lookup"><span data-stu-id="0ab67-134">�</span></span>
