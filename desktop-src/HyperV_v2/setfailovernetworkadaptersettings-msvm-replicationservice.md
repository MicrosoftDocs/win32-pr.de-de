---
description: Konfiguriert die IP-Einstellungen der Netzwerkadapter, die nach einem Failover auf einen virtuellen Computer angewendet werden sollen.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Setfailovernetworkadaptersettings-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367927"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="871b8-103">Setfailovernetworkadaptersettings-Methode der MSVM- \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="871b8-103">SetFailoverNetworkAdapterSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="871b8-104">Konfiguriert die IP-Einstellungen des Netzwerkadapters, die nach einem Failover auf einen virtuellen Computer angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="871b8-104">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span> <span data-ttu-id="871b8-105">Diese Konfigurationsparameter werden nach einem Failovervorgang angewendet, unmittelbar nach dem Einrichten der Kommunikation mit der KVP Exchange-Integrations Komponente, die innerhalb des Gast Betriebssystems ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="871b8-105">These configuration parameters are applied after a failover operation, immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="871b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="871b8-106">Syntax</span></span>


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="871b8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="871b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="871b8-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="871b8-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="871b8-109">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, dessen Netzwerkadapter konfiguriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="871b8-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="871b8-110">*Network Settings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="871b8-110">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="871b8-111">Ein Array von eingebetteten Instanzen von [**MSVM- \_ failovernetworkadaptersettingdata**](msvm-failovernetworkadaptersettingdata.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="871b8-111">An array of embedded instances of [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) objects.</span></span> <span data-ttu-id="871b8-112">Jede Instanz beschreibt die Konfigurationsparameter für einen der Netzwerkadapter innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="871b8-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="871b8-113">Die Eigenschaften " **IPADRESSEN** " und " **dhcpabled** " müssen für jede Instanz angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="871b8-113">The **IPAddresses** and **DHCPEnabled** properties must be specified on each instance.</span></span>

</dd> <dt>

<span data-ttu-id="871b8-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="871b8-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="871b8-115">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="871b8-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="871b8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="871b8-116">Return value</span></span>

<span data-ttu-id="871b8-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="871b8-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="871b8-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="871b8-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="871b8-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="871b8-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="871b8-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="871b8-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="871b8-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="871b8-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="871b8-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="871b8-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="871b8-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="871b8-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="871b8-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="871b8-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="871b8-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="871b8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="871b8-131">Requirements</span></span>



| <span data-ttu-id="871b8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="871b8-132">Requirement</span></span> | <span data-ttu-id="871b8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="871b8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="871b8-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="871b8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="871b8-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="871b8-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="871b8-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="871b8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="871b8-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="871b8-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="871b8-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="871b8-138">Namespace</span></span><br/>                | <span data-ttu-id="871b8-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="871b8-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="871b8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="871b8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="871b8-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="871b8-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="871b8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="871b8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="871b8-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="871b8-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="871b8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="871b8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871b8-145">**Initiatefailover**</span><span class="sxs-lookup"><span data-stu-id="871b8-145">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="871b8-146">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="871b8-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="871b8-147">**Revertfailover**</span><span class="sxs-lookup"><span data-stu-id="871b8-147">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

