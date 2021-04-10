---
title: Setusergroupnames-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt die usergroupnames-Eigenschaft für die Remotedesktop-Ressourcen Autorisierungs Richtlinie fest (RD \ 160; Rap).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Setusergroupnames-Methode Remotedesktopdienste
- Setusergroupnames-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, setusergroupnames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104289"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="93edf-106">Setusergroupnames-Methode der Win32- \_ Klasse "zgatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="93edf-106">SetUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="93edf-107">Legt die **usergroupnames** -Eigenschaft für die Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP) fest.</span><span class="sxs-lookup"><span data-stu-id="93edf-107">Sets the **UserGroupNames** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="93edf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="93edf-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="93edf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="93edf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93edf-110">*Usergroupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93edf-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93edf-111">Durch Semikolons getrennte Liste von Benutzergruppen Namen.</span><span class="sxs-lookup"><span data-stu-id="93edf-111">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="93edf-112">Die Namen weisen das Format *Domäne \\ usergroupname* auf.</span><span class="sxs-lookup"><span data-stu-id="93edf-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="93edf-113">Wenn der Benutzer zu einer dieser Benutzergruppen gehört, wird der Zugriff zugelassen.</span><span class="sxs-lookup"><span data-stu-id="93edf-113">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93edf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93edf-114">Return value</span></span>

<span data-ttu-id="93edf-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="93edf-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="93edf-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="93edf-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="93edf-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="93edf-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="93edf-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93edf-118">Remarks</span></span>

<span data-ttu-id="93edf-119">Wenn sich mehrere Benutzergruppen Namen im *usergroupnames* -Parameter befinden und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="93edf-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="93edf-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="93edf-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="93edf-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="93edf-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93edf-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="93edf-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="93edf-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="93edf-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93edf-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="93edf-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="93edf-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93edf-125">Requirements</span></span>



| <span data-ttu-id="93edf-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93edf-126">Requirement</span></span> | <span data-ttu-id="93edf-127">Wert</span><span class="sxs-lookup"><span data-stu-id="93edf-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93edf-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93edf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93edf-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="93edf-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="93edf-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93edf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93edf-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93edf-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="93edf-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="93edf-132">Namespace</span></span><br/>                | <span data-ttu-id="93edf-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="93edf-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="93edf-134">MOF</span><span class="sxs-lookup"><span data-stu-id="93edf-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93edf-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="93edf-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="93edf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="93edf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93edf-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93edf-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="93edf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93edf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93edf-139">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="93edf-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

