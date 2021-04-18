---
title: Getlastrestorestatus-Methode der SystemRestore-Klasse
description: Ruft den Status der letzten Systemwiederherstellung ab.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Getlastrestorestatus-Methode System Wiederherstellung
- Getlastrestorestatus-Methode System Wiederherstellung, SystemRestore-Klasse
- System Restore-Klassen System Wiederherstellung, getlastrestorestatus-Methode
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340760"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a><span data-ttu-id="6d9b7-106">Getlastrestorestatus-Methode der SystemRestore-Klasse</span><span class="sxs-lookup"><span data-stu-id="6d9b7-106">GetLastRestoreStatus method of the SystemRestore class</span></span>

<span data-ttu-id="6d9b7-107">Ruft den Status der letzten Systemwiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-107">Retrieves the status of the last system restore.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9b7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d9b7-108">Syntax</span></span>


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a><span data-ttu-id="6d9b7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d9b7-109">Parameters</span></span>

<span data-ttu-id="6d9b7-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d9b7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d9b7-111">Return value</span></span>

<span data-ttu-id="6d9b7-112">Die-Methode gibt einen der folgenden Statuswerte zurück.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-112">The method returns one of the following status values.</span></span>



| <span data-ttu-id="6d9b7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d9b7-113">Return value</span></span>                                                                 | <span data-ttu-id="6d9b7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d9b7-114">Description</span></span>                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6d9b7-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b7-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6d9b7-116">Die letzte Wiederherstellung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-116">The last restore failed.</span></span><br/>          |
| <dl> <span data-ttu-id="6d9b7-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b7-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6d9b7-118">Die letzte Wiederherstellung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-118">The last restore was successful.</span></span><br/>  |
| <dl> <span data-ttu-id="6d9b7-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b7-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6d9b7-120">Die letzte Wiederherstellung wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="6d9b7-120">The last restore was interrupted.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="6d9b7-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d9b7-121">Examples</span></span>


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a><span data-ttu-id="6d9b7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d9b7-122">Requirements</span></span>



| <span data-ttu-id="6d9b7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d9b7-123">Requirement</span></span> | <span data-ttu-id="6d9b7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6d9b7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6d9b7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d9b7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9b7-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d9b7-126">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6d9b7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d9b7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9b7-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6d9b7-128">None supported</span></span><br/>                                                         |
| <span data-ttu-id="6d9b7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d9b7-129">Namespace</span></span><br/>                | <span data-ttu-id="6d9b7-130">\\Standardwert</span><span class="sxs-lookup"><span data-stu-id="6d9b7-130">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="6d9b7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6d9b7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d9b7-132"><dt>SR. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b7-132"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9b7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d9b7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9b7-134">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="6d9b7-134">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





