---
title: Recyclerpcapplicationpools-Methode der Win32_TSGatewayServerSettings-Klasse
description: Wiederverwendungen der RPC-Anwendungs Pools in IIS.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- Recyclerpcapplicationpools-Methode Remotedesktopdienste
- Recyclerpcapplicationpools-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, recyclerpcapplicationpools-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476425"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="d7640-106">Recyclerpcapplicationpools-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="d7640-106">RecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="d7640-107">Wiederverwendungen der RPC-Anwendungs Pools in IIS.</span><span class="sxs-lookup"><span data-stu-id="d7640-107">Recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7640-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7640-108">Syntax</span></span>


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="d7640-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7640-109">Parameters</span></span>

<span data-ttu-id="d7640-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d7640-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7640-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7640-111">Return value</span></span>

<span data-ttu-id="d7640-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d7640-112">Type: **uint32**</span></span>

<span data-ttu-id="d7640-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d7640-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d7640-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7640-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d7640-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d7640-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7640-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7640-116">Remarks</span></span>

<span data-ttu-id="d7640-117">Das Aufrufen dieser Methode führt dazu, dass alle vorhandenen Verbindungen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="d7640-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="d7640-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7640-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d7640-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="d7640-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d7640-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="d7640-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d7640-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7640-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d7640-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d7640-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7640-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7640-123">Requirements</span></span>



| <span data-ttu-id="d7640-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7640-124">Requirement</span></span> | <span data-ttu-id="d7640-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d7640-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7640-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7640-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7640-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d7640-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d7640-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7640-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7640-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7640-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="d7640-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7640-130">Namespace</span></span><br/>                | <span data-ttu-id="d7640-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d7640-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d7640-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d7640-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7640-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="d7640-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7640-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d7640-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7640-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7640-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d7640-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7640-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7640-137">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="d7640-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="d7640-138">**Setauthenticationplugin**</span><span class="sxs-lookup"><span data-stu-id="d7640-138">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

