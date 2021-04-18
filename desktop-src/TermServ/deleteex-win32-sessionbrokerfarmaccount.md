---
title: DeleteEx-Methode der Win32_SessionBrokerFarmAccount-Klasse
description: Die Win32- \_ Klasse "sessionbrokerfarmaccount" ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar. | DeleteEx-Methode der Win32_SessionBrokerFarmAccount-Klasse
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- DeleteEx-Methode Remotedesktopdienste
- DeleteEx-Methode Remotedesktopdienste, Win32_SessionBrokerFarmAccount-Klasse
- Win32_SessionBrokerFarmAccount-Klasse Remotedesktopdienste, DeleteEx-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354936"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="5443b-107">DeleteEx-Methode der Win32- \_ Klasse "sessionbrokerfarmaccount"</span><span class="sxs-lookup"><span data-stu-id="5443b-107">DeleteEx method of the Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="5443b-108">\[Die Win32-Klasse " [**\_ sessionbrokerfarmaccount**](win32-sessionbrokerfarmaccount.md) " ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5443b-108">\[The [**Win32\_SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="5443b-109">Löscht das Farmkonto.</span><span class="sxs-lookup"><span data-stu-id="5443b-109">Deletes the farm account.</span></span>

## <a name="syntax"></a><span data-ttu-id="5443b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5443b-110">Syntax</span></span>


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a><span data-ttu-id="5443b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5443b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5443b-112">*Deletecomputerobject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5443b-112">*DeleteComputerObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5443b-113">Gibt an, ob das der Farm zugeordnete Computer Objekt aus Active Directory entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5443b-113">Indicates whether the computer object associated with the farm is to be removed from Active Directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5443b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5443b-114">Return value</span></span>

<span data-ttu-id="5443b-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5443b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5443b-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5443b-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5443b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5443b-117">Requirements</span></span>



| <span data-ttu-id="5443b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5443b-118">Requirement</span></span> | <span data-ttu-id="5443b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5443b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5443b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5443b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5443b-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5443b-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5443b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5443b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5443b-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5443b-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="5443b-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5443b-124">End of client support</span></span><br/>    | <span data-ttu-id="5443b-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5443b-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5443b-126">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5443b-126">End of server support</span></span><br/>    | <span data-ttu-id="5443b-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5443b-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="5443b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5443b-128">Namespace</span></span><br/>                | <span data-ttu-id="5443b-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5443b-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="5443b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5443b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5443b-131"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="5443b-131"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5443b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5443b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5443b-133"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5443b-133"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5443b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5443b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5443b-135">**Win32 \_ sessionbrokerfarmaccount**</span><span class="sxs-lookup"><span data-stu-id="5443b-135">**Win32\_SessionBrokerFarmAccount**</span></span>](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





