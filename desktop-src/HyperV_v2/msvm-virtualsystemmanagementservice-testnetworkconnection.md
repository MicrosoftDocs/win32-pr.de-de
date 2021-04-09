---
description: Testet die Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Testnetworkconnection-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128400"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="3d855-103">Testnetworkconnection-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3d855-103">TestNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3d855-104">Testet die Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="3d855-104">Tests the network connectivity of a VM in a Windows network virtualization environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d855-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d855-105">Syntax</span></span>


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3d855-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d855-107">*Targetnetworkadapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d855-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-108">Verweis auf eine [**MSVM- \_ ethernetportbereitungssettingdata**](msvm-ethernetportallocationsettingdata.md) , die den Zielnetzwerk Adapter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3d855-108">Reference to a [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) describing the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-109">*Issender* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d855-109">*IsSender* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-110">Gibt an, ob diese Methode beim Absender oder Empfänger aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3d855-110">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-111">*Senderip* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d855-111">*SenderIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-112">Die Absender-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3d855-112">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-113">*Receiverip* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d855-113">*ReceiverIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-114">Die Mac-Adresse des Senders.</span><span class="sxs-lookup"><span data-stu-id="3d855-114">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-115">*Receivermac* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d855-115">*ReceiverMac* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-116">Die Mac-Adresse des Senders.</span><span class="sxs-lookup"><span data-stu-id="3d855-116">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-117">*Isolationid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d855-117">*IsolationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-118">Die Isolations-ID.</span><span class="sxs-lookup"><span data-stu-id="3d855-118">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-119">*Sequencennummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d855-119">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-120">Die Isolations-ID.</span><span class="sxs-lookup"><span data-stu-id="3d855-120">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-121">*RoundtripTime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d855-121">*RoundTripTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-122">Die Roundtripzeit.</span><span class="sxs-lookup"><span data-stu-id="3d855-122">The round trip time.</span></span>

</dd> <dt>

<span data-ttu-id="3d855-123">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d855-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d855-124">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3d855-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d855-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d855-125">Return value</span></span>

<span data-ttu-id="3d855-126">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3d855-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3d855-127">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3d855-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-128">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3d855-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-129">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="3d855-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3d855-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-131">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="3d855-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-132">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3d855-132">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-133">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3d855-133">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-134">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="3d855-134">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3d855-135">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3d855-135">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3d855-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d855-136">Requirements</span></span>



| <span data-ttu-id="3d855-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d855-137">Requirement</span></span> | <span data-ttu-id="3d855-138">Wert</span><span class="sxs-lookup"><span data-stu-id="3d855-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d855-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d855-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3d855-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3d855-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3d855-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d855-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3d855-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3d855-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3d855-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d855-143">Namespace</span></span><br/>                | <span data-ttu-id="3d855-144">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3d855-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3d855-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3d855-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d855-146"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3d855-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d855-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3d855-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d855-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d855-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3d855-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d855-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d855-150">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="3d855-150">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

