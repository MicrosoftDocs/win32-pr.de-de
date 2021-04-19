---
description: Ermöglicht den Zugriff auf die interaktive Sitzung des virtuellen Computers auf die angegebene Liste von Treuhändern.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Grantinteractivesessionaccess-Methode der Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8bd49805b5fdc5545a81e4f0b816fe35a6c37b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356655"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="0ef53-103">Grantinteractivesessionaccess-Methode der MSVM \_ Terminalservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0ef53-103">GrantInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="0ef53-104">Ermöglicht den Zugriff auf die interaktive Sitzung des virtuellen Computers auf die angegebene Liste von Treuhändern.</span><span class="sxs-lookup"><span data-stu-id="0ef53-104">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef53-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef53-105">Syntax</span></span>


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0ef53-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ef53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef53-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef53-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef53-108">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt, dem der Zugriff gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef53-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to which access will be granted.</span></span>

</dd> <dt>

<span data-ttu-id="0ef53-109">*Treuhänder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef53-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef53-110">Ein Array von Zeichen folgen, das jeweils einen Vertrauens nehmer identifiziert, dem Zugriff auf die interaktive Sitzung des virtuellen Computers gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef53-110">An array of strings, each identifying a trustee that will be granted access to the interactive session of the virtual machine.</span></span> <span data-ttu-id="0ef53-111">Die Treuhänder-IDs müssen im Windows Sam-kompatiblen Format oder im Windows-SID-Zeichen folgen Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0ef53-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="0ef53-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0ef53-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef53-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0ef53-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef53-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ef53-114">Return value</span></span>

<span data-ttu-id="0ef53-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0ef53-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0ef53-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef53-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="0ef53-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="0ef53-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="0ef53-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="0ef53-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="0ef53-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-122">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="0ef53-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0ef53-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="0ef53-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="0ef53-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0ef53-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="0ef53-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0ef53-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ef53-127">Requirements</span></span>



| <span data-ttu-id="0ef53-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ef53-128">Requirement</span></span> | <span data-ttu-id="0ef53-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0ef53-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef53-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ef53-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef53-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ef53-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0ef53-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ef53-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef53-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ef53-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ef53-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ef53-134">Namespace</span></span><br/>                | <span data-ttu-id="0ef53-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0ef53-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0ef53-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0ef53-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ef53-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0ef53-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ef53-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0ef53-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ef53-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ef53-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ef53-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef53-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef53-141">**MSVM \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="0ef53-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

