---
description: Entfernt die Parameter "dh-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol)" von einem synthetischen Fibre Channel-Port auf einem virtuellen Computer.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Removefbrechannelchap-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348208"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="3adc7-103">Removefibrechannelchap-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3adc7-103">RemoveFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3adc7-104">Entfernt die Parameter "dh-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol)" von einem synthetischen Fibre Channel-Port auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3adc7-104">Removes DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters from a synthetic Fibre Channel port in a virtual machine.</span></span> <span data-ttu-id="3adc7-105">Bei dieser Methode tritt ein Fehler auf, wenn der virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3adc7-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="3adc7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3adc7-106">Syntax</span></span>


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a><span data-ttu-id="3adc7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3adc7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adc7-108">*Fcportsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3adc7-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3adc7-109">Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ syntheticfcportsettingdata**](msvm-syntheticfcportsettingdata.md) -Klasse enthalten, die die synthetischen Fibre Channel Ports definieren, aus denen die dh-CHAP-Parameter entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3adc7-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that define the synthetic Fibre Channel ports to remove the DH-CHAP parameters from.</span></span> <span data-ttu-id="3adc7-110">Die **InstanceId-** Eigenschaft jeder dieser Instanzen identifiziert die Elemente, die geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3adc7-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3adc7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3adc7-111">Return value</span></span>

<span data-ttu-id="3adc7-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3adc7-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3adc7-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3adc7-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-114">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3adc7-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-115">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3adc7-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-116">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3adc7-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-117">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3adc7-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-118">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3adc7-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-119">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3adc7-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-120">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3adc7-120">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-121">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3adc7-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-122">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3adc7-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-123">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3adc7-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3adc7-124">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3adc7-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3adc7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3adc7-125">Requirements</span></span>



| <span data-ttu-id="3adc7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3adc7-126">Requirement</span></span> | <span data-ttu-id="3adc7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3adc7-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3adc7-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3adc7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3adc7-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3adc7-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3adc7-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3adc7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3adc7-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3adc7-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3adc7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3adc7-132">Namespace</span></span><br/>                | <span data-ttu-id="3adc7-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3adc7-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3adc7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3adc7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3adc7-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3adc7-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3adc7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3adc7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3adc7-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3adc7-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3adc7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3adc7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adc7-139">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="3adc7-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




