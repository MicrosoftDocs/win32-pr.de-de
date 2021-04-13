---
title: Rdvcopybasevmlokal-Methode der Win32_RdvhManagement-Klasse
description: Kopiert eine lokale virtuelle Basismaschine auf einen angegebenen RDV-Host Server (Remote Desktop Virtualization).
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Rdvcopybasevmlokal-Methode Remotedesktopdienste
- Rdvcopybasevmlokal-Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, rdvcopybasevmlokal-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392168"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="ea5a9-106">Rdvcopybasevmlokal-Methode der Win32 \_ rdvhmanagement-Klasse</span><span class="sxs-lookup"><span data-stu-id="ea5a9-106">RdvCopyBaseVmLocally method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="ea5a9-107">Kopiert eine lokale virtuelle Basismaschine auf einen angegebenen RDV-Host Server (Remote Desktop Virtualization).</span><span class="sxs-lookup"><span data-stu-id="ea5a9-107">Copies a local base virtual machine to a specified remote desktop virtualization (RDV) host server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea5a9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea5a9-108">Syntax</span></span>


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a><span data-ttu-id="ea5a9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea5a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea5a9-110">*Basevmlocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea5a9-110">*BaseVmLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea5a9-111">Der Speicherort der virtuellen Basismaschine.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-111">The base virtual machine location.</span></span>

</dd> <dt>

<span data-ttu-id="ea5a9-112">*Farmname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea5a9-112">*FarmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea5a9-113">Der Name der Host Farm, in die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-113">The name of the host farm to copy to.</span></span>

</dd> <dt>

<span data-ttu-id="ea5a9-114">*Goldcacheloation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea5a9-114">*GoldCacheLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea5a9-115">Der Speicherort des Gold Caches.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-115">The gold cache location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea5a9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea5a9-116">Return value</span></span>

<span data-ttu-id="ea5a9-117">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ea5a9-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ea5a9-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea5a9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea5a9-119">Requirements</span></span>



| <span data-ttu-id="ea5a9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea5a9-120">Requirement</span></span> | <span data-ttu-id="ea5a9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ea5a9-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea5a9-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea5a9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea5a9-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea5a9-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="ea5a9-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea5a9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea5a9-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea5a9-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ea5a9-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea5a9-126">Namespace</span></span><br/>                | <span data-ttu-id="ea5a9-127">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ea5a9-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="ea5a9-128">MOF</span><span class="sxs-lookup"><span data-stu-id="ea5a9-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea5a9-129"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="ea5a9-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="ea5a9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ea5a9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea5a9-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea5a9-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea5a9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea5a9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea5a9-133">**Win32- \_ rdvhmanagement**</span><span class="sxs-lookup"><span data-stu-id="ea5a9-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





