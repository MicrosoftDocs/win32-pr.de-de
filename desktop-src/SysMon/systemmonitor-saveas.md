---
title: Systemmonitor. SaveAs-Methode
description: Speichert die Werte der Werte in der Diagramm Ansicht in einer Protokolldatei.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs-Methode (Sysmon)
- SaveAs-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", SaveAs-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345288"
---
# <a name="systemmonitorsaveas-method"></a><span data-ttu-id="bb2f3-106">Systemmonitor. SaveAs-Methode</span><span class="sxs-lookup"><span data-stu-id="bb2f3-106">SystemMonitor.SaveAs method</span></span>

<span data-ttu-id="bb2f3-107">Speichert die Werte der Werte in der Diagramm Ansicht in einer Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-107">Saves the counter values in the graph view to a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2f3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb2f3-108">Syntax</span></span>


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a><span data-ttu-id="bb2f3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb2f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb2f3-110">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb2f3-110">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2f3-111">Dateipfad der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-111">File path of the log file.</span></span> <span data-ttu-id="bb2f3-112">Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="bb2f3-113">Die Namen Erweiterung der Protokolldatei muss ". TSV" oder ". htm" lauten.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-113">The log file name extension must be either .tsv or .htm.</span></span> <span data-ttu-id="bb2f3-114">Wenn ein Ordner im Pfad nicht vorhanden ist, wird er von sysmon erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-114">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="bb2f3-115">Wenn die Datei vorhanden ist, wird die Datei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-115">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="bb2f3-116">Sysmon wendet die Standard-ACLs aus dem übergeordneten Verzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-116">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="bb2f3-117">*filetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb2f3-117">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2f3-118">Das Format der in der Protokolldatei gespeicherten Counter-Daten.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-118">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="bb2f3-119">Sie können entweder [**SysmonFileType.sysmonfilehtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) oder **SysmonFileType.sysmonfiletsv** angeben.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-119">You can specify either [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb2f3-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb2f3-120">Return value</span></span>

<span data-ttu-id="bb2f3-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bb2f3-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2f3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb2f3-122">Remarks</span></span>

<span data-ttu-id="bb2f3-123">Nur die in der Diagramm Ansicht sichtbaren Zählerdaten werden gespeichert (Informationen zur tatsächlichen Anzahl gespeicherter Datenpunkte finden Sie unter [**Systemmonitor. datapointcount**](systemmonitor-datapointcount.md)).</span><span class="sxs-lookup"><span data-stu-id="bb2f3-123">Only the counter data visible in the graph view is saved (for the actual number of data points saved, see [**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb2f3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb2f3-124">Requirements</span></span>



| <span data-ttu-id="bb2f3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb2f3-125">Requirement</span></span> | <span data-ttu-id="bb2f3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bb2f3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2f3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb2f3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bb2f3-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb2f3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb2f3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb2f3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bb2f3-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb2f3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb2f3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bb2f3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb2f3-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bb2f3-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2f3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb2f3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2f3-134">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="bb2f3-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="bb2f3-135">**Systemmonitor. relog**</span><span class="sxs-lookup"><span data-stu-id="bb2f3-135">**SystemMonitor.Relog**</span></span>](systemmonitor-relog.md)
</dt> </dl>

 

 





