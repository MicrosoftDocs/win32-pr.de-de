---
title: Restore-Methode der SystemRestore-Klasse
description: Initiiert eine Systemwiederherstellung.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restore Method System Restore
- Restore Method System Restore, SystemRestore-Klasse
- SystemRestore-Klassen System Wiederherstellung, Restore-Methode
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740312"
---
# <a name="restore-method-of-the-systemrestore-class"></a><span data-ttu-id="2f6f5-106">Restore-Methode der SystemRestore-Klasse</span><span class="sxs-lookup"><span data-stu-id="2f6f5-106">Restore method of the SystemRestore class</span></span>

<span data-ttu-id="2f6f5-107">Initiiert eine Systemwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="2f6f5-107">Initiates a system restore.</span></span> <span data-ttu-id="2f6f5-108">Der Aufrufer muss einen Systemneustart erzwingen.</span><span class="sxs-lookup"><span data-stu-id="2f6f5-108">The caller must force a system reboot.</span></span> <span data-ttu-id="2f6f5-109">Die tatsächliche Wiederherstellung erfolgt während des Neustarts.</span><span class="sxs-lookup"><span data-stu-id="2f6f5-109">The actual restoration occurs during the reboot.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f6f5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f6f5-110">Syntax</span></span>


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="2f6f5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f6f5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f6f5-112">*Sequencennummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f6f5-112">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f6f5-113">Die Sequenznummer des Wiederherstellungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="2f6f5-113">The sequence number of the restore point.</span></span> <span data-ttu-id="2f6f5-114">Um die Sequenznummer für einen bestimmten Wiederherstellungspunkt zu ermitteln, zählen Sie alle Wiederherstellungspunkte im System auf.</span><span class="sxs-lookup"><span data-stu-id="2f6f5-114">To determine the sequence number for a specific restore point, enumerate all restore points on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f6f5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f6f5-115">Return value</span></span>

<span data-ttu-id="2f6f5-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f6f5-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2f6f5-117">Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2f6f5-117">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="2f6f5-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f6f5-118">Examples</span></span>


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a><span data-ttu-id="2f6f5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f6f5-119">Requirements</span></span>



| <span data-ttu-id="2f6f5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f6f5-120">Requirement</span></span> | <span data-ttu-id="2f6f5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2f6f5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2f6f5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f6f5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f6f5-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f6f5-123">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2f6f5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f6f5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f6f5-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2f6f5-125">None supported</span></span><br/>                                                         |
| <span data-ttu-id="2f6f5-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f6f5-126">Namespace</span></span><br/>                | <span data-ttu-id="2f6f5-127">\\ \\ Standardwert</span><span class="sxs-lookup"><span data-stu-id="2f6f5-127">Root\\\\Default</span></span><br/>                                                        |
| <span data-ttu-id="2f6f5-128">MOF</span><span class="sxs-lookup"><span data-stu-id="2f6f5-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f6f5-129"><dt>SR. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f6f5-129"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f6f5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f6f5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6f5-131">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="2f6f5-131">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





