---
title: Logfiles. Add-Methode
description: Fügt der Auflistung eine Protokolldatei hinzu.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Methode hinzufügen (Sysmon)
- Add-Methode (Sysmon), Logfiles-Klasse
- Logfiles-Klasse sysmon, Methode hinzufügen
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103827"
---
# <a name="logfilesadd-method"></a><span data-ttu-id="de0bc-106">Logfiles. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="de0bc-106">LogFiles.Add method</span></span>

<span data-ttu-id="de0bc-107">Fügt der Auflistung eine Protokolldatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="de0bc-107">Adds a log file to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="de0bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="de0bc-108">Syntax</span></span>


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a><span data-ttu-id="de0bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="de0bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0bc-110">*Pfadname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de0bc-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de0bc-111">Der Pfad zur Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="de0bc-111">Path to the log file.</span></span> <span data-ttu-id="de0bc-112">Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="de0bc-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="de0bc-113">Der Name der Protokolldatei Erweiterung muss ". csv", ". TSV" oder ". BLG" lauten.</span><span class="sxs-lookup"><span data-stu-id="de0bc-113">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de0bc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de0bc-114">Remarks</span></span>

<span data-ttu-id="de0bc-115">Sie müssen das-Logman.exe Tool oder das MMC-Snap-in "Perfmon. msc" verwenden, um die Protokolldateien zu generieren, die Sie dieser Sammlung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="de0bc-115">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="de0bc-116">Bei Perfmon. msc befinden sich die Leistungs Protokoll Protokolle unter **Leistungsprotokolle und-Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="de0bc-116">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="de0bc-117">Ausführliche Informationen zur Verwendung von Logman.exe oder Perfmon. msc finden Sie, indem Sie im **Hilfe-und Support Center** nach logman suchen oder die Leistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="de0bc-117">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

<span data-ttu-id="de0bc-118">**Vor Windows Vista:** Sie können der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) keine Protokolldateien hinzufügen, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonlogfiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="de0bc-118">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="de0bc-119">Legen Sie zunächst **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonnulldatasource** fest, fügen Sie die Protokolldateien und Leistungsindikatoren hinzu, und legen Sie **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonlogfiles** fest.</span><span class="sxs-lookup"><span data-stu-id="de0bc-119">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

## <a name="requirements"></a><span data-ttu-id="de0bc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de0bc-120">Requirements</span></span>



| <span data-ttu-id="de0bc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de0bc-121">Requirement</span></span> | <span data-ttu-id="de0bc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="de0bc-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de0bc-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de0bc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="de0bc-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de0bc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="de0bc-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de0bc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="de0bc-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de0bc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de0bc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="de0bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de0bc-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="de0bc-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0bc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de0bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0bc-130">LogFiles</span><span class="sxs-lookup"><span data-stu-id="de0bc-130">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="de0bc-131">**Logfileitem**</span><span class="sxs-lookup"><span data-stu-id="de0bc-131">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="de0bc-132">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="de0bc-132">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





