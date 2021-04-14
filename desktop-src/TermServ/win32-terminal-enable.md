---
title: Enable-Methode der Win32_Terminal-Klasse
description: Mit der enable-Methode wird das Terminal deaktiviert oder aktiviert.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Methoden Remotedesktopdienste aktivieren
- Methoden Remotedesktopdienste aktivieren, Win32_Terminal Klasse
- Win32_Terminal Klasse Remotedesktopdienste, Methode aktivieren
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391656"
---
# <a name="enable-method-of-the-win32_terminal-class"></a><span data-ttu-id="84b33-106">Enable-Methode der Win32- \_ Terminal Klasse</span><span class="sxs-lookup"><span data-stu-id="84b33-106">Enable method of the Win32\_Terminal class</span></span>

<span data-ttu-id="84b33-107">Mit der **enable** -Methode wird das Terminal deaktiviert oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="84b33-107">The **Enable** method disables or enables the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b33-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="84b33-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="84b33-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="84b33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84b33-110">*fenableterminal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84b33-110">*fEnableTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84b33-111">Flag, das das Terminal deaktiviert oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="84b33-111">Flag that disables or enables the terminal.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="84b33-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="84b33-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="84b33-113">Das Terminal ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="84b33-113">The terminal is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="84b33-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="84b33-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="84b33-115">Das Terminal ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="84b33-115">The terminal is enabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84b33-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84b33-116">Return value</span></span>

<span data-ttu-id="84b33-117">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84b33-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="84b33-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="84b33-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="84b33-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84b33-119">Remarks</span></span>

<span data-ttu-id="84b33-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="84b33-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="84b33-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="84b33-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="84b33-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="84b33-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="84b33-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="84b33-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="84b33-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84b33-124">Requirements</span></span>



| <span data-ttu-id="84b33-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84b33-125">Requirement</span></span> | <span data-ttu-id="84b33-126">Wert</span><span class="sxs-lookup"><span data-stu-id="84b33-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84b33-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84b33-127">Minimum supported client</span></span><br/> | <span data-ttu-id="84b33-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84b33-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84b33-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84b33-129">Minimum supported server</span></span><br/> | <span data-ttu-id="84b33-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84b33-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84b33-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="84b33-131">Namespace</span></span><br/>                | <span data-ttu-id="84b33-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="84b33-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="84b33-133">MOF</span><span class="sxs-lookup"><span data-stu-id="84b33-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84b33-134"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="84b33-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="84b33-135">DLL</span><span class="sxs-lookup"><span data-stu-id="84b33-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84b33-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84b33-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b33-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84b33-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b33-138">**Win32- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="84b33-138">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

