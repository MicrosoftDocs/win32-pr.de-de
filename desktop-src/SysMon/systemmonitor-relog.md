---
title: Systemmonitor. relog-Methode
description: Protokolliert die Daten des Zählers erneut in einer neuen Datei. Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu verringern.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Relog-Methode (Sysmon)
- Relog-Methode (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", Methode "relog"
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103418"
---
# <a name="systemmonitorrelog-method"></a><span data-ttu-id="77cc6-107">Systemmonitor. relog-Methode</span><span class="sxs-lookup"><span data-stu-id="77cc6-107">SystemMonitor.Relog method</span></span>

<span data-ttu-id="77cc6-108">Protokolliert die Daten des Zählers erneut in einer neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="77cc6-108">Relogs the counter data to a new file.</span></span> <span data-ttu-id="77cc6-109">Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu verringern.</span><span class="sxs-lookup"><span data-stu-id="77cc6-109">You can also use this method to specify a new file type and to reduce the number of samples contained in the log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="77cc6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="77cc6-110">Syntax</span></span>


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="77cc6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="77cc6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77cc6-112">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77cc6-112">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77cc6-113">Dateipfad der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="77cc6-113">File path of the log file.</span></span> <span data-ttu-id="77cc6-114">Sie können den Pfad als absoluten, relativen oder UNC-Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="77cc6-114">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="77cc6-115">Die Namen Erweiterung der Protokolldatei muss entweder ". BLG", ". TSV" oder ". csv" lauten.</span><span class="sxs-lookup"><span data-stu-id="77cc6-115">The log file name extension must be either .blg, .tsv, or .csv.</span></span> <span data-ttu-id="77cc6-116">Wenn ein Ordner im Pfad nicht vorhanden ist, wird er von sysmon erstellt.</span><span class="sxs-lookup"><span data-stu-id="77cc6-116">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="77cc6-117">Wenn die Datei vorhanden ist, wird die Datei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="77cc6-117">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="77cc6-118">Sysmon wendet die Standard-ACLs aus dem übergeordneten Verzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="77cc6-118">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="77cc6-119">*filetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77cc6-119">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77cc6-120">Das Format der in der Protokolldatei gespeicherten Counter-Daten.</span><span class="sxs-lookup"><span data-stu-id="77cc6-120">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="77cc6-121">Sie können entweder [**SysmonFileType.sysmonfileblg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonfilecsv** oder **SysmonFileType.sysmonfiletsv** angeben.</span><span class="sxs-lookup"><span data-stu-id="77cc6-121">You can specify either [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv**, or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> <dt>

<span data-ttu-id="77cc6-122">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77cc6-122">*filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77cc6-123">Anzahl der Abtastungen aus den alten Protokolldateien, die in der neuen Protokolldatei gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77cc6-123">Number of samples from the old log files to save in the new log file.</span></span> <span data-ttu-id="77cc6-124">Geben Sie 1 an, um jedes Beispiel aus den alten Dateien in den neuen Dateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="77cc6-124">Specify 1 to save every sample from the old files to the new files.</span></span> <span data-ttu-id="77cc6-125">Geben Sie 2 an, um eine von allen zwei Beispielen aus der alten Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="77cc6-125">Specify 2 to save one out of every two samples from the old file.</span></span> <span data-ttu-id="77cc6-126">Geben Sie 3 an, um eine von allen drei Beispielen aus der alten Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="77cc6-126">Specify 3 to save one out of every three samples from the old file.</span></span> <span data-ttu-id="77cc6-127">Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="77cc6-127">And so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77cc6-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77cc6-128">Return value</span></span>

<span data-ttu-id="77cc6-129">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="77cc6-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77cc6-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77cc6-130">Remarks</span></span>

<span data-ttu-id="77cc6-131">Diese Methode verwendet die Protokolldateien, die in der [**System Monitor. Logfiles**](systemmonitor-logfiles.md) -Auflistung enthalten sind, um die zählungdaten erneut zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="77cc6-131">This method uses the log files contained in the [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) collection to relog the counter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="77cc6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77cc6-132">Requirements</span></span>



| <span data-ttu-id="77cc6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77cc6-133">Requirement</span></span> | <span data-ttu-id="77cc6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="77cc6-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77cc6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77cc6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="77cc6-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77cc6-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77cc6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77cc6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="77cc6-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77cc6-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77cc6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="77cc6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77cc6-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="77cc6-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77cc6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77cc6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77cc6-142">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="77cc6-142">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="77cc6-143">**Systemmonitor. SaveAs**</span><span class="sxs-lookup"><span data-stu-id="77cc6-143">**SystemMonitor.SaveAs**</span></span>](systemmonitor-saveas.md)
</dt> </dl>

 

 





