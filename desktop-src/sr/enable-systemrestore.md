---
title: Enable-Methode der SystemRestore-Klasse
description: Aktiviert die Überwachung auf einem bestimmten Laufwerk.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Aktivieren der Methoden System Wiederherstellung
- Methoden System Wiederherstellung aktivieren, SystemRestore-Klasse
- System Restore-Klassen System Wiederherstellung, Enable-Methode
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342446"
---
# <a name="enable-method-of-the-systemrestore-class"></a><span data-ttu-id="d78e5-106">Enable-Methode der SystemRestore-Klasse</span><span class="sxs-lookup"><span data-stu-id="d78e5-106">Enable method of the SystemRestore class</span></span>

<span data-ttu-id="d78e5-107">Aktiviert die Überwachung auf einem bestimmten Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="d78e5-107">Enables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="d78e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d78e5-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="d78e5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d78e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d78e5-110">*Laufwerk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d78e5-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d78e5-111">Das zu aktivierende Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="d78e5-111">The drive to be enabled.</span></span> <span data-ttu-id="d78e5-112">Die Laufwerks Zeichenfolge muss die Form "C: \\ " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d78e5-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="d78e5-113">Wenn es sich bei diesem Parameter um das Systemlaufwerk oder eine leere Zeichenfolge ("") handelt, werden alle Laufwerke überwacht.</span><span class="sxs-lookup"><span data-stu-id="d78e5-113">If this parameter is the system drive or an empty string (""), all drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d78e5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d78e5-114">Return value</span></span>

<span data-ttu-id="d78e5-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d78e5-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d78e5-116">Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d78e5-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="d78e5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d78e5-117">Remarks</span></span>

<span data-ttu-id="d78e5-118">Die **enable** -Methode wartet nicht darauf, dass die Überwachung vollständig aktiviert wird, bevor Sie zurückkehrt, da dies einige Zeit in Anspruch nehmen kann.</span><span class="sxs-lookup"><span data-stu-id="d78e5-118">The **Enable** method does not wait for monitoring to be enabled completely before it returns, because this could take a while.</span></span> <span data-ttu-id="d78e5-119">Stattdessen wird sofort nach dem Start des System Wiederherstellungs Dienstanbieter und des Filter Treibers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d78e5-119">Instead, it returns immediately after starting the System Restore service and filter driver.</span></span>

<span data-ttu-id="d78e5-120">Zum Aktivieren der Systemwiederherstellung auf einem nicht-System Laufwerk müssen Sie zuerst die Systemwiederherstellung auf dem Systemlaufwerk aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d78e5-120">To enable System Restore on a non-system drive, you must first enable System Restore on the system drive.</span></span>

<span data-ttu-id="d78e5-121">Diese Methode schlägt im abgesicherten Modus fehl.</span><span class="sxs-lookup"><span data-stu-id="d78e5-121">This method fails in safe mode.</span></span>

## <a name="examples"></a><span data-ttu-id="d78e5-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d78e5-122">Examples</span></span>


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="d78e5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d78e5-123">Requirements</span></span>



| <span data-ttu-id="d78e5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d78e5-124">Requirement</span></span> | <span data-ttu-id="d78e5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d78e5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d78e5-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d78e5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d78e5-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d78e5-127">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d78e5-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d78e5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d78e5-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d78e5-129">None supported</span></span><br/>                                                         |
| <span data-ttu-id="d78e5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="d78e5-130">Namespace</span></span><br/>                | <span data-ttu-id="d78e5-131">\\Standardwert</span><span class="sxs-lookup"><span data-stu-id="d78e5-131">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="d78e5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d78e5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d78e5-133"><dt>SR. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d78e5-133"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d78e5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d78e5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d78e5-135">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="d78e5-135">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





