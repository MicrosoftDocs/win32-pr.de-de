---
title: Aktualisierungscontext-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktualisiert das Zertifikat, das vom Remotedesktop Gateway-Server (RD-Gateway) verwendet wird.
ms.assetid: caefeb85-1c7a-4868-9ee8-10ab09354595
ms.tgt_platform: multiple
keywords:
- Aktualisierungscontext-Methode Remotedesktopdienste
- Aktualisierungscontext-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, aktualisierungscontext-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RefreshCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b03d77fff9574b0aff577d8ff45b54f57758f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391848"
---
# <a name="refreshcertcontext-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="d31b0-106">Aktualisierungscontext-Methode der Win32- \_ Klasse "tgatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="d31b0-106">RefreshCertContext method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="d31b0-107">Aktualisiert das Zertifikat, das vom Remotedesktop Gateway-Server (RD-Gateway) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d31b0-107">Refreshes the certificate that is used by the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31b0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d31b0-108">Syntax</span></span>


```mof
uint32 RefreshCertContext(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="d31b0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d31b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d31b0-110">*CertHash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d31b0-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d31b0-111">Der Hash des Zertifikats, das vom RD-Gateway Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d31b0-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d31b0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d31b0-112">Return value</span></span>

<span data-ttu-id="d31b0-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d31b0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d31b0-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d31b0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d31b0-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d31b0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d31b0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d31b0-116">Remarks</span></span>

<span data-ttu-id="d31b0-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d31b0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d31b0-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="d31b0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d31b0-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="d31b0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d31b0-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d31b0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d31b0-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d31b0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d31b0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d31b0-122">Requirements</span></span>



| <span data-ttu-id="d31b0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d31b0-123">Requirement</span></span> | <span data-ttu-id="d31b0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d31b0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d31b0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d31b0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d31b0-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d31b0-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d31b0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d31b0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d31b0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d31b0-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d31b0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="d31b0-129">Namespace</span></span><br/>                | <span data-ttu-id="d31b0-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d31b0-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d31b0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d31b0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d31b0-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="d31b0-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d31b0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d31b0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d31b0-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d31b0-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d31b0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d31b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31b0-136">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="d31b0-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

