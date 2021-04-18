---
description: 'Der wbemtime-Klassen Subtraktions Operator (&\# 8211;) wurde überladen zu:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Wbemtime:: Operator-Operatoren (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352575"
---
# <a name="wbemtimeoperator--operators"></a><span data-ttu-id="0cb21-103">Wbemtime:: Operator-Operatoren</span><span class="sxs-lookup"><span data-stu-id="0cb21-103">WBEMTime::operator- operators</span></span>

<span data-ttu-id="0cb21-104">\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="0cb21-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0cb21-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="0cb21-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0cb21-106">Der [**wbemtime**](wbemtime.md) -Klassen Subtraktions Operator () wurde überladen zu:</span><span class="sxs-lookup"><span data-stu-id="0cb21-106">The [**WBEMTime**](wbemtime.md) class subtraction operator (�) has been overloaded to:</span></span>

-   <span data-ttu-id="0cb21-107">Subtrahieren Sie eine Zeitspanne von der Zeit eines Objekts, um ein neues Zeit Objekt zu schaffen, das die resultierende Zeit enthält.</span><span class="sxs-lookup"><span data-stu-id="0cb21-107">Subtract a time span from an object's time to produce a new time object that contains the resulting time.</span></span>
-   <span data-ttu-id="0cb21-108">Subtrahieren Sie eine Uhrzeit aus der-Zeit des-Objekts, um ein neues Zeitspannen Objekt zu erhalten, das die Differenz zwischen den beiden vorkommen enthält.</span><span class="sxs-lookup"><span data-stu-id="0cb21-108">Subtract a time from the object's time to produce a new time span object that contains the difference between the two times.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0cb21-109">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="0cb21-109">Overload list</span></span>



| <span data-ttu-id="0cb21-110">Operator</span><span class="sxs-lookup"><span data-stu-id="0cb21-110">Operator</span></span>                                                                         | <span data-ttu-id="0cb21-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cb21-111">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="0cb21-112">**Operator-(wbemtime&)**</span><span class="sxs-lookup"><span data-stu-id="0cb21-112">**operator-(WBEMTime&)**</span></span>](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | <span data-ttu-id="0cb21-113">Subtrahiert eine **wbemtime** von einer **wbemtime**.</span><span class="sxs-lookup"><span data-stu-id="0cb21-113">Subtracts a **WBEMTime** from a **WBEMTime**.</span></span><br/>                         |
| <span data-ttu-id="0cb21-114">[**Operator-(wbemtimespan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span><span class="sxs-lookup"><span data-stu-id="0cb21-114">[**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span></span> | <span data-ttu-id="0cb21-115">Subtrahiert [**wbemtimespan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) von einem **wbemtime**-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0cb21-115">Subtracts a [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) from a **WBEMTime**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0cb21-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cb21-116">Requirements</span></span>



| <span data-ttu-id="0cb21-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cb21-117">Requirement</span></span> | <span data-ttu-id="0cb21-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0cb21-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb21-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cb21-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb21-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cb21-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="0cb21-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cb21-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb21-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cb21-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="0cb21-123">Header</span><span class="sxs-lookup"><span data-stu-id="0cb21-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb21-124"><dt>Wbemtime. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb21-124"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="0cb21-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb21-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb21-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb21-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="0cb21-127">�</span><span class="sxs-lookup"><span data-stu-id="0cb21-127">�</span></span>

<span data-ttu-id="0cb21-128">�</span><span class="sxs-lookup"><span data-stu-id="0cb21-128">�</span></span>
