---
title: SetName-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Legt die Name-Eigenschaft für diesen Remote Authentication Dial-in User Service Server (RADIUS) fest.
ms.assetid: 2dabc6fb-7740-4039-9bbd-5b2490fe5988
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste, Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste, SetName-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4b563c59ce1546b4cf471653407e3390676625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741481"
---
# <a name="setname-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="06cd1-106">SetName-Methode der Win32- \_ Klasse "tgatewayradiusserver"</span><span class="sxs-lookup"><span data-stu-id="06cd1-106">SetName method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="06cd1-107">Legt die **Name** -Eigenschaft für diesen Remote Authentication Dial-in User Service Server (RADIUS) fest.</span><span class="sxs-lookup"><span data-stu-id="06cd1-107">Sets the **Name** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cd1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06cd1-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="06cd1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="06cd1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cd1-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06cd1-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cd1-111">Neuer Name.</span><span class="sxs-lookup"><span data-stu-id="06cd1-111">New name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06cd1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06cd1-112">Return value</span></span>

<span data-ttu-id="06cd1-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="06cd1-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="06cd1-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06cd1-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="06cd1-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="06cd1-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06cd1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06cd1-116">Remarks</span></span>

<span data-ttu-id="06cd1-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="06cd1-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="06cd1-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="06cd1-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="06cd1-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="06cd1-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="06cd1-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="06cd1-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="06cd1-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="06cd1-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="06cd1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06cd1-122">Requirements</span></span>



| <span data-ttu-id="06cd1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06cd1-123">Requirement</span></span> | <span data-ttu-id="06cd1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="06cd1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06cd1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06cd1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="06cd1-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="06cd1-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="06cd1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06cd1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="06cd1-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06cd1-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="06cd1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="06cd1-129">Namespace</span></span><br/>                | <span data-ttu-id="06cd1-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="06cd1-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="06cd1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="06cd1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06cd1-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="06cd1-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="06cd1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="06cd1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06cd1-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06cd1-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="06cd1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06cd1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cd1-136">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="06cd1-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

