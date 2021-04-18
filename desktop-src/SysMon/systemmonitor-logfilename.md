---
title: Systemmonitor. LogFileName (Eigenschaft)
description: Ruft den Namen einer Protokolldatei ab, die als Quelle der im System Monitor angezeigten Indikatorenwerte verwendet werden soll, oder legt ihn fest.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- LogFileName-Eigenschaft (Sysmon)
- LogFileName-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", LogFileName (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391935"
---
# <a name="systemmonitorlogfilename-property"></a><span data-ttu-id="6398b-106">Systemmonitor. LogFileName (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6398b-106">SystemMonitor.LogFileName property</span></span>

<span data-ttu-id="6398b-107">Ruft den Namen einer Protokolldatei ab, die als Quelle der im System Monitor angezeigten Indikatorenwerte verwendet werden soll, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="6398b-107">Retrieves or sets the name of a log file to use as the source of counter values displayed in the System Monitor.</span></span>

> [!Note]  
> <span data-ttu-id="6398b-108">Diese Eigenschaft wurde von der [**Logfiles**](systemmonitor-logfiles.md) -Eigenschaft als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="6398b-108">This property has been made obsolete by the [**LogFiles**](systemmonitor-logfiles.md) property.</span></span>

 

<span data-ttu-id="6398b-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6398b-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6398b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6398b-110">Syntax</span></span>


```VB
Property LogFileName As String
```



## <a name="property-value"></a><span data-ttu-id="6398b-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6398b-111">Property value</span></span>

<span data-ttu-id="6398b-112">Der Pfad zur Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="6398b-112">Path to the log file.</span></span> <span data-ttu-id="6398b-113">Sie können einen absoluten, relativen oder UNC-Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="6398b-113">You can specify an absolute, relative, or UNC path.</span></span> <span data-ttu-id="6398b-114">Der Name der Protokolldatei Erweiterung muss ". csv", ". TSV" oder ". BLG" lauten.</span><span class="sxs-lookup"><span data-stu-id="6398b-114">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

## <a name="exceptions"></a><span data-ttu-id="6398b-115">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="6398b-115">Exceptions</span></span>



| <span data-ttu-id="6398b-116">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="6398b-116">Exception type</span></span>                                  | <span data-ttu-id="6398b-117">Bedingung</span><span class="sxs-lookup"><span data-stu-id="6398b-117">Condition</span></span>                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6398b-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="6398b-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="6398b-119">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6398b-119">Unable to find the specified file.</span></span> <span data-ttu-id="6398b-120">Der Err. Number-Wert ist 0xc0000bd1.</span><span class="sxs-lookup"><span data-stu-id="6398b-120">The Err.Number value is 0xC0000BD1.</span></span> |
| <span data-ttu-id="6398b-121">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="6398b-121">**System.ArgumentException**</span></span>                    | <span data-ttu-id="6398b-122">Sie dürfen keine leere Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="6398b-122">You cannot specify an empty string.</span></span>                                    |



 

## <a name="remarks"></a><span data-ttu-id="6398b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6398b-123">Remarks</span></span>

<span data-ttu-id="6398b-124">Diese Eigenschaft gibt den Namen der Protokolldatei aus dem ersten Member der [**Logfiles**](systemmonitor-logfiles.md) -Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="6398b-124">This property returns the log file name from the first member of the [**LogFiles**](systemmonitor-logfiles.md) collection.</span></span>

<span data-ttu-id="6398b-125">Das Festlegen dieser Eigenschaft schlägt fehl, wenn die [**Logfiles**](systemmonitor-logfiles.md) -Auflistung mindestens ein Element enthält.</span><span class="sxs-lookup"><span data-stu-id="6398b-125">Setting this property will fail if the [**LogFiles**](systemmonitor-logfiles.md) collection contains one or more members.</span></span>

<span data-ttu-id="6398b-126">Sie müssen das-Logman.exe Tool oder das MMC-Snap-in "Perfmon. msc" verwenden, um die Protokolldateien zu generieren, die Sie dieser Sammlung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6398b-126">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="6398b-127">Bei Perfmon. msc befinden sich die Leistungs Protokoll Protokolle unter **Leistungsprotokolle und-Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="6398b-127">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="6398b-128">Ausführliche Informationen zur Verwendung von Logman.exe oder Perfmon. msc finden Sie, indem Sie im **Hilfe-und Support Center** nach logman suchen oder die Leistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="6398b-128">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6398b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6398b-129">Requirements</span></span>



| <span data-ttu-id="6398b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6398b-130">Requirement</span></span> | <span data-ttu-id="6398b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6398b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6398b-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6398b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6398b-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6398b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6398b-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6398b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6398b-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6398b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6398b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6398b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6398b-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6398b-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6398b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6398b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6398b-139">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="6398b-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="6398b-140">**Systemmonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="6398b-140">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





