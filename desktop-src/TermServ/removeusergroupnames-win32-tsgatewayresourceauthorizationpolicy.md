---
title: Removeusergroupnames-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Entfernt die angegebenen Benutzergruppen Namen aus den vorhandenen Benutzergruppen in der usergroupnames-Eigenschaft.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Removeusergroupnames-Methode Remotedesktopdienste
- Removeusergroupnames-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, removeusergroupnames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342430"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="b708c-106">Removeusergroupnames-Methode der Win32- \_ Klasse "zgatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="b708c-106">RemoveUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="b708c-107">Entfernt die angegebenen Benutzergruppen Namen aus den vorhandenen Benutzergruppen in der **usergroupnames** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b708c-107">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b708c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b708c-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="b708c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b708c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b708c-110">*Usergroupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b708c-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b708c-111">Durch Semikolons getrennte Liste von Benutzergruppen Namen.</span><span class="sxs-lookup"><span data-stu-id="b708c-111">Semicolon-separated list of user group names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b708c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b708c-112">Return value</span></span>

<span data-ttu-id="b708c-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b708c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b708c-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b708c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b708c-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b708c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b708c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b708c-116">Remarks</span></span>

<span data-ttu-id="b708c-117">Wenn sich mehrere Benutzergruppen Namen im *usergroupnames* -Parameter befinden und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b708c-117">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="b708c-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b708c-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b708c-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b708c-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b708c-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b708c-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b708c-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b708c-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b708c-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b708c-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b708c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b708c-123">Requirements</span></span>



| <span data-ttu-id="b708c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b708c-124">Requirement</span></span> | <span data-ttu-id="b708c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b708c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b708c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b708c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b708c-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b708c-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b708c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b708c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b708c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b708c-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b708c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b708c-130">Namespace</span></span><br/>                | <span data-ttu-id="b708c-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b708c-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b708c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b708c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b708c-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b708c-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b708c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b708c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b708c-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b708c-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b708c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b708c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b708c-137">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="b708c-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

