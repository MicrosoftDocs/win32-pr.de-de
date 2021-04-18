---
title: Setpromptforpassword-Methode der Win32_TSLogonSetting-Klasse
description: Die setpromptforpassword-Methode legt die PromptForPassword-Eigenschaft fest.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Setpromptforpassword-Methode Remotedesktopdienste
- Setpromptforpassword-Methode Remotedesktopdienste, Win32_TSLogonSetting-Klasse
- Win32_TSLogonSetting-Klasse Remotedesktopdienste, setpromptforpassword-Methode
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337528"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="b005d-106">Setpromptforpassword-Methode der Win32- \_ Klasse "tlogonsetting"</span><span class="sxs-lookup"><span data-stu-id="b005d-106">SetPromptForPassword method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="b005d-107">Die **setpromptforpassword** -Methode legt die **PromptForPassword** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b005d-107">The **SetPromptForPassword** method sets the **PromptForPassword** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b005d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b005d-108">Syntax</span></span>


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a><span data-ttu-id="b005d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b005d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b005d-110">*PromptForPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b005d-110">*PromptForPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b005d-111">Flag zum Deaktivieren oder Aktivieren der **PromptForPassword** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b005d-111">Flag disabling or enabling the **PromptForPassword** property.</span></span>

<dt>

<span data-ttu-id="b005d-112">0</span><span class="sxs-lookup"><span data-stu-id="b005d-112">0</span></span>
</dt> <dd>

<span data-ttu-id="b005d-113">Deaktiviert die Kenn Wort Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="b005d-113">Disables password-prompting.</span></span>

</dd> <dt>

<span data-ttu-id="b005d-114">1</span><span class="sxs-lookup"><span data-stu-id="b005d-114">1</span></span>
</dt> <dd>

<span data-ttu-id="b005d-115">Aktiviert die Kenn Wort Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="b005d-115">Enables password-prompting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b005d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b005d-116">Return value</span></span>

<span data-ttu-id="b005d-117">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b005d-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b005d-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b005d-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b005d-119">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="b005d-119">The method returns an error if the setting is under group policy control.</span></span>

<dl> <dt>

<span data-ttu-id="b005d-120">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="b005d-120">**FALSE** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b005d-121">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="b005d-121">**TRUE** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b005d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b005d-122">Remarks</span></span>

<span data-ttu-id="b005d-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b005d-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b005d-124">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b005d-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b005d-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b005d-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b005d-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b005d-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b005d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b005d-127">Requirements</span></span>



| <span data-ttu-id="b005d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b005d-128">Requirement</span></span> | <span data-ttu-id="b005d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b005d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b005d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b005d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b005d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b005d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b005d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b005d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b005d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b005d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b005d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="b005d-134">Namespace</span></span><br/>                | <span data-ttu-id="b005d-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b005d-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b005d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b005d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b005d-137"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b005d-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b005d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b005d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b005d-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b005d-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b005d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b005d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b005d-141">**Win32-Anmelde \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="b005d-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

