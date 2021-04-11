---
description: Der wbemtimespan-Klassenkonstruktor erstellt ein Zeitspannen Objekt. Der Konstruktor ist überladen.
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: 'Wbemtimespan:: wbemtimespan-Konstruktoren (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: af5724a91ab50b5286e23b3c8095163e415d95e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218477"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a><span data-ttu-id="1d7b5-104">Wbemtimespan:: wbemtimespan-Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="1d7b5-104">WBEMTimeSpan::WbemTimeSpan constructors</span></span>

<span data-ttu-id="1d7b5-105">\[Die [**wbemtimespan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="1d7b5-105">\[The [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1d7b5-106">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="1d7b5-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1d7b5-107">Der **wbemtimespan** -Klassenkonstruktor erstellt ein Zeitspannen Objekt.</span><span class="sxs-lookup"><span data-stu-id="1d7b5-107">The **WBEMTimeSpan** class constructor creates a time span object.</span></span> <span data-ttu-id="1d7b5-108">Der Konstruktor ist überladen.</span><span class="sxs-lookup"><span data-stu-id="1d7b5-108">The constructor is overloaded.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1d7b5-109">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="1d7b5-109">Overload list</span></span>



| <span data-ttu-id="1d7b5-110">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="1d7b5-110">Constructor</span></span>                                                                                                 | <span data-ttu-id="1d7b5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d7b5-111">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="1d7b5-112">[**Wbemtimespan ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="1d7b5-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                                      | <span data-ttu-id="1d7b5-113">Erstellt ein nicht initialisiertes Zeitspannen Objekt.</span><span class="sxs-lookup"><span data-stu-id="1d7b5-113">Creates an uninitialized time span object.</span></span><br/>                        |
| <span data-ttu-id="1d7b5-114">[**Wbemtimespan (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="1d7b5-114">[**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                               | <span data-ttu-id="1d7b5-115">Initialisiert das neue Zeitspannen Objekt, das im-Parameterwert ist.</span><span class="sxs-lookup"><span data-stu-id="1d7b5-115">Initializes the new time span object to value in the parameter.</span></span><br/>   |
| <span data-ttu-id="1d7b5-116">[**Wbemtimespan (int, int, int, int, int, int, int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span><span class="sxs-lookup"><span data-stu-id="1d7b5-116">[**WBEMTimeSpan(int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span></span> | <span data-ttu-id="1d7b5-117">Initialisiert das neue Zeitspannen Objekt auf Werte in den Parametern.</span><span class="sxs-lookup"><span data-stu-id="1d7b5-117">Initializes the new time span object to values in the parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1d7b5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d7b5-118">Requirements</span></span>



| <span data-ttu-id="1d7b5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d7b5-119">Requirement</span></span> | <span data-ttu-id="1d7b5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1d7b5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7b5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d7b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1d7b5-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d7b5-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="1d7b5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d7b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1d7b5-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d7b5-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="1d7b5-125">Header</span><span class="sxs-lookup"><span data-stu-id="1d7b5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d7b5-126"><dt>Wbemtime. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d7b5-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="1d7b5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1d7b5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d7b5-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d7b5-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="1d7b5-129">�</span><span class="sxs-lookup"><span data-stu-id="1d7b5-129">�</span></span>

<span data-ttu-id="1d7b5-130">�</span><span class="sxs-lookup"><span data-stu-id="1d7b5-130">�</span></span>
