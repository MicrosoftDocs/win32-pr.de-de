---
description: Stellt die Einstellungen dar, die zum Testen der Netzwerk Konnektivität einer virtuellen Maschine verwendet werden.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Msvm_NetworkConnectionDiagnosticSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050490"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a><span data-ttu-id="342d3-103">MSVM \_ networkconnectiondiagnosticsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="342d3-103">Msvm\_NetworkConnectionDiagnosticSettingData class</span></span>

<span data-ttu-id="342d3-104">Stellt die Einstellungen dar, die zum Testen der Netzwerk Konnektivität einer virtuellen Maschine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="342d3-104">Represents the settings used to test the network connectivity of a virtual machine.</span></span> <span data-ttu-id="342d3-105">Wird von der [**diagnosenetworkconnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="342d3-105">Used by the [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="342d3-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="342d3-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="342d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="342d3-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a><span data-ttu-id="342d3-108">Member</span><span class="sxs-lookup"><span data-stu-id="342d3-108">Members</span></span>

<span data-ttu-id="342d3-109">Die **MSVM \_ networkconnectiondiagnosticsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="342d3-109">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="342d3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="342d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="342d3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="342d3-111">Properties</span></span>

<span data-ttu-id="342d3-112">Die **MSVM \_ networkconnectiondiagnosticsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="342d3-112">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="342d3-113">**Isolationid**</span><span class="sxs-lookup"><span data-stu-id="342d3-113">**IsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="342d3-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="342d3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="342d3-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="342d3-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="342d3-116">Die Isolations-ID.</span><span class="sxs-lookup"><span data-stu-id="342d3-116">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="342d3-117">**IsSender**</span><span class="sxs-lookup"><span data-stu-id="342d3-117">**IsSender**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="342d3-118">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="342d3-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="342d3-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="342d3-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="342d3-120">Gibt an, ob diese Methode beim Absender oder Empfänger aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="342d3-120">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="342d3-121">**Payloadsize**</span><span class="sxs-lookup"><span data-stu-id="342d3-121">**PayloadSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="342d3-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="342d3-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="342d3-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="342d3-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="342d3-124">Die Nutzlastgröße.</span><span class="sxs-lookup"><span data-stu-id="342d3-124">The payload size.</span></span>

</dd> <dt>

<span data-ttu-id="342d3-125">**Receiverip**</span><span class="sxs-lookup"><span data-stu-id="342d3-125">**ReceiverIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="342d3-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="342d3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="342d3-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="342d3-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="342d3-128">Die Empfänger-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="342d3-128">The receiver IP address.</span></span>

</dd> <dt>

<span data-ttu-id="342d3-129">**Receivermac**</span><span class="sxs-lookup"><span data-stu-id="342d3-129">**ReceiverMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="342d3-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="342d3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="342d3-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="342d3-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="342d3-132">Die Mac-Adresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="342d3-132">The receiver MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="342d3-133">**Senderip**</span><span class="sxs-lookup"><span data-stu-id="342d3-133">**SenderIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="342d3-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="342d3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="342d3-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="342d3-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="342d3-136">Die Absender-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="342d3-136">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="342d3-137">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="342d3-137">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="342d3-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="342d3-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="342d3-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="342d3-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="342d3-140">Die Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="342d3-140">The sequence number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="342d3-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="342d3-141">Requirements</span></span>



| <span data-ttu-id="342d3-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="342d3-142">Requirement</span></span> | <span data-ttu-id="342d3-143">Wert</span><span class="sxs-lookup"><span data-stu-id="342d3-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="342d3-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="342d3-144">Minimum supported client</span></span><br/> | <span data-ttu-id="342d3-145">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="342d3-145">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="342d3-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="342d3-146">Minimum supported server</span></span><br/> | <span data-ttu-id="342d3-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="342d3-147">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="342d3-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="342d3-148">Namespace</span></span><br/>                | <span data-ttu-id="342d3-149">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="342d3-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="342d3-150">MOF</span><span class="sxs-lookup"><span data-stu-id="342d3-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="342d3-151"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="342d3-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="342d3-152">DLL</span><span class="sxs-lookup"><span data-stu-id="342d3-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="342d3-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="342d3-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="342d3-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="342d3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="342d3-155">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="342d3-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




