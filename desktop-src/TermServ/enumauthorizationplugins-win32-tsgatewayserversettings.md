---
title: Enumauthorizationplugins-Methode der Win32_TSGatewayServerSettings-Klasse
description: Listet alle registrierten Autorisierungs-Plug-Ins auf.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- Enumauthorizationplugins-Methode Remotedesktopdienste
- Enumauthorizationplugins-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enumauthorizationplugins-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d955c08f5e4f91547751b0f177681ad2abd57c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859297"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="c996a-106">Enumauthorizationplugins-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="c996a-106">EnumAuthorizationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="c996a-107">Listet alle registrierten Autorisierungs-Plug-Ins auf.</span><span class="sxs-lookup"><span data-stu-id="c996a-107">Enumerates all registered authorization plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="c996a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c996a-108">Syntax</span></span>


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="c996a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c996a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c996a-110">*Pluginnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c996a-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c996a-111">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="c996a-111">Type: **string\[\]**</span></span>

<span data-ttu-id="c996a-112">Ein **Zeichen** folgen Array, das die Namen der registrierten Autorisierungs-Plug-ins empfängt.</span><span class="sxs-lookup"><span data-stu-id="c996a-112">A **string** array that receives the names of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="c996a-113">*CLSIDs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c996a-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c996a-114">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="c996a-114">Type: **string\[\]**</span></span>

<span data-ttu-id="c996a-115">Ein **Zeichen** folgen Array, das die CLSIDs der registrierten Autorisierungs-Plug-ins empfängt.</span><span class="sxs-lookup"><span data-stu-id="c996a-115">A **string** array that receives the CLSIDs of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="c996a-116">*Beschreibungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c996a-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c996a-117">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="c996a-117">Type: **string\[\]**</span></span>

<span data-ttu-id="c996a-118">Ein **Zeichen** folgen Array, das die Beschreibungen der registrierten Autorisierungs-Plug-ins empfängt.</span><span class="sxs-lookup"><span data-stu-id="c996a-118">A **string** array that receives the descriptions of the registered authorization plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c996a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c996a-119">Return value</span></span>

<span data-ttu-id="c996a-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c996a-120">Type: **uint32**</span></span>

<span data-ttu-id="c996a-121">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c996a-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c996a-122">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c996a-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c996a-123">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c996a-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c996a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c996a-124">Remarks</span></span>

<span data-ttu-id="c996a-125">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c996a-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c996a-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c996a-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c996a-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c996a-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c996a-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c996a-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c996a-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c996a-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c996a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c996a-130">Requirements</span></span>



| <span data-ttu-id="c996a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c996a-131">Requirement</span></span> | <span data-ttu-id="c996a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c996a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c996a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c996a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c996a-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c996a-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c996a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c996a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c996a-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c996a-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c996a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c996a-137">Namespace</span></span><br/>                | <span data-ttu-id="c996a-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c996a-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c996a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c996a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c996a-140"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="c996a-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c996a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c996a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c996a-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c996a-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c996a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c996a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c996a-144">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="c996a-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

