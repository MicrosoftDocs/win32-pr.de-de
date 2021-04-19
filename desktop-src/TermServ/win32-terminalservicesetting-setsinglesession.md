---
title: Setsinglesession-Methode der Win32_TerminalServiceSetting-Klasse
description: Die setsinglesession-Methode legt die SingleSession-Eigenschaft für die-Klasse fest.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Setsinglesession-Methode Remotedesktopdienste
- Setsinglesession-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setsinglesession-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344498"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f2009-106">Setsinglesession-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="f2009-106">SetSingleSession method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f2009-107">Die **setsinglesession** -Methode legt die **SingleSession** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="f2009-107">The **SetSingleSession** method sets the **SingleSession** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2009-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2009-108">Syntax</span></span>


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a><span data-ttu-id="f2009-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2009-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2009-110">*SingleSession* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2009-110">*SingleSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2009-111">Flag zum Deaktivieren oder Aktivieren der **SingleSession** -Eigenschaft, die bestimmt, ob Benutzer auf eine oder mehrere Remotedesktopdienste Sitzungen beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="f2009-111">Flag disabling or enabling the **SingleSession** property, which determines whether users are limited to one or more Remote Desktop Services sessions.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f2009-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="f2009-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f2009-113">Deaktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2009-113">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f2009-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f2009-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f2009-115">Aktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2009-115">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2009-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2009-116">Return value</span></span>

<span data-ttu-id="f2009-117">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2009-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f2009-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f2009-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2009-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2009-119">Remarks</span></span>

<span data-ttu-id="f2009-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f2009-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f2009-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f2009-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f2009-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2009-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f2009-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f2009-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2009-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2009-124">Requirements</span></span>



| <span data-ttu-id="f2009-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2009-125">Requirement</span></span> | <span data-ttu-id="f2009-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f2009-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2009-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2009-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f2009-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2009-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2009-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2009-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f2009-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2009-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2009-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2009-131">Namespace</span></span><br/>                | <span data-ttu-id="f2009-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f2009-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f2009-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f2009-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2009-134"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f2009-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2009-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f2009-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2009-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2009-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2009-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2009-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2009-138">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="f2009-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

