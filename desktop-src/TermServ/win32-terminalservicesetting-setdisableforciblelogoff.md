---
title: Setdisableforciblelogoff-Methode der Win32_TerminalServiceSetting-Klasse
description: Diese Methode wird nicht unterstützt.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Setdisableforciblelogoff-Methode Remotedesktopdienste
- Setdisableforciblelogoff-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setdisableforciblelogoff-Methode
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
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476404"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="abe3c-106">Setdisableforciblelogoff-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="abe3c-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="abe3c-107">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abe3c-107">This method is not supported.</span></span>

<span data-ttu-id="abe3c-108">**Windows Vista und Windows Server 2008:** Aktiviert oder deaktiviert, ob ein Administrator, der sich bei der Konsole anmeldet, erzwungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="abe3c-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe3c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="abe3c-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="abe3c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="abe3c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe3c-111">*Disableforciblelogoff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abe3c-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe3c-112">Flag zum Deaktivieren oder Aktivieren der **disableerzwungene blelogoff** -Eigenschaft, die bestimmt, ob ein Administrator, der bei der Konsole angemeldet ist, erzwungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="abe3c-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="abe3c-113"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="abe3c-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="abe3c-114">Deaktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="abe3c-114">Disable the property.</span></span> <span data-ttu-id="abe3c-115">Der verbundene Administrator kann abgemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="abe3c-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="abe3c-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="abe3c-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="abe3c-117">Aktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="abe3c-117">Enable the property.</span></span> <span data-ttu-id="abe3c-118">Der verbundene Administrator kann nicht erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="abe3c-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe3c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abe3c-119">Return value</span></span>

<span data-ttu-id="abe3c-120">Gibt bei Erfolg Erfolg zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abe3c-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="abe3c-121">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="abe3c-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe3c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abe3c-122">Requirements</span></span>



| <span data-ttu-id="abe3c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abe3c-123">Requirement</span></span> | <span data-ttu-id="abe3c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="abe3c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abe3c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abe3c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="abe3c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abe3c-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abe3c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abe3c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="abe3c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abe3c-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abe3c-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="abe3c-129">End of client support</span></span><br/>    | <span data-ttu-id="abe3c-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abe3c-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abe3c-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="abe3c-131">End of server support</span></span><br/>    | <span data-ttu-id="abe3c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abe3c-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abe3c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="abe3c-133">Namespace</span></span><br/>                | <span data-ttu-id="abe3c-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="abe3c-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="abe3c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="abe3c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abe3c-136"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="abe3c-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="abe3c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="abe3c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abe3c-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abe3c-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe3c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abe3c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe3c-140">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="abe3c-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





