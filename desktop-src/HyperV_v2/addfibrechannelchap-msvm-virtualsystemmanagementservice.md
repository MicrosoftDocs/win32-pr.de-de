---
description: Fügt einem synthetischen Fibre Channel Port auf einem virtuellen Computer dh-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol)-Parameter hinzu.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Addfbrechannelchap-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959806"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="76037-103">Addfibrechannelchap-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="76037-103">AddFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="76037-104">Fügt einem synthetischen Fibre Channel Port auf einem virtuellen Computer dh-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol)-Parameter hinzu.</span><span class="sxs-lookup"><span data-stu-id="76037-104">Adds DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters to a synthetic Fibre Channel port on a virtual machine.</span></span> <span data-ttu-id="76037-105">Bei dieser Methode tritt ein Fehler auf, wenn der virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76037-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="76037-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="76037-106">Syntax</span></span>


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a><span data-ttu-id="76037-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="76037-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76037-108">*Fcportsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76037-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76037-109">Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ syntheticfcportsettingdata**](msvm-syntheticfcportsettingdata.md) -Klasse enthalten, die Einstellungen für synthetische Fibre Channel Ports für virtuelle Maschinen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="76037-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that describes settings for synthetic Fibre Channel ports for virtual machines.</span></span> <span data-ttu-id="76037-110">Die **InstanceId-** Eigenschaft jeder dieser Instanzen identifiziert die Elemente, die geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76037-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="76037-111">*Secretencoding* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76037-111">*SecretEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76037-112">Gibt den Codierungstyp für den gemeinsamen geheimen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="76037-112">Specifies the type of encoding for the shared secret.</span></span>

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

<span data-ttu-id="76037-113">**Druckbare ASCII** (1)</span><span class="sxs-lookup"><span data-stu-id="76037-113">**Printable ASCII** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="76037-114">**Binär** (2)</span><span class="sxs-lookup"><span data-stu-id="76037-114">**Binary** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="76037-115">*Sharedsecret* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76037-115">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76037-116">Gibt den gemeinsamen geheimen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="76037-116">Specifies the shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76037-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76037-117">Return value</span></span>

<span data-ttu-id="76037-118">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="76037-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="76037-119">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="76037-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="76037-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="76037-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="76037-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="76037-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="76037-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="76037-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="76037-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="76037-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="76037-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="76037-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="76037-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="76037-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="76037-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="76037-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="76037-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="76037-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="76037-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="76037-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="76037-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="76037-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="76037-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="76037-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="76037-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76037-131">Requirements</span></span>



| <span data-ttu-id="76037-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76037-132">Requirement</span></span> | <span data-ttu-id="76037-133">Wert</span><span class="sxs-lookup"><span data-stu-id="76037-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76037-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76037-134">Minimum supported client</span></span><br/> | <span data-ttu-id="76037-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76037-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="76037-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76037-136">Minimum supported server</span></span><br/> | <span data-ttu-id="76037-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76037-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76037-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="76037-138">Namespace</span></span><br/>                | <span data-ttu-id="76037-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="76037-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="76037-140">MOF</span><span class="sxs-lookup"><span data-stu-id="76037-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76037-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="76037-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76037-142">DLL</span><span class="sxs-lookup"><span data-stu-id="76037-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76037-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76037-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76037-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76037-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76037-145">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="76037-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




