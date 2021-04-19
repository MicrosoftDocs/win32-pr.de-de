---
title: Add-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Fügt einen neuen Remote Authentication Dial-in User Service Server (RADIUS) hinzu.
ms.assetid: 78f74bb6-8f70-4bc1-8e4d-1670a3ae3f31
ms.tgt_platform: multiple
keywords:
- Methoden Remotedesktopdienste hinzufügen
- Methoden Remotedesktopdienste hinzufügen, Win32_TSGatewayRADIUSServer Schnittstelle
- Win32_TSGatewayRADIUSServer Schnittstellen Remotedesktopdienste, Methode hinzufügen
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Add
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6869c55a6704944c34c68af065875cad92e8385c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346121"
---
# <a name="add-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="9618a-106">Add-Methode der Win32-Klasse "t- \_ gatewayradiusserver"</span><span class="sxs-lookup"><span data-stu-id="9618a-106">Add method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="9618a-107">Fügt einen neuen Remote Authentication Dial-in User Service Server (RADIUS) hinzu.</span><span class="sxs-lookup"><span data-stu-id="9618a-107">Adds a new Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9618a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9618a-108">Syntax</span></span>


```mof
uint32 Add(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="9618a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9618a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9618a-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9618a-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9618a-111">Name des RADIUS-Servers.</span><span class="sxs-lookup"><span data-stu-id="9618a-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="9618a-112">*Sharedsecret* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9618a-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9618a-113">Gemeinsamer geheimer Schlüssel für den RADIUS-Server.</span><span class="sxs-lookup"><span data-stu-id="9618a-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9618a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9618a-114">Return value</span></span>

<span data-ttu-id="9618a-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="9618a-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9618a-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9618a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9618a-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9618a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9618a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9618a-118">Remarks</span></span>

<span data-ttu-id="9618a-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9618a-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9618a-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="9618a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9618a-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9618a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9618a-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9618a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9618a-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9618a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9618a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9618a-124">Requirements</span></span>



| <span data-ttu-id="9618a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9618a-125">Requirement</span></span> | <span data-ttu-id="9618a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9618a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9618a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9618a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9618a-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9618a-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9618a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9618a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9618a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9618a-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9618a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="9618a-131">Namespace</span></span><br/>                | <span data-ttu-id="9618a-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9618a-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9618a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9618a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9618a-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9618a-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9618a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9618a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9618a-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9618a-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9618a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9618a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9618a-138">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="9618a-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

