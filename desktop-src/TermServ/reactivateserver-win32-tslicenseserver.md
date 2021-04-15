---
title: Reactivateserver-Methode der Win32_TSLicenseServer-Klasse
description: Reaktiviert den Remotedesktop Lizenzserver, indem ein neuer Bezeichner verwendet wird, der über das Telefon oder das Internet abgerufen wurde.
ms.assetid: dd9ff938-a683-4f60-b7cc-7580892953b6
ms.tgt_platform: multiple
keywords:
- Reactivateserver-Methode Remotedesktopdienste
- Reactivateserver-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, reactivateserver-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50e84eb0bed0b52ad463fce50ce334d6c8eb8d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476710"
---
# <a name="reactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f296b-106">Reactivateserver-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="f296b-106">ReactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f296b-107">Reaktiviert den Remotedesktop Lizenzserver, indem ein neuer Bezeichner verwendet wird, der über das Telefon oder das Internet abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f296b-107">Reactivates the Remote Desktop license server by using a new identifier that was obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f296b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f296b-108">Syntax</span></span>


```mof
uint32 ReactivateServer(
  [in]  string sNewLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f296b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f296b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f296b-110">*snewlicenseserverid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f296b-110">*sNewLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f296b-111">Remotedesktop Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f296b-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="f296b-112">*Activationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f296b-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f296b-113">Der zurückgegebene Aktivierungs Status kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="f296b-113">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="f296b-114">0</span><span class="sxs-lookup"><span data-stu-id="f296b-114">0</span></span>
</dt> <dd>

<span data-ttu-id="f296b-115">Der Remotedesktop Lizenzserver wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f296b-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="f296b-116">1</span><span class="sxs-lookup"><span data-stu-id="f296b-116">1</span></span>
</dt> <dd>

<span data-ttu-id="f296b-117">Der Remotedesktop Lizenzserver ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f296b-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="f296b-118">2</span><span class="sxs-lookup"><span data-stu-id="f296b-118">2</span></span>
</dt> <dd>

<span data-ttu-id="f296b-119">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f296b-119">An unknown error occurred.</span></span> <span data-ttu-id="f296b-120">Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f296b-120">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f296b-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f296b-121">Return value</span></span>

<span data-ttu-id="f296b-122">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f296b-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f296b-123">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f296b-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f296b-124">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f296b-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f296b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f296b-125">Remarks</span></span>

<span data-ttu-id="f296b-126">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f296b-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f296b-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f296b-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f296b-128">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f296b-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f296b-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f296b-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f296b-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f296b-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f296b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f296b-131">Requirements</span></span>



| <span data-ttu-id="f296b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f296b-132">Requirement</span></span> | <span data-ttu-id="f296b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f296b-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f296b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f296b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f296b-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f296b-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f296b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f296b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f296b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f296b-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f296b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="f296b-138">Namespace</span></span><br/>                | <span data-ttu-id="f296b-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f296b-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f296b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f296b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f296b-141"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f296b-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f296b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f296b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f296b-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f296b-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f296b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f296b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f296b-145">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="f296b-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

