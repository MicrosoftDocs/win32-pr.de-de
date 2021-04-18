---
title: Setvirtualipmode-Methode der Win32_TSVirtualIP-Klasse
description: Legt den Wert der virtualipmode-Eigenschaft fest.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Setvirtualipmode-Methode Remotedesktopdienste
- Setvirtualipmode-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, setvirtualipmode-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344685"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="1ccd5-106">Setvirtualipmode-Methode der Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="1ccd5-106">SetVirtualIPMode method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="1ccd5-107">Legt den Wert der **virtualipmode** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="1ccd5-107">Sets the **VirtualIPMode** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ccd5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ccd5-108">Syntax</span></span>


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a><span data-ttu-id="1ccd5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ccd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ccd5-110">*Virtualisierungsmodus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ccd5-110">*VirtualIPMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ccd5-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ccd5-111">Type: **uint32**</span></span>

<span data-ttu-id="1ccd5-112">Gibt an, welcher IP-Virtualisierungsmodus auf dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ccd5-112">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="1ccd5-113">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="1ccd5-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="1ccd5-114">0</span><span class="sxs-lookup"><span data-stu-id="1ccd5-114">0</span></span>
</dt> <dd>

<span data-ttu-id="1ccd5-115">Der IP-Virtualisierungsmodus ist pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1ccd5-115">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd5-116">1</span><span class="sxs-lookup"><span data-stu-id="1ccd5-116">1</span></span>
</dt> <dd>

<span data-ttu-id="1ccd5-117">Der IP-Virtualisierungsmodus ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1ccd5-117">The IP virtualization mode is per-user.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ccd5-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ccd5-118">Return value</span></span>

<span data-ttu-id="1ccd5-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ccd5-119">Type: **uint32**</span></span>

<span data-ttu-id="1ccd5-120">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1ccd5-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1ccd5-121">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1ccd5-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1ccd5-122">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="1ccd5-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ccd5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ccd5-123">Requirements</span></span>



| <span data-ttu-id="1ccd5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ccd5-124">Requirement</span></span> | <span data-ttu-id="1ccd5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1ccd5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccd5-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ccd5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ccd5-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ccd5-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1ccd5-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ccd5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ccd5-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ccd5-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="1ccd5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ccd5-130">Namespace</span></span><br/>                | <span data-ttu-id="1ccd5-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1ccd5-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1ccd5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1ccd5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ccd5-133"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ccd5-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ccd5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1ccd5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ccd5-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ccd5-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ccd5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ccd5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ccd5-137">**Win32- \_ virtualialip**</span><span class="sxs-lookup"><span data-stu-id="1ccd5-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





