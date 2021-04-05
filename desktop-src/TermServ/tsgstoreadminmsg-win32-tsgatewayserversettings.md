---
title: Zgstoreadminmsg-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktualisiert die administrative Meldung für den Gatewayserver.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Zgstoreadminmsg-Methode Remotedesktopdienste
- Methode Remotedesktopdienste der Methode "zgstoreadminmsg", Win32_TSGatewayServerSettings Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, Methode "zgstoreadminmsg"
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858954"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="11c06-106">Zgstoreadminmsg-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="11c06-106">TSGStoreAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="11c06-107">Aktualisiert die administrative Meldung für den Gatewayserver.</span><span class="sxs-lookup"><span data-stu-id="11c06-107">Updates the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c06-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="11c06-108">Syntax</span></span>


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="11c06-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c06-110">"GS- *mmsg* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="11c06-110">*TSGAdmMsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c06-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c06-111">Type: **string**</span></span>

<span data-ttu-id="11c06-112">Der Text der administrativen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="11c06-112">The administrative message text.</span></span>

</dd> <dt>

<span data-ttu-id="11c06-113">*Msgstarttime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11c06-113">*MsgStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c06-114">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c06-114">Type: **string**</span></span>

<span data-ttu-id="11c06-115">Die Startzeit der administrativen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="11c06-115">The administrative message start time.</span></span>

</dd> <dt>

<span data-ttu-id="11c06-116">*Msgendtime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11c06-116">*MsgEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c06-117">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c06-117">Type: **string**</span></span>

<span data-ttu-id="11c06-118">Die Endzeit der administrativen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="11c06-118">The administrative message end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c06-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11c06-119">Return value</span></span>

<span data-ttu-id="11c06-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11c06-120">Type: **uint32**</span></span>

<span data-ttu-id="11c06-121">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="11c06-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="11c06-122">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11c06-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="11c06-123">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="11c06-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11c06-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11c06-124">Remarks</span></span>

<span data-ttu-id="11c06-125">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="11c06-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="11c06-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="11c06-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="11c06-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="11c06-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="11c06-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="11c06-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="11c06-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="11c06-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="11c06-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11c06-130">Requirements</span></span>



| <span data-ttu-id="11c06-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11c06-131">Requirement</span></span> | <span data-ttu-id="11c06-132">Wert</span><span class="sxs-lookup"><span data-stu-id="11c06-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c06-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11c06-133">Minimum supported client</span></span><br/> | <span data-ttu-id="11c06-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11c06-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="11c06-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11c06-135">Minimum supported server</span></span><br/> | <span data-ttu-id="11c06-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11c06-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="11c06-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="11c06-137">Namespace</span></span><br/>                | <span data-ttu-id="11c06-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="11c06-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="11c06-139">MOF</span><span class="sxs-lookup"><span data-stu-id="11c06-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11c06-140"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="11c06-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="11c06-141">DLL</span><span class="sxs-lookup"><span data-stu-id="11c06-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c06-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c06-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="11c06-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11c06-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c06-144">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="11c06-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

