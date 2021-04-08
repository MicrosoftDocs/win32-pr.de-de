---
title: Removeusergroupnames-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Entfernt die angegebenen Benutzergruppen Namen aus den vorhandenen Benutzergruppen in der usergroupnames-Eigenschaft.
ms.assetid: 4ddbac15-7054-482a-8b5c-49551561673e
ms.tgt_platform: multiple
keywords:
- Removeusergroupnames-Methode Remotedesktopdienste
- Removeusergroupnames-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, removeusergroupnames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e4c3d9556243bcb28167378fea6018b4cd2ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949611"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c1a96-106">Removeusergroupnames-Methode der Win32- \_ Klasse "sgatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="c1a96-106">RemoveUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c1a96-107">Entfernt die angegebenen Benutzergruppen Namen aus den vorhandenen Benutzergruppen in der **usergroupnames** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c1a96-107">Removes specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1a96-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="c1a96-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1a96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a96-110">*Usergroupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1a96-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a96-111">Benutzergruppen Namen, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c1a96-111">User group names to remove.</span></span> <span data-ttu-id="c1a96-112">Benutzergruppen Namen müssen im Format " *Domäne \\ usergroupname*" vorliegen.</span><span class="sxs-lookup"><span data-stu-id="c1a96-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a96-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1a96-113">Return value</span></span>

<span data-ttu-id="c1a96-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c1a96-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c1a96-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1a96-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c1a96-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c1a96-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a96-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1a96-117">Remarks</span></span>

<span data-ttu-id="c1a96-118">Wenn sich mehrere Benutzergruppen Namen im *usergroupnames* -Parameter befinden und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c1a96-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="c1a96-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c1a96-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c1a96-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c1a96-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c1a96-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c1a96-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c1a96-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1a96-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c1a96-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c1a96-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a96-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1a96-124">Requirements</span></span>



| <span data-ttu-id="c1a96-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1a96-125">Requirement</span></span> | <span data-ttu-id="c1a96-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c1a96-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a96-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1a96-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a96-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c1a96-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c1a96-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1a96-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a96-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1a96-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c1a96-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1a96-131">Namespace</span></span><br/>                | <span data-ttu-id="c1a96-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c1a96-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c1a96-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c1a96-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1a96-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="c1a96-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1a96-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c1a96-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1a96-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1a96-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c1a96-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1a96-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a96-138">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="c1a96-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

