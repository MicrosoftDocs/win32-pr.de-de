---
description: Fordert das virtuelle Remotedesktopdienste virtuellen Gerät auf, eine Pipe-Verbindung mit dem virtuellen Computer zu starten.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Enableendpoints-Methode der Msvm_RdvComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214747"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a><span data-ttu-id="8de8b-103">Enableendpoints-Methode der MSVM \_ rdvcomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="8de8b-103">EnableEndPoints method of the Msvm\_RdvComponent class</span></span>

<span data-ttu-id="8de8b-104">Fordert das virtuelle Remotedesktopdienste virtuellen Gerät auf, eine Pipe-Verbindung mit dem virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="8de8b-104">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de8b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8de8b-105">Syntax</span></span>


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a><span data-ttu-id="8de8b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8de8b-106">Parameters</span></span>

<span data-ttu-id="8de8b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8de8b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8de8b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8de8b-108">Return value</span></span>

<span data-ttu-id="8de8b-109">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="8de8b-109">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8de8b-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8de8b-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-111">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="8de8b-111">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-112">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="8de8b-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-113">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="8de8b-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-114">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="8de8b-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-115">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="8de8b-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="8de8b-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-117">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="8de8b-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-118">**Nicht** genügend Arbeitsspeicher (32774)</span><span class="sxs-lookup"><span data-stu-id="8de8b-118">**Out of memory** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8de8b-119">Die **Datei wurde nicht gefunden** (32775).</span><span class="sxs-lookup"><span data-stu-id="8de8b-119">**File not found** (32775)</span></span>
</dt> <dt>

 <span data-ttu-id="8de8b-120">(32776)</span><span class="sxs-lookup"><span data-stu-id="8de8b-120">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="8de8b-121">(32777)</span><span class="sxs-lookup"><span data-stu-id="8de8b-121">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="8de8b-122">(32778)</span><span class="sxs-lookup"><span data-stu-id="8de8b-122">(32778)</span></span>
</dt> <dt>

 <span data-ttu-id="8de8b-123">(32779)</span><span class="sxs-lookup"><span data-stu-id="8de8b-123">(32779)</span></span>
</dt> <dt>

 <span data-ttu-id="8de8b-124">(32780)</span><span class="sxs-lookup"><span data-stu-id="8de8b-124">(32780)</span></span>
</dt> <dt>

 <span data-ttu-id="8de8b-125">(32781)</span><span class="sxs-lookup"><span data-stu-id="8de8b-125">(32781)</span></span>
</dt> <dt>

 <span data-ttu-id="8de8b-126">(32782)</span><span class="sxs-lookup"><span data-stu-id="8de8b-126">(32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8de8b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8de8b-127">Requirements</span></span>



| <span data-ttu-id="8de8b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8de8b-128">Requirement</span></span> | <span data-ttu-id="8de8b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8de8b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de8b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8de8b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8de8b-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8de8b-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8de8b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8de8b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8de8b-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8de8b-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8de8b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8de8b-134">Namespace</span></span><br/>                | <span data-ttu-id="8de8b-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8de8b-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8de8b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8de8b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8de8b-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8de8b-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8de8b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8de8b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8de8b-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8de8b-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8de8b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8de8b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de8b-141">**MSVM \_ rdvcomponent**</span><span class="sxs-lookup"><span data-stu-id="8de8b-141">**Msvm\_RdvComponent**</span></span>](msvm-rdvcomponent.md)
</dt> </dl>

 

 




