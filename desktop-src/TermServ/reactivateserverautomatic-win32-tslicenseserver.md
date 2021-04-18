---
title: Reactivateserverautomatic-Methode der Win32_TSLicenseServer-Klasse
description: Reaktiviert den Remotedesktop Lizenzserver über eine automatische Internet Verbindung.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Reactivateserverautomatic-Methode Remotedesktopdienste
- Reactivateserverautomatic-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, reactivateserverautomatic-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344711"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="ef3bf-106">Reactivateserverautomatic-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="ef3bf-106">ReactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="ef3bf-107">Reaktiviert den Remotedesktop Lizenzserver über eine automatische Internet Verbindung.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-107">Reactivates the Remote Desktop license server by using an automatic connection to the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef3bf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef3bf-108">Syntax</span></span>


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="ef3bf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef3bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef3bf-110">*Grund* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef3bf-110">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-111">Grund für die Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-111">Reason for the activation.</span></span> <span data-ttu-id="ef3bf-112">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-112">It can be one of the following values.</span></span>

<dt>

<span data-ttu-id="ef3bf-113">0</span><span class="sxs-lookup"><span data-stu-id="ef3bf-113">0</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-114">Der Server wurde erneut bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-114">The server was redeployed.</span></span>

</dd> <dt>

<span data-ttu-id="ef3bf-115">1</span><span class="sxs-lookup"><span data-stu-id="ef3bf-115">1</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-116">Das Zertifikat ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-116">The certificate was corrupt.</span></span>

</dd> <dt>

<span data-ttu-id="ef3bf-117">2</span><span class="sxs-lookup"><span data-stu-id="ef3bf-117">2</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-118">Der private Schlüssel wurde kompromittiert.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-118">The private key was compromised.</span></span>

</dd> <dt>

<span data-ttu-id="ef3bf-119">3</span><span class="sxs-lookup"><span data-stu-id="ef3bf-119">3</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-120">Der Aktivierungsschlüssel ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-120">The activation key expired.</span></span>

</dd> <dt>

<span data-ttu-id="ef3bf-121">4</span><span class="sxs-lookup"><span data-stu-id="ef3bf-121">4</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-122">Der Server wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-122">The server was upgraded.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ef3bf-123">*Activationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ef3bf-123">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-124">Der zurückgegebene Aktivierungs Status kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-124">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="ef3bf-125">0</span><span class="sxs-lookup"><span data-stu-id="ef3bf-125">0</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-126">Der Remotedesktop Lizenzserver wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-126">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="ef3bf-127">1</span><span class="sxs-lookup"><span data-stu-id="ef3bf-127">1</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-128">Der Remotedesktop Lizenzserver ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-128">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="ef3bf-129">2</span><span class="sxs-lookup"><span data-stu-id="ef3bf-129">2</span></span>
</dt> <dd>

<span data-ttu-id="ef3bf-130">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-130">An unknown error occurred.</span></span> <span data-ttu-id="ef3bf-131">Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-131">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef3bf-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef3bf-132">Return value</span></span>

<span data-ttu-id="ef3bf-133">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-133">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ef3bf-134">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-134">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ef3bf-135">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ef3bf-135">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef3bf-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef3bf-136">Remarks</span></span>

<span data-ttu-id="ef3bf-137">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-137">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ef3bf-138">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ef3bf-139">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ef3bf-140">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ef3bf-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ef3bf-141">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ef3bf-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef3bf-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef3bf-142">Requirements</span></span>



| <span data-ttu-id="ef3bf-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef3bf-143">Requirement</span></span> | <span data-ttu-id="ef3bf-144">Wert</span><span class="sxs-lookup"><span data-stu-id="ef3bf-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3bf-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef3bf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ef3bf-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ef3bf-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ef3bf-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef3bf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ef3bf-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef3bf-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ef3bf-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef3bf-149">Namespace</span></span><br/>                | <span data-ttu-id="ef3bf-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ef3bf-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ef3bf-151">MOF</span><span class="sxs-lookup"><span data-stu-id="ef3bf-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef3bf-152"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ef3bf-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef3bf-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ef3bf-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef3bf-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef3bf-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef3bf-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef3bf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef3bf-156">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="ef3bf-156">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

