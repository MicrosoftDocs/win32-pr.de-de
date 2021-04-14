---
title: Remove-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Entfernt den aktuellen Remote Authentication Dial-in User Service Server (RADIUS).
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Remove-Methode Remotedesktopdienste
- Remove-Methode Remotedesktopdienste, Win32_TSGatewayRADIUSServer-Schnittstelle
- Win32_TSGatewayRADIUSServer Schnittstellen Remotedesktopdienste, Methode entfernen
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a91fc4a3ba8bf638dcffd76e3bf3517795674fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341107"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="d32b9-106">Remove-Methode der Win32-Klasse "t- \_ gatewayradiusserver"</span><span class="sxs-lookup"><span data-stu-id="d32b9-106">Remove method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="d32b9-107">Entfernt den aktuellen Remote Authentication Dial-in User Service Server (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="d32b9-107">Removes the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d32b9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d32b9-108">Syntax</span></span>


```mof
uint32 Remove();
```



## <a name="parameters"></a><span data-ttu-id="d32b9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d32b9-109">Parameters</span></span>

<span data-ttu-id="d32b9-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d32b9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d32b9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d32b9-111">Return value</span></span>

<span data-ttu-id="d32b9-112">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d32b9-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d32b9-113">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d32b9-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d32b9-114">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d32b9-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d32b9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d32b9-115">Remarks</span></span>

<span data-ttu-id="d32b9-116">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d32b9-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d32b9-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="d32b9-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d32b9-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="d32b9-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d32b9-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d32b9-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d32b9-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d32b9-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d32b9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d32b9-121">Requirements</span></span>



| <span data-ttu-id="d32b9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d32b9-122">Requirement</span></span> | <span data-ttu-id="d32b9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d32b9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32b9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d32b9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d32b9-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d32b9-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d32b9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d32b9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d32b9-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d32b9-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d32b9-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d32b9-128">Namespace</span></span><br/>                | <span data-ttu-id="d32b9-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d32b9-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d32b9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d32b9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d32b9-131"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="d32b9-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d32b9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d32b9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d32b9-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d32b9-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d32b9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d32b9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d32b9-135">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="d32b9-135">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

