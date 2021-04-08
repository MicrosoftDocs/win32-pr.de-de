---
title: Setauthenticationpluginandrecyclerpcapplicationpools-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt das aktuelle Authentifizierungs-Plug-in für den Remotedesktop Gateway-Server (RD-Gateway) fest und wieder verwendet die RPC-Anwendungs Pools in IIS.
ms.assetid: cdceaf50-3d0a-4af0-9ad5-fb43760fcf7b
ms.tgt_platform: multiple
keywords:
- Setauthenticationpluginandrecyclerpcapplicationpools-Methode Remotedesktopdienste
- Setauthenticationpluginandrecyclerpcapplicationpools-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setauthenticationpluginandrecyclerpcapplicationpools-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPluginAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b234e04c349d20ea178de12f050190b30193d444
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740720"
---
# <a name="setauthenticationpluginandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="399f8-106">Setauthenticationpluginandrecyclerpcapplicationpools-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="399f8-106">SetAuthenticationPluginAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="399f8-107">Legt das aktuelle Authentifizierungs-Plug-in für den Remotedesktop Gateway-Server (RD-Gateway) fest und wieder verwendet die RPC-Anwendungs Pools in IIS.</span><span class="sxs-lookup"><span data-stu-id="399f8-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

<span data-ttu-id="399f8-108">Diese Methode entspricht dem Aufrufen der Methoden [**setauthenticationplugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) und [**recyclerpcapplicationpools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) nacheinander.</span><span class="sxs-lookup"><span data-stu-id="399f8-108">This method is equivalent to calling the [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) and [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) methods in sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="399f8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="399f8-109">Syntax</span></span>


```mof
uint32 SetAuthenticationPluginAndRecycleRpcApplicationPools(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="399f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="399f8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="399f8-111">*PluginName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="399f8-111">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="399f8-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="399f8-112">Type: **string**</span></span>

<span data-ttu-id="399f8-113">Name des Authentifizierungs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="399f8-113">Name of the authentication plug-in</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="399f8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="399f8-114">Return value</span></span>

<span data-ttu-id="399f8-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="399f8-115">Type: **uint32**</span></span>

<span data-ttu-id="399f8-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="399f8-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="399f8-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="399f8-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="399f8-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="399f8-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="399f8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="399f8-119">Remarks</span></span>

<span data-ttu-id="399f8-120">Das Aufrufen dieser Methode führt dazu, dass alle vorhandenen Verbindungen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="399f8-120">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="399f8-121">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="399f8-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="399f8-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="399f8-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="399f8-123">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="399f8-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="399f8-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="399f8-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="399f8-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="399f8-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="399f8-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="399f8-126">Requirements</span></span>



| <span data-ttu-id="399f8-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="399f8-127">Requirement</span></span> | <span data-ttu-id="399f8-128">Wert</span><span class="sxs-lookup"><span data-stu-id="399f8-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="399f8-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="399f8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="399f8-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="399f8-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="399f8-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="399f8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="399f8-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="399f8-132">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="399f8-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="399f8-133">Namespace</span></span><br/>                | <span data-ttu-id="399f8-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="399f8-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="399f8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="399f8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="399f8-136"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="399f8-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="399f8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="399f8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="399f8-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="399f8-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="399f8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="399f8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399f8-140">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="399f8-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="399f8-141">**Setauthenticationplugin**</span><span class="sxs-lookup"><span data-stu-id="399f8-141">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="399f8-142">**Recyclerpcapplicationpools**</span><span class="sxs-lookup"><span data-stu-id="399f8-142">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

