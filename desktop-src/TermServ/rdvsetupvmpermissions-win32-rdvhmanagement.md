---
title: Rdvsetupvmberechtigungs-Methode der Win32_RdvhManagement-Klasse
description: Legt die Berechtigungen für eine virtuelle Maschine für den aktuellen Benutzer fest.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- RdvsetupvmberechtiRemotedesktopdienste-Methode
- Rdvsetupvmberechtigungs Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, rdvsetupvmberechtigungs Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476713"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="c713e-106">Rdvsetupvmberechtigungs-Methode der Win32 \_ rdvhmanagement-Klasse</span><span class="sxs-lookup"><span data-stu-id="c713e-106">RdvSetupVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="c713e-107">Legt die Berechtigungen für eine virtuelle Maschine für den aktuellen Benutzer fest.</span><span class="sxs-lookup"><span data-stu-id="c713e-107">Sets the permissions on a virtual machine for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="c713e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c713e-108">Syntax</span></span>


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="c713e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c713e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c713e-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c713e-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c713e-111">Der Name des virtuellen Computers, für den Berechtigungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c713e-111">The name of the virtual machine to set permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c713e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c713e-112">Return value</span></span>

<span data-ttu-id="c713e-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c713e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c713e-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c713e-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c713e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c713e-115">Requirements</span></span>



| <span data-ttu-id="c713e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c713e-116">Requirement</span></span> | <span data-ttu-id="c713e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c713e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c713e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c713e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c713e-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c713e-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="c713e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c713e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c713e-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c713e-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="c713e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c713e-122">Namespace</span></span><br/>                | <span data-ttu-id="c713e-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c713e-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="c713e-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c713e-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c713e-125"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="c713e-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c713e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c713e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c713e-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c713e-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c713e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c713e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c713e-129">**Win32- \_ rdvhmanagement**</span><span class="sxs-lookup"><span data-stu-id="c713e-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





