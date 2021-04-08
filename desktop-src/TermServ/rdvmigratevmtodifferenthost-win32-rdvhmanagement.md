---
title: RdvMigrateVmToDifferentHost-Methode der Win32_RdvhManagement-Klasse
description: Initiiert eine Live Migration einer virtuellen Maschine zu einem angegebenen Host.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- RdvMigrateVmToDifferentHost-Methode Remotedesktopdienste
- RdvMigrateVmToDifferentHost-Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, RdvMigrateVmToDifferentHost-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741496"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="13b7b-106">RdvMigrateVmToDifferentHost-Methode der Win32- \_ rdvhmanagement-Klasse</span><span class="sxs-lookup"><span data-stu-id="13b7b-106">RdvMigrateVmToDifferentHost method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="13b7b-107">Initiiert eine Live Migration einer virtuellen Maschine zu einem angegebenen Host.</span><span class="sxs-lookup"><span data-stu-id="13b7b-107">Initiates a live migration of a virtual machine to a specified host.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b7b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13b7b-108">Syntax</span></span>


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a><span data-ttu-id="13b7b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="13b7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b7b-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13b7b-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13b7b-111">Der Name des zu migrierenden virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="13b7b-111">Name of the virtual machine to migrate.</span></span>

</dd> <dt>

<span data-ttu-id="13b7b-112">*Destinationhost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13b7b-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13b7b-113">der Name des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="13b7b-113">name of the destination host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b7b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13b7b-114">Return value</span></span>

<span data-ttu-id="13b7b-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b7b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="13b7b-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="13b7b-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b7b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13b7b-117">Requirements</span></span>



| <span data-ttu-id="13b7b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13b7b-118">Requirement</span></span> | <span data-ttu-id="13b7b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="13b7b-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b7b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13b7b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13b7b-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="13b7b-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="13b7b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13b7b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13b7b-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13b7b-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="13b7b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="13b7b-124">Namespace</span></span><br/>                | <span data-ttu-id="13b7b-125">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="13b7b-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="13b7b-126">MOF</span><span class="sxs-lookup"><span data-stu-id="13b7b-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13b7b-127"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="13b7b-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="13b7b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="13b7b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b7b-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b7b-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b7b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13b7b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b7b-131">**Win32- \_ rdvhmanagement**</span><span class="sxs-lookup"><span data-stu-id="13b7b-131">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





