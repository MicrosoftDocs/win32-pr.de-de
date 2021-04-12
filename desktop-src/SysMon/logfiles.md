---
title: LogFiles-Objekt (Isysmon.h)
description: Verwenden Sie diese Klasse, um eine Auflistung von einer oder mehreren Protokolldateien zu verwalten, die Leistungsdaten enthalten. Um dieses Objekt abzurufen, rufen Sie Systemmonitor. Logfiles auf.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- Logfiles-Objekt (Sysmon)
- Logfiles-Objekt (Sysmon), beschrieben
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475051"
---
# <a name="logfiles-object"></a><span data-ttu-id="2250d-105">Logfiles-Objekt</span><span class="sxs-lookup"><span data-stu-id="2250d-105">LogFiles object</span></span>

<span data-ttu-id="2250d-106">Verwenden Sie diese Klasse, um eine Auflistung von einer oder mehreren Protokolldateien zu verwalten, die Leistungsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2250d-106">Use this class to manage a collection of one or more log files that contain performance counter data.</span></span>

<span data-ttu-id="2250d-107">Um dieses Objekt abzurufen, rufen Sie [**Systemmonitor. Logfiles**](systemmonitor-logfiles.md)auf.</span><span class="sxs-lookup"><span data-stu-id="2250d-107">To retrieve this object, call [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).</span></span>

## <a name="members"></a><span data-ttu-id="2250d-108">Member</span><span class="sxs-lookup"><span data-stu-id="2250d-108">Members</span></span>

<span data-ttu-id="2250d-109">Das **Logfiles** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2250d-109">The **LogFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="2250d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="2250d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2250d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2250d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2250d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="2250d-112">Methods</span></span>

<span data-ttu-id="2250d-113">Das **Logfiles** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2250d-113">The **LogFiles** object has these methods.</span></span>



| <span data-ttu-id="2250d-114">Methode</span><span class="sxs-lookup"><span data-stu-id="2250d-114">Method</span></span>                                          | <span data-ttu-id="2250d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2250d-115">Description</span></span>                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="2250d-116">**Eren**</span><span class="sxs-lookup"><span data-stu-id="2250d-116">**Add**</span></span>](systemmonitor-logfiles-add.md)       | <span data-ttu-id="2250d-117">Fügt der Auflistung eine [**logfileitem**](logfileitem.md) -Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="2250d-117">Adds a [**LogFileItem**](logfileitem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="2250d-118">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="2250d-118">**Remove**</span></span>](systemmonitor-logfiles-remove.md) | <span data-ttu-id="2250d-119">Entfernt eine [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="2250d-119">Removes a [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2250d-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2250d-120">Properties</span></span>

<span data-ttu-id="2250d-121">Das **Logfiles** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2250d-121">The **LogFiles** object has these properties.</span></span>



| <span data-ttu-id="2250d-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2250d-122">Property</span></span>                                                 | <span data-ttu-id="2250d-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2250d-123">Description</span></span>                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2250d-124">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="2250d-124">**Count**</span></span>](systemmonitor-logfiles-count.md)<br/> | <span data-ttu-id="2250d-125">Ruft die Anzahl der [**logfileitem**](logfileitem.md) -Instanzen in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="2250d-125">Retrieves the number of [**LogFileItem**](logfileitem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="2250d-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="2250d-126">**Item**</span></span>](systemmonitor-logfiles-item.md)<br/>   | <span data-ttu-id="2250d-127">Ruft die angegebene [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="2250d-127">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2250d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2250d-128">Remarks</span></span>

<span data-ttu-id="2250d-129">Legen Sie [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonlogfiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)fest, damit die Leistungsindikatoren von sysmon aus einer Protokolldatei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2250d-129">To have SYSMON display performance counters from a log file, set [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="2250d-130">Nachdem Sie der Auflistung die Protokolldateien hinzugefügt haben, geben Sie mithilfe der [**Zähler**](counters.md) Sammlung die Indikatorendaten an, die Sie aus den Protokolldateien lesen möchten.</span><span class="sxs-lookup"><span data-stu-id="2250d-130">After adding the log files to the collection, use the [**Counters**](counters.md) collection to specify the counters data that you want to read from the log files.</span></span> <span data-ttu-id="2250d-131">Beachten Sie Folgendes: Wenn **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonlogfiles** festgelegt ist, werden die Protokolldateien von sysmon jedes Mal neu erstellt, wenn Sie eine Protokolldatei oder einen Indikatoren zu den jeweiligen Sammlungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2250d-131">Note that if **SystemMonitor.DataSourceType** is set to **DataSourceTypeConstants.sysmonLogFiles**, SYSMON will resample the log files each time you add a log file or counter to their respective collections.</span></span>

<span data-ttu-id="2250d-132">**Vor Windows Vista:** Sie können der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) keine Protokolldateien hinzufügen, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonlogfiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2250d-132">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="2250d-133">Legen Sie zunächst **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonnulldatasource** fest, fügen Sie die Protokolldateien und Leistungsindikatoren hinzu, und legen Sie **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonlogfiles** fest.</span><span class="sxs-lookup"><span data-stu-id="2250d-133">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

<span data-ttu-id="2250d-134">Die Eigenschaften [**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md) und [**Systemmonitor. logviewstoppt**](systemmonitor-logviewstop.md) geben den Bereich der Stichprobenwerte aus den zu Graphen enden Protokolldateien an.</span><span class="sxs-lookup"><span data-stu-id="2250d-134">The [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties specify the range of sampled values from the log files to graph.</span></span> <span data-ttu-id="2250d-135">In sysmon-Diagrammen wird nur eine Ansicht der Daten aus der Protokolldatei angezeigt (in der Diagramm Ansicht wird kein Bildlauf durchführen, wie dies beim Anzeigen der aktuellen Aktivität des Computers der Fall ist).</span><span class="sxs-lookup"><span data-stu-id="2250d-135">SYSMON graphs only one view worth of data from the log file (the graph view does not scroll as it does when graphing the current activity of the computer).</span></span> <span data-ttu-id="2250d-136">Wenn die Stichprobendaten überschreiten, was in einer einzelnen Diagramm Ansicht angezeigt werden kann, komprimiert sysmon die Stichprobendaten (jeder Diagramm Punkt steht für den Durchschnitt mehrerer Stichprobenwerte), damit alle Stichprobendaten aus den Protokolldateien im Diagramm abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="2250d-136">If the sampled data exceeds what can be shown on a single graph view, SYSMON compresses the sampled data (each graphed point represents the average of multiple sampled values) to fit all the sampled data from the log files on the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="2250d-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2250d-137">Requirements</span></span>



| <span data-ttu-id="2250d-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2250d-138">Requirement</span></span> | <span data-ttu-id="2250d-139">Wert</span><span class="sxs-lookup"><span data-stu-id="2250d-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2250d-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2250d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2250d-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2250d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2250d-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2250d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2250d-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2250d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2250d-144">Header</span><span class="sxs-lookup"><span data-stu-id="2250d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2250d-145"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2250d-145"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2250d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2250d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2250d-147"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2250d-147"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





