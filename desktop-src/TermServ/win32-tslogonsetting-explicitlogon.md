---
title: Explizilogon-Methode der Win32_TSLogonSetting-Klasse
description: Die explizlogon-Methode legt die Anmelde Informationen fest, die für die Authentifizierung verwendet werden.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Explizlogon-Methode Remotedesktopdienste
- Explizitlogon-Methode Remotedesktopdienste, Win32_TSLogonSetting-Klasse
- Win32_TSLogonSetting-Klasse Remotedesktopdienste, explizilogon-Methode
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392062"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="c2cec-106">Explizilogon-Methode der Win32- \_ Klasse "tlogonsetting"</span><span class="sxs-lookup"><span data-stu-id="c2cec-106">ExplicitLogon method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="c2cec-107">Die **explizlogon** -Methode legt die Anmelde Informationen fest, die für die Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2cec-107">The **ExplicitLogon** method sets the credentials to use for authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2cec-108">Syntax</span></span>


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a><span data-ttu-id="c2cec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2cec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cec-110">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2cec-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cec-111">Die Anmelde Informationen für den Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="c2cec-111">The user name logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="c2cec-112">*Domäne* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2cec-112">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cec-113">Anmelde Informationen für die Domäne.</span><span class="sxs-lookup"><span data-stu-id="c2cec-113">The domain logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="c2cec-114">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2cec-114">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cec-115">Die Anmelde Informationen für die Kenn Wort Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="c2cec-115">The password logon credential.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cec-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2cec-116">Return value</span></span>

<span data-ttu-id="c2cec-117">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2cec-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c2cec-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c2cec-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="c2cec-119">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="c2cec-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cec-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2cec-120">Remarks</span></span>

<span data-ttu-id="c2cec-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c2cec-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c2cec-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c2cec-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c2cec-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c2cec-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c2cec-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c2cec-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2cec-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2cec-125">Requirements</span></span>



| <span data-ttu-id="c2cec-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2cec-126">Requirement</span></span> | <span data-ttu-id="c2cec-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c2cec-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cec-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2cec-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cec-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2cec-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2cec-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2cec-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cec-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2cec-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2cec-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2cec-132">Namespace</span></span><br/>                | <span data-ttu-id="c2cec-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c2cec-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c2cec-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c2cec-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2cec-135"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2cec-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2cec-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c2cec-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2cec-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2cec-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cec-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2cec-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cec-139">**Win32-Anmelde \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="c2cec-139">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

