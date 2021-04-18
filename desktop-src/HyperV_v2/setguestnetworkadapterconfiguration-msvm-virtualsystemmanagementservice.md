---
description: Konfiguriert die Netzwerkadapter innerhalb des Gast Betriebssystems.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Setguestnetworkadapterconfiguration-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529042"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="aa74d-103">Setguestnetworkadapterconfiguration-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa74d-103">SetGuestNetworkAdapterConfiguration method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="aa74d-104">Konfiguriert die Netzwerkadapter innerhalb des Gast Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="aa74d-104">Configures the network adapters within the guest operating system.</span></span> <span data-ttu-id="aa74d-105">Diese Konfigurationsparameter werden unmittelbar nach dem Einrichten der Kommunikation mit der in dem Gast Betriebssystem ausgelaufenden KVP Exchange-Integrations Komponente angewendet.</span><span class="sxs-lookup"><span data-stu-id="aa74d-105">These configuration parameters are applied immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa74d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa74d-106">Syntax</span></span>


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="aa74d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa74d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa74d-108">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa74d-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa74d-109">Ein Verweis auf die [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, deren Netzwerkadapter konfiguriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aa74d-109">A reference to the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="aa74d-110">*Network Configuration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa74d-110">*NetworkConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa74d-111">Ein Array von eingebetteten Instanzen der [**MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="aa74d-111">An array of embedded instances of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span> <span data-ttu-id="aa74d-112">Jede Instanz beschreibt die Konfigurationsparameter für einen der Netzwerkadapter innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="aa74d-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="aa74d-113">Die **dhcpabled** -Eigenschaft muss für jede Instanz angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa74d-113">The **DHCPEnabled** property must be specified for each instance.</span></span>

</dd> <dt>

<span data-ttu-id="aa74d-114">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aa74d-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa74d-115">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="aa74d-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa74d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa74d-116">Return value</span></span>

<span data-ttu-id="aa74d-117">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="aa74d-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="aa74d-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="aa74d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="aa74d-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="aa74d-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="aa74d-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="aa74d-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="aa74d-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="aa74d-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="aa74d-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="aa74d-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="aa74d-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="aa74d-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="aa74d-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aa74d-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="aa74d-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aa74d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa74d-131">Requirements</span></span>



| <span data-ttu-id="aa74d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa74d-132">Requirement</span></span> | <span data-ttu-id="aa74d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="aa74d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa74d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa74d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="aa74d-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa74d-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aa74d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa74d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="aa74d-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa74d-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa74d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa74d-138">Namespace</span></span><br/>                | <span data-ttu-id="aa74d-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa74d-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aa74d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="aa74d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa74d-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa74d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa74d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="aa74d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa74d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa74d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa74d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa74d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa74d-145">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="aa74d-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

