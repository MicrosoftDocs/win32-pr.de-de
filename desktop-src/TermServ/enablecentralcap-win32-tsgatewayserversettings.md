---
title: Enablecentralcap-Methode der Win32_TSGatewayServerSettings-Klasse
description: Steuert die centralcapaktivierte-Eigenschaft, die die Remotedesktopdienste Verbindungs Autorisierungs Richtlinien steuert (RD \ 160; Caps) für den Remotedesktop Gateway-Server (RD-Gateway).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Enablecentralcap-Methode Remotedesktopdienste
- Enablecentralcap-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enablecentralcap-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392229"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="30fc6-106">Enablecentralcap-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="30fc6-106">EnableCentralCAP method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="30fc6-107">Steuert die **centralcapaktivierte** -Eigenschaft, die die Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) für den Remotedesktop Gateway (RD-Gateway)-Server steuert.</span><span class="sxs-lookup"><span data-stu-id="30fc6-107">Controls the **CentralCAPEnabled** property, which controls the Remote Desktop Services connection authorization policies (RD CAPs) for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="30fc6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30fc6-108">Syntax</span></span>


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="30fc6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30fc6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30fc6-110">*Centralcapaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30fc6-110">*CentralCAPEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30fc6-111">Wenn diese Einstellung auf **true** festgelegt ist, werden RD-CAPs von zentralen RD-CAP-Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="30fc6-111">If set to **True**, RD CAPs from central RD CAP servers will be used.</span></span> <span data-ttu-id="30fc6-112">Wenn diese Einstellung auf " **false**" festgelegt ist, werden nur Richtlinien vom lokalen Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="30fc6-112">If set to **False**, only policies from the local server will be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30fc6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30fc6-113">Return value</span></span>

<span data-ttu-id="30fc6-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="30fc6-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="30fc6-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30fc6-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="30fc6-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="30fc6-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30fc6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30fc6-117">Remarks</span></span>

<span data-ttu-id="30fc6-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="30fc6-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="30fc6-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="30fc6-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="30fc6-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="30fc6-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="30fc6-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="30fc6-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="30fc6-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="30fc6-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="30fc6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30fc6-123">Requirements</span></span>



| <span data-ttu-id="30fc6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30fc6-124">Requirement</span></span> | <span data-ttu-id="30fc6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="30fc6-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fc6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30fc6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="30fc6-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="30fc6-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="30fc6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30fc6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="30fc6-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30fc6-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="30fc6-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="30fc6-130">Namespace</span></span><br/>                | <span data-ttu-id="30fc6-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="30fc6-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="30fc6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="30fc6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30fc6-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="30fc6-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="30fc6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="30fc6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30fc6-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30fc6-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="30fc6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30fc6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30fc6-137">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="30fc6-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

