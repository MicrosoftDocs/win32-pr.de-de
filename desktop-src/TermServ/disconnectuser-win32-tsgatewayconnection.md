---
title: Disconnectuser-Methode der Win32_TSGatewayConnection-Klasse ("zgauthenticationengine. h")
description: Trennt alle Verbindungen des angegebenen Benutzers vom Remotedesktop Gateway-Server (RD-Gateway).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Disconnectuser-Methode Remotedesktopdienste
- Disconnectuser-Methode Remotedesktopdienste, Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste, disconnectuser-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742152"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="031bf-106">Disconnectuser-Methode der Win32-Klasse "t- \_ gatewayconnection"</span><span class="sxs-lookup"><span data-stu-id="031bf-106">DisconnectUser method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="031bf-107">Trennt alle Verbindungen des angegebenen Benutzers vom Remotedesktop Gateway-Server (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="031bf-107">Disconnects all connections of the specified user from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="031bf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="031bf-108">Syntax</span></span>


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="031bf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="031bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031bf-110">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031bf-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031bf-111">Der Benutzername im Format \* Domain \* **\\** _username_ , dessen Verbindungen getrennt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="031bf-111">The user name, in \*Domain\***\\**_UserName_ format, whose connections are to be disconnected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031bf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="031bf-112">Return value</span></span>

<span data-ttu-id="031bf-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="031bf-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="031bf-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="031bf-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="031bf-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="031bf-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="031bf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="031bf-116">Remarks</span></span>

<span data-ttu-id="031bf-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="031bf-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="031bf-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="031bf-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="031bf-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="031bf-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="031bf-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="031bf-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="031bf-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="031bf-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="031bf-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="031bf-122">Requirements</span></span>



| <span data-ttu-id="031bf-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="031bf-123">Requirement</span></span> | <span data-ttu-id="031bf-124">Wert</span><span class="sxs-lookup"><span data-stu-id="031bf-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="031bf-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="031bf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="031bf-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="031bf-126">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="031bf-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="031bf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="031bf-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="031bf-128">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="031bf-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="031bf-129">Namespace</span></span><br/>                | <span data-ttu-id="031bf-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="031bf-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                             |
| <span data-ttu-id="031bf-131">Header</span><span class="sxs-lookup"><span data-stu-id="031bf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="031bf-132"><dt>"Zgauthenticationengine. h"</dt></span><span class="sxs-lookup"><span data-stu-id="031bf-132"><dt>Tsgauthenticationengine.h</dt></span></span> </dl> |
| <span data-ttu-id="031bf-133">MOF</span><span class="sxs-lookup"><span data-stu-id="031bf-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="031bf-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="031bf-134"><dt>TSGateway.mof</dt></span></span> </dl>             |
| <span data-ttu-id="031bf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="031bf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="031bf-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="031bf-136"><dt>AagWmi.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="031bf-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="031bf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031bf-138">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="031bf-138">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

