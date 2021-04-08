---
description: Widerruft den Zugriff auf die interaktive Sitzung der virtuellen Maschine aus der angegebenen Liste von Treuhändern.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Revokeinteractivesessionaccess-Methode der Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756499"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="795d4-103">Revokeinteractivesessionaccess-Methode der MSVM \_ Terminalservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="795d4-103">RevokeInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="795d4-104">Widerruft den Zugriff auf die interaktive Sitzung der virtuellen Maschine aus der angegebenen Liste von Treuhändern.</span><span class="sxs-lookup"><span data-stu-id="795d4-104">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="795d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="795d4-105">Syntax</span></span>


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="795d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="795d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="795d4-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="795d4-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795d4-108">Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse, die den virtuellen Computer darstellt, auf den der Zugriff aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="795d4-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to which access will be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="795d4-109">*Treuhänder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="795d4-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795d4-110">Ein Array von Zeichen folgen, das jeweils einen Vertrauens nehmer identifiziert, dessen Zugriffsrechte widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="795d4-110">An array of strings, each identifying a trustee whose access rights will be revoked.</span></span> <span data-ttu-id="795d4-111">Die Treuhänder-IDs müssen im Windows Sam-kompatiblen Format oder im Windows-SID-Zeichen folgen Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="795d4-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="795d4-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="795d4-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="795d4-113">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="795d4-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="795d4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="795d4-114">Return value</span></span>

<span data-ttu-id="795d4-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="795d4-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="795d4-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="795d4-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-117">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="795d4-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-118">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="795d4-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="795d4-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-120">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="795d4-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-121">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="795d4-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-122">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="795d4-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-123">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="795d4-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="795d4-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-125">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="795d4-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="795d4-126">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="795d4-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="795d4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="795d4-127">Requirements</span></span>



| <span data-ttu-id="795d4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="795d4-128">Requirement</span></span> | <span data-ttu-id="795d4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="795d4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="795d4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="795d4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="795d4-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="795d4-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="795d4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="795d4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="795d4-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="795d4-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="795d4-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="795d4-134">Namespace</span></span><br/>                | <span data-ttu-id="795d4-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="795d4-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="795d4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="795d4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="795d4-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="795d4-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="795d4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="795d4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="795d4-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="795d4-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="795d4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="795d4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795d4-141">**MSVM \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="795d4-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

