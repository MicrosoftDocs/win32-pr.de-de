---
description: Ändert die Autorisierungs Anmelde Informationen des Besitzers des TPM-Geräts. Die alten und neuen Autorisierungs Kennwörter für Besitzer sind erforderlich.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Changebesitzauth-Methode der CIM_TPM-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360022"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a><span data-ttu-id="74599-104">Changebesitzauth-Methode der CIM \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="74599-104">ChangeOwnerAuth method of the CIM\_TPM class</span></span>

<span data-ttu-id="74599-105">Ändert die Autorisierungs Anmelde Informationen des Besitzers des TPM-Geräts.</span><span class="sxs-lookup"><span data-stu-id="74599-105">Changes the owner authorization credential of the TPM device.</span></span> <span data-ttu-id="74599-106">Die alten und neuen Autorisierungs Kennwörter für Besitzer sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="74599-106">The old and new owner authorization passwords are required.</span></span>

## <a name="syntax"></a><span data-ttu-id="74599-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74599-107">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="74599-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74599-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74599-109">*Oldownerauth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74599-109">*OldOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74599-110">Stellt die alten Autorisierungs Anmelde Informationen dar, die erforderlich sind, um das TPM-Gerät in Besitz zu nehmen. Die **CIM \_ sharedcredential** -Unterklasse ist möglicherweise mit einem nicht-NULL-Wert von **CIM \_ sharedcredential** erforderlich.**Secret** -Eigenschaft für den-Parameter.</span><span class="sxs-lookup"><span data-stu-id="74599-110">Represents the old owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="74599-111">" *Netwownerauth* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="74599-111">*NewOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74599-112">Stellt die neuen Autorisierungs Anmelde Informationen dar, die erforderlich sind, um das TPM-Gerät in Besitz zu nehmen. Die **CIM \_ sharedcredential** -Unterklasse ist möglicherweise mit einem nicht-NULL-Wert von **CIM \_ sharedcredential** erforderlich.**Secret** -Eigenschaft für den-Parameter.</span><span class="sxs-lookup"><span data-stu-id="74599-112">Represents the new owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74599-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74599-113">Return value</span></span>

<span data-ttu-id="74599-114">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74599-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="74599-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="74599-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74599-116">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="74599-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74599-117">**Unbekannter/nicht** angegebener Fehler (2)</span><span class="sxs-lookup"><span data-stu-id="74599-117">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74599-118">**DMTF reserviert** (3.. 4095)</span><span class="sxs-lookup"><span data-stu-id="74599-118">**DMTF Reserved** (3..4095)</span></span>
</dt> <dt>

<span data-ttu-id="74599-119">**Reservierte Methode** (4096.. 32767)</span><span class="sxs-lookup"><span data-stu-id="74599-119">**Method Reserved** (4096..32767)</span></span>
</dt> <dt>

<span data-ttu-id="74599-120">**Anbieter angegeben** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="74599-120">**Vendor Specified** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="74599-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74599-121">Requirements</span></span>



| <span data-ttu-id="74599-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74599-122">Requirement</span></span> | <span data-ttu-id="74599-123">Wert</span><span class="sxs-lookup"><span data-stu-id="74599-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74599-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74599-124">Minimum supported client</span></span><br/> | <span data-ttu-id="74599-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74599-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="74599-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74599-126">Minimum supported server</span></span><br/> | <span data-ttu-id="74599-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="74599-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="74599-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="74599-128">Namespace</span></span><br/>                | <span data-ttu-id="74599-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="74599-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="74599-130">MOF</span><span class="sxs-lookup"><span data-stu-id="74599-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74599-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="74599-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74599-132">DLL</span><span class="sxs-lookup"><span data-stu-id="74599-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74599-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74599-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74599-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74599-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74599-135">**CIM- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="74599-135">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




