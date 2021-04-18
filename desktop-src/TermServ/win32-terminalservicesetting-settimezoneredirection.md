---
title: Settimezoneredirection-Methode der Win32_TerminalServiceSetting-Klasse
description: Mit der settimezoneredirection-Methode wird die timezoneredirection-Eigenschaft festgelegt, die es dem Client Computer ermöglicht, seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umzuleiten.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Settimezoneredirection-Methode Remotedesktopdienste
- Settimezoneredirection-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, settimezoneredirection-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340999"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="b60d7-106">Settimezoneredirection-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="b60d7-106">SetTimeZoneRedirection method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="b60d7-107">Mit der **settimezoneredirection** -Methode wird die **timezoneredirection** -Eigenschaft festgelegt, die es dem Client Computer ermöglicht, seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="b60d7-107">The **SetTimeZoneRedirection** method sets the **TimeZoneRedirection** property, which allows the client computer to redirect its time zone settings to the Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b60d7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b60d7-108">Syntax</span></span>


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a><span data-ttu-id="b60d7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b60d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b60d7-110">*Timezoneredirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b60d7-110">*TimeZoneRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b60d7-111">Der neue Wert für die **timezoneredirection** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b60d7-111">The new value for the **TimeZoneRedirection** property.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b60d7-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="b60d7-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b60d7-113">Deaktiviert die **timezoneredirection** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b60d7-113">Disables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="b60d7-114">Es findet keine Zeit Zonen Umleitung statt.</span><span class="sxs-lookup"><span data-stu-id="b60d7-114">No time zone redirection occurs.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b60d7-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b60d7-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b60d7-116">Aktiviert die **timezoneredirection** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b60d7-116">Enables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="b60d7-117">Die Zeitzone des Clients wird an die Zeitzone der Sitzung umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b60d7-117">The client's time zone is redirected to the session's time zone.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b60d7-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b60d7-118">Return value</span></span>

<span data-ttu-id="b60d7-119">Gibt bei Erfolg 0 zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b60d7-119">Returns 0 on success; otherwise returns a WMI error code.</span></span> <span data-ttu-id="b60d7-120">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b60d7-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b60d7-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b60d7-121">Remarks</span></span>

<span data-ttu-id="b60d7-122">Standardmäßig ist die Zeitzone für die Remotedesktopdienste Sitzung identisch mit der Zeitzone für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server.</span><span class="sxs-lookup"><span data-stu-id="b60d7-122">By default, the time zone for the Remote Desktop Services session is the same as the time zone for the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="b60d7-123">-Client Computer können keine Zeitzoneninformationen umleiten.</span><span class="sxs-lookup"><span data-stu-id="b60d7-123">Client computers cannot redirect time zone information.</span></span>

<span data-ttu-id="b60d7-124">Wenn die Zeit Zonen Umleitung deaktiviert ist, erben neue Sitzungen die Zeitzone des Servers.</span><span class="sxs-lookup"><span data-stu-id="b60d7-124">If time zone redirection is disabled, new sessions inherit the server time zone.</span></span> <span data-ttu-id="b60d7-125">Wenn eine Sitzung erneut eine Verbindung herstellt, behält die Sitzung die Zeitzone bei, die vor dem Trennen der Verbindung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b60d7-125">When a session reconnects, the session retains the time zone it had prior to disconnecting.</span></span>

<span data-ttu-id="b60d7-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b60d7-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b60d7-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b60d7-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b60d7-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b60d7-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b60d7-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b60d7-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b60d7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b60d7-130">Requirements</span></span>



| <span data-ttu-id="b60d7-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b60d7-131">Requirement</span></span> | <span data-ttu-id="b60d7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b60d7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b60d7-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b60d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b60d7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b60d7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b60d7-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b60d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b60d7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b60d7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b60d7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b60d7-137">Namespace</span></span><br/>                | <span data-ttu-id="b60d7-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b60d7-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b60d7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b60d7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b60d7-140"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b60d7-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b60d7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b60d7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b60d7-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b60d7-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b60d7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b60d7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b60d7-144">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="b60d7-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

