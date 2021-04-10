---
title: Setdefaultpluginsandrecyclerpcapplicationpools-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt die aktuellen Authentifizierungs-und Autorisierungs-Plug-Ins für den Remotedesktop Gateway-Server (RD-Gateway) fest und wieder verwendet die RPC-Anwendungs Pools in IIS.
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- Setdefaultpluginsandrecyclerpcapplicationpools-Methode Remotedesktopdienste
- Setdefaultpluginsandrecyclerpcapplicationpools-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setdefaultpluginsandrecyclerpcapplicationpools-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957057"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="dccb9-106">Setdefaultpluginsandrecyclerpcapplicationpools-Methode der Win32- \_ Klasse "Klasse-gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="dccb9-106">SetDefaultPluginsAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="dccb9-107">Legt die aktuellen Authentifizierungs-und Autorisierungs-Plug-Ins für den Remotedesktop Gateway-Server (RD-Gateway) fest und wieder verwendet die RPC-Anwendungs Pools in IIS.</span><span class="sxs-lookup"><span data-stu-id="dccb9-107">Sets the current authentication and authorization plug-ins for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="dccb9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dccb9-108">Syntax</span></span>


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="dccb9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccb9-109">Parameters</span></span>

<span data-ttu-id="dccb9-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="dccb9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dccb9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dccb9-111">Return value</span></span>

<span data-ttu-id="dccb9-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dccb9-112">Type: **uint32**</span></span>

<span data-ttu-id="dccb9-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="dccb9-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="dccb9-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dccb9-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="dccb9-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dccb9-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dccb9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dccb9-116">Remarks</span></span>

<span data-ttu-id="dccb9-117">Das Aufrufen dieser Methode führt dazu, dass alle vorhandenen Verbindungen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="dccb9-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="dccb9-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dccb9-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="dccb9-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="dccb9-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dccb9-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="dccb9-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dccb9-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dccb9-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dccb9-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dccb9-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dccb9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dccb9-123">Requirements</span></span>



| <span data-ttu-id="dccb9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dccb9-124">Requirement</span></span> | <span data-ttu-id="dccb9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dccb9-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dccb9-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dccb9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dccb9-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dccb9-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="dccb9-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dccb9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dccb9-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dccb9-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="dccb9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="dccb9-130">Namespace</span></span><br/>                | <span data-ttu-id="dccb9-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="dccb9-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="dccb9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="dccb9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dccb9-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="dccb9-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="dccb9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dccb9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dccb9-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dccb9-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="dccb9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dccb9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccb9-137">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="dccb9-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

