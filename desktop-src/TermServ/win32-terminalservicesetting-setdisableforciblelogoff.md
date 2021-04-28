---
title: SetDisableForcibleLogoff-Methode der Win32_TerminalServiceSetting-Klasse
description: 'SetDisableForcibleLogoff-Methode der Win32_TerminalServiceSetting-Klasse: Diese Methode wird nicht unterstützt.'
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- SetDisableForcibleLogoff-Methode Remotedesktopdienste
- SetDisableForcibleLogoff-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste , SetDisableForcibleLogoff-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103708"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d0ac8-106">SetDisableForcibleLogoff-Methode der Win32 \_ TerminalServiceSetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="d0ac8-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d0ac8-107">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-107">This method is not supported.</span></span>

<span data-ttu-id="d0ac8-108">**Windows Vista und Windows Server 2008:** Aktiviert oder deaktiviert, ob ein bei der Konsole angemeldeter Administrator abgemeldet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ac8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0ac8-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="d0ac8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0ac8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ac8-111">*DisableForcibleLogoff* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d0ac8-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ac8-112">Flag zum Deaktivieren oder Aktivieren der **DisableForcibleLogoff-Eigenschaft,** die bestimmt, ob ein Administrator, der bei der Konsole angemeldet ist, abgemeldet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="d0ac8-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="d0ac8-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="d0ac8-114">Deaktivieren Sie die -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-114">Disable the property.</span></span> <span data-ttu-id="d0ac8-115">Der verbundene Administrator kann abgemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="d0ac8-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="d0ac8-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="d0ac8-117">Aktivieren Sie die -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-117">Enable the property.</span></span> <span data-ttu-id="d0ac8-118">Der verbundene Administrator kann nicht abgemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ac8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0ac8-119">Return value</span></span>

<span data-ttu-id="d0ac8-120">Gibt Erfolg bei Erfolg zurück. andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="d0ac8-121">Eine Liste dieser Werte finden Sie [unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)</span><span class="sxs-lookup"><span data-stu-id="d0ac8-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ac8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0ac8-122">Requirements</span></span>



| <span data-ttu-id="d0ac8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0ac8-123">Requirement</span></span> | <span data-ttu-id="d0ac8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d0ac8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ac8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0ac8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ac8-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0ac8-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0ac8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0ac8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ac8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0ac8-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0ac8-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d0ac8-129">End of client support</span></span><br/>    | <span data-ttu-id="d0ac8-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0ac8-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0ac8-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d0ac8-131">End of server support</span></span><br/>    | <span data-ttu-id="d0ac8-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0ac8-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0ac8-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0ac8-133">Namespace</span></span><br/>                | <span data-ttu-id="d0ac8-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d0ac8-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d0ac8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d0ac8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0ac8-136"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac8-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0ac8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d0ac8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0ac8-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac8-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ac8-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0ac8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ac8-140">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="d0ac8-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





