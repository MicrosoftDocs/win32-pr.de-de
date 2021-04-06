---
title: Setsharedsecret-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Legt die sharedsecret-Eigenschaft für diesen Remote Authentication Dial-in User Service Server (RADIUS) fest.
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Setsharedsecret-Methode Remotedesktopdienste
- Setsharedsecret-Methode Remotedesktopdienste, Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste, setsharedsecret-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742368"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="5d554-106">Setsharedsecret-Methode der Win32- \_ Klasse "segatewayradiusserver"</span><span class="sxs-lookup"><span data-stu-id="5d554-106">SetSharedSecret method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="5d554-107">Legt die **sharedsecret** -Eigenschaft für diesen Remote Authentication Dial-in User Service Server (RADIUS) fest.</span><span class="sxs-lookup"><span data-stu-id="5d554-107">Sets the **SharedSecret** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d554-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d554-108">Syntax</span></span>


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="5d554-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d554-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d554-110">*Sharedsecret* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d554-110">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d554-111">Neuer gemeinsamer geheimer Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5d554-111">New shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d554-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d554-112">Return value</span></span>

<span data-ttu-id="5d554-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5d554-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5d554-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d554-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5d554-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5d554-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d554-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d554-116">Remarks</span></span>

<span data-ttu-id="5d554-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d554-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5d554-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5d554-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5d554-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5d554-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5d554-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5d554-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5d554-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5d554-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d554-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d554-122">Requirements</span></span>



| <span data-ttu-id="5d554-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d554-123">Requirement</span></span> | <span data-ttu-id="5d554-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5d554-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d554-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d554-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5d554-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5d554-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5d554-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d554-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5d554-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d554-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5d554-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d554-129">Namespace</span></span><br/>                | <span data-ttu-id="5d554-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5d554-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5d554-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5d554-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d554-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="5d554-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d554-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5d554-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d554-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d554-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5d554-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d554-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d554-136">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="5d554-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

