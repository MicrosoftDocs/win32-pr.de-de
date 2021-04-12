---
title: SetCertificate-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt den Zertifikat Hash für die HTTPS-Bindung an Port 443 in IIS fest.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- SetCertificate-Methode Remotedesktopdienste
- SetCertificate-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, SetCertificate-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1da7e3abcca671b0c8bf70461c77d56e68cf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105848"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="750a0-106">SetCertificate-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="750a0-106">SetCertificate method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="750a0-107">Legt den Zertifikat Hash für die HTTPS-Bindung an Port 443 in IIS fest.</span><span class="sxs-lookup"><span data-stu-id="750a0-107">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="750a0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="750a0-108">Syntax</span></span>


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="750a0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="750a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750a0-110">*CertHash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="750a0-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="750a0-111">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="750a0-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="750a0-112">Der neue Zertifikat Hash.</span><span class="sxs-lookup"><span data-stu-id="750a0-112">The new certificate hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750a0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="750a0-113">Return value</span></span>

<span data-ttu-id="750a0-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="750a0-114">Type: **uint32**</span></span>

<span data-ttu-id="750a0-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="750a0-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="750a0-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="750a0-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="750a0-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="750a0-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="750a0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="750a0-118">Remarks</span></span>

<span data-ttu-id="750a0-119">Nachdem der Zertifikat Hash mit dieser Methode festgelegt wurde, müssen Sie die [**configure**](configure-win32-tsgatewayserversettings.md) -Methode zum Ausführen des Konfigurations Vorgangs abrufen.</span><span class="sxs-lookup"><span data-stu-id="750a0-119">After the certificate hash has been set with this method, you must call the [**Configure**](configure-win32-tsgatewayserversettings.md) method to complete the configuration process.</span></span>

<span data-ttu-id="750a0-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="750a0-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="750a0-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="750a0-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="750a0-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="750a0-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="750a0-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="750a0-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="750a0-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="750a0-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="750a0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="750a0-125">Requirements</span></span>



| <span data-ttu-id="750a0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="750a0-126">Requirement</span></span> | <span data-ttu-id="750a0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="750a0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="750a0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="750a0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="750a0-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="750a0-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="750a0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="750a0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="750a0-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="750a0-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="750a0-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="750a0-132">Namespace</span></span><br/>                | <span data-ttu-id="750a0-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="750a0-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="750a0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="750a0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="750a0-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="750a0-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="750a0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="750a0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="750a0-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="750a0-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="750a0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="750a0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750a0-139">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="750a0-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

