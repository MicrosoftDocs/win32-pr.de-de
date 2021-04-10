---
title: Setvirtualipactive-Methode der Win32_TSVirtualIP-Klasse
description: Legt den Wert der virtualipactive-Eigenschaft fest.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Setvirtualipactive-Methode Remotedesktopdienste
- Setvirtualipactive-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, setvirtualipactive-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956664"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="7a83b-106">Setvirtualipactive-Methode der Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="7a83b-106">SetVirtualIPActive method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="7a83b-107">Legt den Wert der **virtualipactive** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7a83b-107">Sets the **VirtualIPActive** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a83b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a83b-108">Syntax</span></span>


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a><span data-ttu-id="7a83b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a83b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a83b-110">*Virtualipactive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a83b-110">*VirtualIPActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a83b-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a83b-111">Type: **uint32**</span></span>

<span data-ttu-id="7a83b-112">Gibt an, ob die IP-Virtualisierung auf dem Server aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="7a83b-112">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="7a83b-113">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="7a83b-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="7a83b-114">Null</span><span class="sxs-lookup"><span data-stu-id="7a83b-114">zero</span></span>
</dt> <dd>

<span data-ttu-id="7a83b-115">Die IP-Virtualisierung ist nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="7a83b-115">IP virtualization is not active.</span></span>

</dd> <dt>

<span data-ttu-id="7a83b-116">ungleich NULL</span><span class="sxs-lookup"><span data-stu-id="7a83b-116">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="7a83b-117">Die IP-Virtualisierung ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="7a83b-117">IP virtualization is active.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a83b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a83b-118">Return value</span></span>

<span data-ttu-id="7a83b-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a83b-119">Type: **uint32**</span></span>

<span data-ttu-id="7a83b-120">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a83b-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7a83b-121">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7a83b-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="7a83b-122">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="7a83b-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a83b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a83b-123">Requirements</span></span>



| <span data-ttu-id="7a83b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a83b-124">Requirement</span></span> | <span data-ttu-id="7a83b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7a83b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a83b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a83b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7a83b-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a83b-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7a83b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a83b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7a83b-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a83b-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="7a83b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a83b-130">Namespace</span></span><br/>                | <span data-ttu-id="7a83b-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7a83b-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7a83b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7a83b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a83b-133"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7a83b-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a83b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7a83b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a83b-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a83b-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a83b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a83b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a83b-137">**Win32- \_ virtualialip**</span><span class="sxs-lookup"><span data-stu-id="7a83b-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





