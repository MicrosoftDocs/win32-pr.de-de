---
title: Rdvundovmberechtigungs-Methode der Win32_RdvhManagement-Klasse
description: Stellt die von rdvsetupvm-Berechtigungen festgelegten Berechtigungen auf dem angegebenen virtuellen Computer wieder her.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Rdvundovmberechtigungen-Methode Remotedesktopdienste
- Rdvundovmberechtigungs Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, rdvundovmberechtigungs Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478867"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="53266-106">Rdvundovmberechtigungs-Methode der Win32 \_ rdvhmanagement-Klasse</span><span class="sxs-lookup"><span data-stu-id="53266-106">RdvUndoVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="53266-107">Stellt die von [**rdvsetupvm-Berechtigungen**](rdvsetupvmpermissions-win32-rdvhmanagement.md) festgelegten Berechtigungen auf dem angegebenen virtuellen Computer wieder her.</span><span class="sxs-lookup"><span data-stu-id="53266-107">Reverts permissions set by [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) on the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="53266-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="53266-108">Syntax</span></span>


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="53266-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="53266-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53266-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53266-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53266-111">Der Name des virtuellen Computers, für den Berechtigungen rückgängig gemacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53266-111">Name of the virtual machine to undo permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53266-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53266-112">Return value</span></span>

<span data-ttu-id="53266-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="53266-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="53266-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="53266-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="53266-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53266-115">Requirements</span></span>



| <span data-ttu-id="53266-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53266-116">Requirement</span></span> | <span data-ttu-id="53266-117">Wert</span><span class="sxs-lookup"><span data-stu-id="53266-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="53266-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53266-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53266-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="53266-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="53266-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53266-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53266-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53266-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="53266-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="53266-122">Namespace</span></span><br/>                | <span data-ttu-id="53266-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="53266-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="53266-124">MOF</span><span class="sxs-lookup"><span data-stu-id="53266-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53266-125"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="53266-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="53266-126">DLL</span><span class="sxs-lookup"><span data-stu-id="53266-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53266-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53266-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53266-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53266-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53266-129">**Win32- \_ rdvhmanagement**</span><span class="sxs-lookup"><span data-stu-id="53266-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





