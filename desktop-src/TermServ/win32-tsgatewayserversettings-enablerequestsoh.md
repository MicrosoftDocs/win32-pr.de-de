---
title: Enablerequestsoh-Methode der Win32_TSGatewayServerSettings-Klasse
description: Enablerequestsoh ist nicht mehr verfügbar.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- Enablerequestsoh-Methode Remotedesktopdienste
- Enablerequestsoh-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enablerequestsoh-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344708"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="5c5ec-106">Enablerequestsoh-Methode der Win32- \_ Klasse "tgatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="5c5ec-106">EnableRequestSOH method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="5c5ec-107">\[Die **enablerequestsoh** -Methode ist ab Windows Server 2016 nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5c5ec-107">\[The **EnableRequestSOH** method is no longer available as of Windows Server 2016.\]</span></span>

<span data-ttu-id="5c5ec-108">Aktiviert oder deaktiviert Anforderungen für ein Statement of Health (SoH).</span><span class="sxs-lookup"><span data-stu-id="5c5ec-108">Enables or disables requests for a Statement of Health (SoH).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5ec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c5ec-109">Syntax</span></span>


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a><span data-ttu-id="5c5ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c5ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c5ec-111">*Requestsoh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c5ec-111">*RequestSOH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c5ec-112">Geben Sie **true** an, um die Funktion zu aktivieren, oder **false** , um das Feature zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="5c5ec-112">Specify **TRUE** to enable the feature or **FALSE** to disable the feature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c5ec-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c5ec-113">Return value</span></span>

<span data-ttu-id="5c5ec-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5c5ec-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5c5ec-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5c5ec-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c5ec-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c5ec-117">Remarks</span></span>

<span data-ttu-id="5c5ec-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5c5ec-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5c5ec-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5c5ec-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c5ec-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5c5ec-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5c5ec-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c5ec-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c5ec-123">Requirements</span></span>



| <span data-ttu-id="5c5ec-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c5ec-124">Requirement</span></span> | <span data-ttu-id="5c5ec-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5c5ec-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5ec-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c5ec-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5c5ec-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c5ec-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5c5ec-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c5ec-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5c5ec-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c5ec-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5c5ec-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5c5ec-130">End of server support</span></span><br/>    | <span data-ttu-id="5c5ec-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5c5ec-131">Windows Server 2012 R2</span></span><br/>                                                        |
| <span data-ttu-id="5c5ec-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c5ec-132">Namespace</span></span><br/>                | <span data-ttu-id="5c5ec-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5c5ec-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5c5ec-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5c5ec-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c5ec-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="5c5ec-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c5ec-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5c5ec-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c5ec-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c5ec-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5c5ec-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c5ec-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5ec-139">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="5c5ec-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

