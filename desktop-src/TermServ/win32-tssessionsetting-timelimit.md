---
title: Timelimit-Methode der Win32_TSSessionSetting-Klasse
description: Legt die maximale Zeit fest, die dem angegebenen Sitzungs Beschränkungstyp zugeordnet ist.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Timelimit-Methode Remotedesktopdienste
- Timelimit-Methode Remotedesktopdienste, Win32_TSSessionSetting-Klasse
- Win32_TSSessionSetting-Klasse Remotedesktopdienste, timelimit-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517396"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="e0c2f-106">Timelimit-Methode der Win32- \_ Klasse "tssessionsetting"</span><span class="sxs-lookup"><span data-stu-id="e0c2f-106">TimeLimit method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="e0c2f-107">Legt die maximale Zeit fest, die dem angegebenen Sitzungs Beschränkungstyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-107">Sets the maximum time allocated to the specified session-limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c2f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0c2f-108">Syntax</span></span>


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a><span data-ttu-id="e0c2f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0c2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c2f-110">*SessionLimitType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0c2f-110">*SessionLimitType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0c2f-111">Gibt den Typ der Sitzungs Limit-Eigenschaft an, die von der-Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-111">Specifies the type of session-limit property that the method is setting.</span></span>

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span data-ttu-id="e0c2f-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="e0c2f-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="e0c2f-113">Die-Methode legt die **ActiveSessionLimit** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-113">The method is setting the **ActiveSessionLimit** property.</span></span>

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span data-ttu-id="e0c2f-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="e0c2f-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="e0c2f-115">Die-Methode legt die **DisconnectedSessionLimit** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-115">The method is setting the **DisconnectedSessionLimit** property.</span></span>

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span data-ttu-id="e0c2f-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="e0c2f-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="e0c2f-117">Die-Methode legt die **IdleSessionLimit** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-117">The method is setting the **IdleSessionLimit** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e0c2f-118">*ValueLimit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0c2f-118">*ValueLimit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0c2f-119">Die neue maximale Zeit (in Millisekunden) für die Eigenschaft, die vom *SessionLimitType* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-119">The new maximum time, in milliseconds, for the property specified by the *SessionLimitType* parameter.</span></span> <span data-ttu-id="e0c2f-120">Der Wert 0 (null) gibt an, dass keine Sitzungs Beschränkung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-120">The value zero indicates that there is no session limit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c2f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0c2f-121">Return value</span></span>

<span data-ttu-id="e0c2f-122">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-122">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e0c2f-123">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e0c2f-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="e0c2f-124">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c2f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0c2f-125">Remarks</span></span>

<span data-ttu-id="e0c2f-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e0c2f-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e0c2f-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0c2f-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e0c2f-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e0c2f-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c2f-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0c2f-130">Requirements</span></span>



| <span data-ttu-id="e0c2f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0c2f-131">Requirement</span></span> | <span data-ttu-id="e0c2f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e0c2f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c2f-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0c2f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c2f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0c2f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0c2f-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0c2f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c2f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0c2f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0c2f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0c2f-137">Namespace</span></span><br/>                | <span data-ttu-id="e0c2f-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e0c2f-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e0c2f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e0c2f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0c2f-140"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e0c2f-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0c2f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e0c2f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0c2f-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0c2f-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0c2f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0c2f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c2f-144">**Win32- \_ tssessionsetting**</span><span class="sxs-lookup"><span data-stu-id="e0c2f-144">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

