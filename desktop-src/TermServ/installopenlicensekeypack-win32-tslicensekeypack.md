---
title: Installopenlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Open License Remotedesktopdienste License Key Pack.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Installopenlicenskeypack-Methode Remotedesktopdienste
- Installopenlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, installopenlicenabkeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475945"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="61993-106">Installopenlicenerkeypack-Methode der Win32-Klasse "-Klasse". \_</span><span class="sxs-lookup"><span data-stu-id="61993-106">InstallOpenLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="61993-107">Installiert ein Open License Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="61993-107">Installs an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="61993-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="61993-108">Syntax</span></span>


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="61993-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="61993-109">Parameters</span></span>

<span data-ttu-id="61993-110">*slicensenum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61993-110">*sLicenseNumber* \[in\]</span></span>

<span data-ttu-id="61993-111">numerische Zeichenfolge mit 8 Zeichen, die mit dem Lizenzschlüssel Paket bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="61993-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="61993-112">Der *slicensenreber* -Parameter darf keine Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="61993-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="61993-113">*sauthorizationnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61993-113">*sAuthorizationNumber* \[in\]</span></span>

<span data-ttu-id="61993-114">eine alphanumerische Zeichenfolge mit 15 Zeichen, die mit dem Lizenzschlüssel bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="61993-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="61993-115">Der *sauthorizationnumber* -Parameter darf keine Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="61993-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="61993-116">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61993-116">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="61993-117">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="61993-117">Product version.</span></span>

| <span data-ttu-id="61993-118">Wert</span><span class="sxs-lookup"><span data-stu-id="61993-118">Value</span></span> | <span data-ttu-id="61993-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61993-119">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="61993-120">0</span><span class="sxs-lookup"><span data-stu-id="61993-120">0</span></span> | <span data-ttu-id="61993-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="61993-121">Not supported</span></span> |
| <span data-ttu-id="61993-122">1</span><span class="sxs-lookup"><span data-stu-id="61993-122">1</span></span> | <span data-ttu-id="61993-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="61993-123">Not supported</span></span> |
| <span data-ttu-id="61993-124">2</span><span class="sxs-lookup"><span data-stu-id="61993-124">2</span></span> | <span data-ttu-id="61993-125">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61993-125">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="61993-126">4</span><span class="sxs-lookup"><span data-stu-id="61993-126">4</span></span> | <span data-ttu-id="61993-127">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="61993-127">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="61993-128">5</span><span class="sxs-lookup"><span data-stu-id="61993-128">5</span></span> | <span data-ttu-id="61993-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="61993-129">Windows Server 2016</span></span> |
| <span data-ttu-id="61993-130">6</span><span class="sxs-lookup"><span data-stu-id="61993-130">6</span></span> | <span data-ttu-id="61993-131">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="61993-131">Windows Server 2019</span></span> |

<span data-ttu-id="61993-132">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61993-132">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61993-133">Produkttyp.</span><span class="sxs-lookup"><span data-stu-id="61993-133">Product type.</span></span>

| <span data-ttu-id="61993-134">Wert</span><span class="sxs-lookup"><span data-stu-id="61993-134">Value</span></span> | <span data-ttu-id="61993-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61993-135">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="61993-136">0</span><span class="sxs-lookup"><span data-stu-id="61993-136">0</span></span> | <span data-ttu-id="61993-137">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="61993-137">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="61993-138">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="61993-138">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="61993-139">1</span><span class="sxs-lookup"><span data-stu-id="61993-139">1</span></span> | <span data-ttu-id="61993-140">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="61993-140">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="61993-141">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="61993-141">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="61993-142">2</span><span class="sxs-lookup"><span data-stu-id="61993-142">2</span></span> | <span data-ttu-id="61993-143">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="61993-143">This product type is not valid.</span></span> |

<span data-ttu-id="61993-144">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61993-144">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="61993-145">Die Anzahl der zu installierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="61993-145">The number of licenses to install.</span></span>

<span data-ttu-id="61993-146">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="61993-146">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="61993-147">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="61993-147">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="61993-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61993-148">Return value</span></span>

<span data-ttu-id="61993-149">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="61993-149">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="61993-150">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61993-150">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="61993-151">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="61993-151">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61993-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61993-152">Remarks</span></span>

<span data-ttu-id="61993-153">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="61993-153">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="61993-154">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="61993-154">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="61993-155">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="61993-155">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="61993-156">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="61993-156">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="61993-157">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="61993-157">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="61993-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61993-158">Requirements</span></span>



| <span data-ttu-id="61993-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61993-159">Requirement</span></span> | <span data-ttu-id="61993-160">Wert</span><span class="sxs-lookup"><span data-stu-id="61993-160">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="61993-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61993-161">Minimum supported client</span></span><br/> | <span data-ttu-id="61993-162">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="61993-162">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="61993-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61993-163">Minimum supported server</span></span><br/> | <span data-ttu-id="61993-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61993-164">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="61993-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="61993-165">Namespace</span></span><br/>                | <span data-ttu-id="61993-166">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="61993-166">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="61993-167">MOF</span><span class="sxs-lookup"><span data-stu-id="61993-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61993-168"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="61993-168"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="61993-169">DLL</span><span class="sxs-lookup"><span data-stu-id="61993-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61993-170"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61993-170"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61993-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61993-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61993-172">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="61993-172">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

