---
title: Setvirtualizeloopbackaddressesaktivierte Methode der Win32_TSVirtualIP-Klasse
description: Legt den Wert der virtualizeloopbackaddressesaktivierten Eigenschaft fest.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Setvirtualizeloopbackaddressesaktivierte Methode Remotedesktopdienste
- Setvirtualizeloopbackaddressesaktivierte Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP Klasse Remotedesktopdienste, setvirtualizeloopbackaddressesaktivierte Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339316"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="56ccf-106">Setvirtualizeloopbackaddressesaktivierte Methode der Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="56ccf-106">SetVirtualizeLoopbackAddressesEnabled method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="56ccf-107">Legt den Wert der **virtualizeloopbackaddressesaktivierten** Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="56ccf-107">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ccf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="56ccf-108">Syntax</span></span>


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="56ccf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="56ccf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ccf-110">*Virtualizeloopbackaddressesaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56ccf-110">*VirtualizeLoopbackAddressesEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56ccf-111">Gibt an, ob die Loopback adressvirtualisierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="56ccf-111">Specifies whether to enable loopback address virtualization.</span></span> <span data-ttu-id="56ccf-112">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="56ccf-112">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="56ccf-113">0</span><span class="sxs-lookup"><span data-stu-id="56ccf-113">0</span></span>
</dt> <dd>

<span data-ttu-id="56ccf-114">Aktivieren Sie die Loopback adressvirtualisierung nicht.</span><span class="sxs-lookup"><span data-stu-id="56ccf-114">Do not enable loopback address virtualization.</span></span>

</dd> <dt>

<span data-ttu-id="56ccf-115">1</span><span class="sxs-lookup"><span data-stu-id="56ccf-115">1</span></span>
</dt> <dd>

<span data-ttu-id="56ccf-116">Aktivieren der Loopback adressvirtualisierung.</span><span class="sxs-lookup"><span data-stu-id="56ccf-116">Enable loopback address virtualization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ccf-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56ccf-117">Return value</span></span>

<span data-ttu-id="56ccf-118">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56ccf-118">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="56ccf-119">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="56ccf-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="56ccf-120">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="56ccf-120">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ccf-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56ccf-121">Requirements</span></span>



| <span data-ttu-id="56ccf-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56ccf-122">Requirement</span></span> | <span data-ttu-id="56ccf-123">Wert</span><span class="sxs-lookup"><span data-stu-id="56ccf-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56ccf-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56ccf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="56ccf-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="56ccf-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="56ccf-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56ccf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="56ccf-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56ccf-127">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="56ccf-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="56ccf-128">Namespace</span></span><br/>                | <span data-ttu-id="56ccf-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="56ccf-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="56ccf-130">MOF</span><span class="sxs-lookup"><span data-stu-id="56ccf-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56ccf-131"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="56ccf-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="56ccf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="56ccf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56ccf-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56ccf-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ccf-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56ccf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ccf-135">**Win32- \_ virtualialip**</span><span class="sxs-lookup"><span data-stu-id="56ccf-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





