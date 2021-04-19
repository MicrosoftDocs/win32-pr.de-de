---
title: Activateserver-Methode der Win32_TSLicenseServer-Klasse
description: Aktiviert den Remotedesktop Lizenzserver mit einer Remotedesktop-Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wird.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Activateserver-Methode Remotedesktopdienste
- Activateserver-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, activateserver-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343057"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="73a67-106">Activateserver-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="73a67-106">ActivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="73a67-107">Aktiviert den Remotedesktop Lizenzserver mit einer Remotedesktop-Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="73a67-107">Activates the Remote Desktop license server by using a Remote Desktop license server identifier that is obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a67-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="73a67-108">Syntax</span></span>


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="73a67-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="73a67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a67-110">*slicenseserverid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73a67-110">*sLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a67-111">Remotedesktop Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="73a67-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span> <span data-ttu-id="73a67-112">Der *slicenseserverid* -Parameter ist eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="73a67-112">The *sLicenseServerId* parameter is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="73a67-113">*Activationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73a67-113">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73a67-114">Der zurückgegebene Aktivierungs Status kann einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="73a67-114">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="73a67-115">0</span><span class="sxs-lookup"><span data-stu-id="73a67-115">0</span></span>
</dt> <dd>

<span data-ttu-id="73a67-116">Der Remotedesktop Lizenzserver wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="73a67-116">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="73a67-117">1</span><span class="sxs-lookup"><span data-stu-id="73a67-117">1</span></span>
</dt> <dd>

<span data-ttu-id="73a67-118">Der Remotedesktop Lizenzserver ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="73a67-118">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="73a67-119">2</span><span class="sxs-lookup"><span data-stu-id="73a67-119">2</span></span>
</dt> <dd>

<span data-ttu-id="73a67-120">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="73a67-120">An unknown error occurred.</span></span> <span data-ttu-id="73a67-121">Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="73a67-121">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73a67-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73a67-122">Return value</span></span>

<span data-ttu-id="73a67-123">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="73a67-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="73a67-124">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="73a67-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="73a67-125">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="73a67-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="73a67-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73a67-126">Remarks</span></span>

<span data-ttu-id="73a67-127">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="73a67-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="73a67-128">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="73a67-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73a67-129">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="73a67-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73a67-130">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="73a67-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73a67-131">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="73a67-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73a67-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73a67-132">Requirements</span></span>



| <span data-ttu-id="73a67-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73a67-133">Requirement</span></span> | <span data-ttu-id="73a67-134">Wert</span><span class="sxs-lookup"><span data-stu-id="73a67-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a67-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73a67-135">Minimum supported client</span></span><br/> | <span data-ttu-id="73a67-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="73a67-136">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="73a67-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73a67-137">Minimum supported server</span></span><br/> | <span data-ttu-id="73a67-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73a67-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="73a67-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="73a67-139">Namespace</span></span><br/>                | <span data-ttu-id="73a67-140">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="73a67-140">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="73a67-141">MOF</span><span class="sxs-lookup"><span data-stu-id="73a67-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73a67-142"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="73a67-142"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="73a67-143">DLL</span><span class="sxs-lookup"><span data-stu-id="73a67-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73a67-144"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73a67-144"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a67-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73a67-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a67-146">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="73a67-146">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

