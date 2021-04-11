---
title: Deaktivieren der Methode der SystemRestore-Klasse
description: Deaktiviert die Überwachung auf einem bestimmten Laufwerk.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Wiederherstellung des Methoden Systems deaktivieren
- Methoden System Wiederherstellung deaktivieren, SystemRestore-Klasse
- SystemRestore-Klassen System Wiederherstellung, Methode deaktivieren
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104061"
---
# <a name="disable-method-of-the-systemrestore-class"></a><span data-ttu-id="ded03-106">Deaktivieren der Methode der SystemRestore-Klasse</span><span class="sxs-lookup"><span data-stu-id="ded03-106">Disable method of the SystemRestore class</span></span>

<span data-ttu-id="ded03-107">Deaktiviert die Überwachung auf einem bestimmten Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="ded03-107">Disables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded03-108">Syntax</span></span>


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="ded03-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ded03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded03-110">*Laufwerk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ded03-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded03-111">Das Laufwerk, das deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ded03-111">The drive to be disabled.</span></span> <span data-ttu-id="ded03-112">Die Laufwerks Zeichenfolge muss die Form "C: \\ " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ded03-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="ded03-113">Wenn dieser Parameter das Systemlaufwerk oder eine leere Zeichenfolge ("") ist, werden keine Laufwerke überwacht.</span><span class="sxs-lookup"><span data-stu-id="ded03-113">If this parameter is the system drive or an empty string (""), no drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded03-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ded03-114">Return value</span></span>

<span data-ttu-id="ded03-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ded03-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ded03-116">Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ded03-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="ded03-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ded03-117">Examples</span></span>


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="ded03-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ded03-118">Requirements</span></span>



| <span data-ttu-id="ded03-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ded03-119">Requirement</span></span> | <span data-ttu-id="ded03-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ded03-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ded03-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ded03-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ded03-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ded03-122">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ded03-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ded03-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ded03-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ded03-124">None supported</span></span><br/>                                                         |
| <span data-ttu-id="ded03-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ded03-125">Namespace</span></span><br/>                | <span data-ttu-id="ded03-126">\\Standardwert</span><span class="sxs-lookup"><span data-stu-id="ded03-126">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="ded03-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ded03-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ded03-128"><dt>SR. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ded03-128"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded03-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ded03-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded03-130">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="ded03-130">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





