---
title: Update-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Aktualisiert den aktuellen Remote Authentication Dial-in User Service Server (RADIUS).
ms.assetid: 38a15768-66eb-40d6-a079-16555f2bf96a
ms.tgt_platform: multiple
keywords:
- Update-Methode Remotedesktopdienste
- Update-Methode Remotedesktopdienste, Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste, Update-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4faf0c87e49a507ac300d7e8b32f218ed006ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740705"
---
# <a name="update-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="adbef-106">Update-Methode der Win32-Klasse "t- \_ gatewayradiusserver"</span><span class="sxs-lookup"><span data-stu-id="adbef-106">Update method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="adbef-107">Aktualisiert den aktuellen Remote Authentication Dial-in User Service Server (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="adbef-107">Updates the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="adbef-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="adbef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="adbef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adbef-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adbef-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbef-111">Name des RADIUS-Servers.</span><span class="sxs-lookup"><span data-stu-id="adbef-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="adbef-112">*Sharedsecret* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adbef-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbef-113">Gemeinsamer geheimer Schlüssel für den RADIUS-Server.</span><span class="sxs-lookup"><span data-stu-id="adbef-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adbef-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="adbef-114">Return value</span></span>

<span data-ttu-id="adbef-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="adbef-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="adbef-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="adbef-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="adbef-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="adbef-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="adbef-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adbef-118">Remarks</span></span>

<span data-ttu-id="adbef-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="adbef-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="adbef-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="adbef-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="adbef-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="adbef-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="adbef-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="adbef-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="adbef-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="adbef-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="adbef-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adbef-124">Requirements</span></span>



| <span data-ttu-id="adbef-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adbef-125">Requirement</span></span> | <span data-ttu-id="adbef-126">Wert</span><span class="sxs-lookup"><span data-stu-id="adbef-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="adbef-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adbef-127">Minimum supported client</span></span><br/> | <span data-ttu-id="adbef-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="adbef-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="adbef-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adbef-129">Minimum supported server</span></span><br/> | <span data-ttu-id="adbef-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adbef-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="adbef-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="adbef-131">Namespace</span></span><br/>                | <span data-ttu-id="adbef-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="adbef-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="adbef-133">MOF</span><span class="sxs-lookup"><span data-stu-id="adbef-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adbef-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="adbef-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="adbef-135">DLL</span><span class="sxs-lookup"><span data-stu-id="adbef-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adbef-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adbef-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="adbef-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adbef-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adbef-138">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="adbef-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

