---
title: Update-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Aktualisiert die aktuelle Remotedesktop Ressourcen Autorisierungs Richtlinie (RD \ 160; Rap).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Update-Methode Remotedesktopdienste
- Update-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, Update-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104282"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="db713-106">Update-Methode der Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="db713-106">Update method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="db713-107">Aktualisiert die aktuelle Remotedesktop Ressourcen Autorisierungs Richtlinie (RD-RAP).</span><span class="sxs-lookup"><span data-stu-id="db713-107">Updates the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="db713-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db713-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="db713-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db713-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db713-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-111">Name der RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="db713-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="db713-112">*Beschreibung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-113">Beschreibung der RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="db713-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="db713-114">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-115">Gibt an, ob die RD-RAP aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="db713-115">Indicates whether the RD RAP should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="db713-116">*Resourcegroupname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-116">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-117">Name der Ressourcengruppe, die mit dieser RD-RAP verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="db713-117">Resource group name associated with this RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="db713-118">*Resourcegrouptype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-118">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-119">Der Ressourcen Gruppentyp.</span><span class="sxs-lookup"><span data-stu-id="db713-119">Resource group type.</span></span>

<dt>

<span data-ttu-id="db713-120">Sorgte</span><span class="sxs-lookup"><span data-stu-id="db713-120">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="db713-121">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="db713-121">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="db713-122">Gewöhnt</span><span class="sxs-lookup"><span data-stu-id="db713-122">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="db713-123">Computer Gruppe, wie in Active Directory Domain Services gespeichert.</span><span class="sxs-lookup"><span data-stu-id="db713-123">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="db713-124">Allen</span><span class="sxs-lookup"><span data-stu-id="db713-124">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="db713-125">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="db713-125">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="db713-126">*Usergroupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-127">Durch Semikolons getrennte Liste von Benutzergruppen Namen.</span><span class="sxs-lookup"><span data-stu-id="db713-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="db713-128">Die Namen weisen das Format *Domäne \\ usergroupname* auf.</span><span class="sxs-lookup"><span data-stu-id="db713-128">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="db713-129">Wenn der Benutzer zu einer dieser Benutzergruppen gehört, wird der Zugriff zugelassen.</span><span class="sxs-lookup"><span data-stu-id="db713-129">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> <dt>

<span data-ttu-id="db713-130">*Protocolnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-131">Durch Semikolons getrennte Liste der Protokollnamen, die für diese Richtlinie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="db713-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="db713-132">Namen müssen mit der Rückgabe der [**getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) -Methode der Win32-Klasse " [**\_ tgatewayserversettings**](win32-tsgatewayserversettings.md) " identisch sein.</span><span class="sxs-lookup"><span data-stu-id="db713-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="db713-133">*Portnummern* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db713-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db713-134">Durch Semikolons getrennte Liste von Portnummern, die für diese Richtlinie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="db713-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="db713-135">Um eine beliebige Portnummer zuzulassen, legen Sie " \* " fest.</span><span class="sxs-lookup"><span data-stu-id="db713-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db713-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db713-136">Return value</span></span>

<span data-ttu-id="db713-137">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="db713-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="db713-138">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db713-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="db713-139">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="db713-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db713-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db713-140">Remarks</span></span>

<span data-ttu-id="db713-141">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="db713-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="db713-142">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="db713-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="db713-143">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="db713-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="db713-144">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="db713-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="db713-145">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="db713-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="db713-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db713-146">Requirements</span></span>



| <span data-ttu-id="db713-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db713-147">Requirement</span></span> | <span data-ttu-id="db713-148">Wert</span><span class="sxs-lookup"><span data-stu-id="db713-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db713-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db713-149">Minimum supported client</span></span><br/> | <span data-ttu-id="db713-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db713-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="db713-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db713-151">Minimum supported server</span></span><br/> | <span data-ttu-id="db713-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db713-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="db713-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="db713-153">Namespace</span></span><br/>                | <span data-ttu-id="db713-154">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="db713-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="db713-155">MOF</span><span class="sxs-lookup"><span data-stu-id="db713-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db713-156"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="db713-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="db713-157">DLL</span><span class="sxs-lookup"><span data-stu-id="db713-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db713-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db713-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="db713-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db713-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db713-160">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="db713-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

