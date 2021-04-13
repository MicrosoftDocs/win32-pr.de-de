---
title: Setauthorizationplugin-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt das aktuelle Autorisierungs-Plug-in für den Remotedesktop Gateway-Server (RD-Gateway) fest.
ms.assetid: 236c9cca-4efc-433a-8f1f-e3044e0588b3
ms.tgt_platform: multiple
keywords:
- Setauthorizationplugin-Methode Remotedesktopdienste
- Setauthorizationplugin-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setauthorizationplugin-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthorizationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdb3cb07a7c0a30e84245a2d22e383dea168247
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518173"
---
# <a name="setauthorizationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="f82d1-106">Setauthorizationplugin-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="f82d1-106">SetAuthorizationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="f82d1-107">Legt das aktuelle Autorisierungs-Plug-in für den Remotedesktop Gateway-Server (RD-Gateway) fest.</span><span class="sxs-lookup"><span data-stu-id="f82d1-107">Sets the current authorization plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f82d1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f82d1-108">Syntax</span></span>


```mof
uint32 SetAuthorizationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="f82d1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f82d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f82d1-110">*PluginName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f82d1-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f82d1-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f82d1-111">Type: **string**</span></span>

<span data-ttu-id="f82d1-112">Der Name des neuen aktuellen Autorisierungs-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="f82d1-112">The name of the new current authorization plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f82d1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f82d1-113">Return value</span></span>

<span data-ttu-id="f82d1-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f82d1-114">Type: **uint32**</span></span>

<span data-ttu-id="f82d1-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f82d1-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f82d1-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f82d1-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f82d1-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f82d1-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f82d1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f82d1-118">Remarks</span></span>

<span data-ttu-id="f82d1-119">Sie müssen die Methode [**recyclerpcapplicationpools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) aufzurufen, damit das Autorisierungs-Plug-in funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f82d1-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authorization plug-in to work.</span></span>

<span data-ttu-id="f82d1-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f82d1-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f82d1-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f82d1-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f82d1-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f82d1-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f82d1-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f82d1-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f82d1-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f82d1-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f82d1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f82d1-125">Requirements</span></span>



| <span data-ttu-id="f82d1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f82d1-126">Requirement</span></span> | <span data-ttu-id="f82d1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f82d1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f82d1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f82d1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f82d1-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f82d1-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f82d1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f82d1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f82d1-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f82d1-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="f82d1-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f82d1-132">Namespace</span></span><br/>                | <span data-ttu-id="f82d1-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f82d1-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f82d1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f82d1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f82d1-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="f82d1-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f82d1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f82d1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f82d1-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f82d1-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f82d1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f82d1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f82d1-139">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="f82d1-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="f82d1-140">**Recyclerpcapplicationpools**</span><span class="sxs-lookup"><span data-stu-id="f82d1-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

