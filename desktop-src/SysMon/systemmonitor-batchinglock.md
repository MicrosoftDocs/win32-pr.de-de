---
title: SystemMonitor.Batchinglock-Methode
description: Sperrt den System Monitor, um zu verhindern, dass die Stichprobenentnahme von Daten aus dem neu hinzugefügten Wert oder der neuen Protokolldatei
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Batchinglock-Methode (Sysmon)
- Batchinglock-Methode "sysmon", Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", batchinglock-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339159"
---
# <a name="systemmonitorbatchinglock-method"></a><span data-ttu-id="85d52-106">SystemMonitor.Batchinglock-Methode</span><span class="sxs-lookup"><span data-stu-id="85d52-106">SystemMonitor.BatchingLock method</span></span>

<span data-ttu-id="85d52-107">Sperrt den System Monitor, um zu verhindern, dass die Stichprobenentnahme von Daten aus dem neu hinzugefügten Wert oder der neuen Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="85d52-107">Locks the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d52-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="85d52-108">Syntax</span></span>


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a><span data-ttu-id="85d52-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="85d52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d52-110">*Sperre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d52-110">*lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d52-111">Legen Sie diese Einstellung auf "true" fest, um den System Monitor zu sperren, um zu verhindern, dass Daten aus dem neu hinzugefügten-oder-Protokoll</span><span class="sxs-lookup"><span data-stu-id="85d52-111">Set to True to lock the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span> <span data-ttu-id="85d52-112">Legen Sie auf false fest, um die Sperre zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="85d52-112">Set to False to remove the lock.</span></span>

</dd> <dt>

<span data-ttu-id="85d52-113">*batchreason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d52-113">*batchReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d52-114">Identifiziert die Quelle der Daten, die Sie sperren.</span><span class="sxs-lookup"><span data-stu-id="85d52-114">Identifies the source of the data that you are locking.</span></span> <span data-ttu-id="85d52-115">Verwenden Sie denselben Grund Wert, wenn Sie die Ressource sperren und entsperren.</span><span class="sxs-lookup"><span data-stu-id="85d52-115">Use the same reason value when locking and unlocking the resource.</span></span> <span data-ttu-id="85d52-116">Mögliche Werte finden Sie in der [**sysmonbatchreason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="85d52-116">For possible values, see the [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d52-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85d52-117">Return value</span></span>

<span data-ttu-id="85d52-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="85d52-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d52-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85d52-119">Remarks</span></span>

<span data-ttu-id="85d52-120">Diese Methode muss zweimal aufgerufen werden, um die Quelle zu sperren (true) und einmal, um die Quelle zu entsperren (false).</span><span class="sxs-lookup"><span data-stu-id="85d52-120">You must call this method twice, once to lock the source (True) and once to unlock the source (False).</span></span>

<span data-ttu-id="85d52-121">Sie können nur eine Sperre platzieren.</span><span class="sxs-lookup"><span data-stu-id="85d52-121">You can place only one lock.</span></span> <span data-ttu-id="85d52-122">Wenn Sie z. b. die Sperre für sysmonbatchaddfiles festlegen und dann einen zweiten Anruf mithilfe von sysmonbatchaddcounters durchführen, wird der zweite-Befehl die Sperre entfernt, die durch den ersten-Befehl platziert wird.</span><span class="sxs-lookup"><span data-stu-id="85d52-122">For example, if you set the lock for SysmonBatchAddFiles and then make a second call using SysmonBatchAddCounters as the reason, the second call removes the lock placed by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d52-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85d52-123">Requirements</span></span>



| <span data-ttu-id="85d52-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85d52-124">Requirement</span></span> | <span data-ttu-id="85d52-125">Wert</span><span class="sxs-lookup"><span data-stu-id="85d52-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85d52-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85d52-126">Minimum supported client</span></span><br/> | <span data-ttu-id="85d52-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85d52-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85d52-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85d52-128">Minimum supported server</span></span><br/> | <span data-ttu-id="85d52-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85d52-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85d52-130">DLL</span><span class="sxs-lookup"><span data-stu-id="85d52-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85d52-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="85d52-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85d52-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85d52-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d52-133">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="85d52-133">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





