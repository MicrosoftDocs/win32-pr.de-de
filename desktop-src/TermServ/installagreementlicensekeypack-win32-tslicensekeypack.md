---
title: Installagreementlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Installagreementlicenskeypack-Methode Remotedesktopdienste
- Installagreementlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, installagreementlicenerkeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340369"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="f6226-106">Installagreementlicenskeypack-Methode der Win32- \_ Klasse "plicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="f6226-106">InstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="f6226-107">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f6226-107">Installs a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6226-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6226-108">Syntax</span></span>


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="f6226-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6226-109">Parameters</span></span>

<span data-ttu-id="f6226-110">*Agreementtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6226-110">*AgreementType* \[in\]</span></span>

<span data-ttu-id="f6226-111">Vertragstyp.</span><span class="sxs-lookup"><span data-stu-id="f6226-111">Agreement type.</span></span>

| <span data-ttu-id="f6226-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f6226-112">Value</span></span> | <span data-ttu-id="f6226-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6226-113">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f6226-114">0</span><span class="sxs-lookup"><span data-stu-id="f6226-114">0</span></span> | <span data-ttu-id="f6226-115">Das Lizenzschlüssel Paket wird von einem SELECT-Volumenlizenzvertrag (für Kunden mit 250 oder mehr Computern) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f6226-115">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="f6226-116">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="f6226-116">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="f6226-117">1</span><span class="sxs-lookup"><span data-stu-id="f6226-117">1</span></span> | <span data-ttu-id="f6226-118">Das Lizenzschlüssel Paket basiert auf einem Enterprise-Volumenlizenzvertrag für Kunden mit 250 oder mehr Computern.</span><span class="sxs-lookup"><span data-stu-id="f6226-118">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="f6226-119">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="f6226-119">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="f6226-120">2</span><span class="sxs-lookup"><span data-stu-id="f6226-120">2</span></span> | <span data-ttu-id="f6226-121">Das Lizenzschlüssel Paket basiert auf einem Campus-Volumenlizenzvertrag für eine höhere Bildungseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="f6226-121">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="f6226-122">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="f6226-122">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="f6226-123">3</span><span class="sxs-lookup"><span data-stu-id="f6226-123">3</span></span> | <span data-ttu-id="f6226-124">Das Lizenzschlüssel Paket wird von einem Schul-Volumenlizenzvertrag für primäre und sekundäre Einrichtungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f6226-124">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="f6226-125">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="f6226-125">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="f6226-126">4</span><span class="sxs-lookup"><span data-stu-id="f6226-126">4</span></span> | <span data-ttu-id="f6226-127">Das Lizenzschlüssel Paket wird von einem Dienstanbieter-Lizenzvertrag für Dienstanbieter zum Lizenzieren von Microsoft-Software auf monatlicher Basis.</span><span class="sxs-lookup"><span data-stu-id="f6226-127">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="f6226-128">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="f6226-128">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="f6226-129">5</span><span class="sxs-lookup"><span data-stu-id="f6226-129">5</span></span> | <span data-ttu-id="f6226-130">Das Lizenzschlüssel Paket ist aus einem anderen Lizenzvertrag, wie z. b. Open Value, Open-Year-Lizenz und Open-Abonnement-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="f6226-130">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="f6226-131">Der *sagreementnumber* -Parameter ist die Vertragsnummer, die mit ihren Programminformationen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6226-131">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span> |

<span data-ttu-id="f6226-132">*sagreementnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6226-132">*sAgreementNumber* \[in\]</span></span>

<span data-ttu-id="f6226-133">Vertragsnummer oder Registrierungsnummer.</span><span class="sxs-lookup"><span data-stu-id="f6226-133">Agreement number or enrollment number.</span></span> <span data-ttu-id="f6226-134">Der *sagreementnumber* -Parameter ist eine siebenstellige numerische Zeichenfolge ohne Bindestriche.</span><span class="sxs-lookup"><span data-stu-id="f6226-134">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

<span data-ttu-id="f6226-135">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6226-135">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="f6226-136">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="f6226-136">Product version.</span></span>

| <span data-ttu-id="f6226-137">Wert</span><span class="sxs-lookup"><span data-stu-id="f6226-137">Value</span></span> | <span data-ttu-id="f6226-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6226-138">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f6226-139">0</span><span class="sxs-lookup"><span data-stu-id="f6226-139">0</span></span> | <span data-ttu-id="f6226-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6226-140">Not supported</span></span> |
| <span data-ttu-id="f6226-141">1</span><span class="sxs-lookup"><span data-stu-id="f6226-141">1</span></span> | <span data-ttu-id="f6226-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6226-142">Not supported</span></span> |
| <span data-ttu-id="f6226-143">2</span><span class="sxs-lookup"><span data-stu-id="f6226-143">2</span></span> | <span data-ttu-id="f6226-144">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6226-144">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="f6226-145">4</span><span class="sxs-lookup"><span data-stu-id="f6226-145">4</span></span> | <span data-ttu-id="f6226-146">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f6226-146">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="f6226-147">5</span><span class="sxs-lookup"><span data-stu-id="f6226-147">5</span></span> | <span data-ttu-id="f6226-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f6226-148">Windows Server 2016</span></span> |
| <span data-ttu-id="f6226-149">6</span><span class="sxs-lookup"><span data-stu-id="f6226-149">6</span></span> | <span data-ttu-id="f6226-150">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="f6226-150">Windows Server 2019</span></span> |

<span data-ttu-id="f6226-151">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6226-151">*ProductType* \[in\]</span></span>

<span data-ttu-id="f6226-152">Produkttyp.</span><span class="sxs-lookup"><span data-stu-id="f6226-152">Product type.</span></span>

| <span data-ttu-id="f6226-153">Wert</span><span class="sxs-lookup"><span data-stu-id="f6226-153">Value</span></span> | <span data-ttu-id="f6226-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6226-154">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f6226-155">0</span><span class="sxs-lookup"><span data-stu-id="f6226-155">0</span></span> | <span data-ttu-id="f6226-156">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="f6226-156">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="f6226-157">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="f6226-157">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="f6226-158">1</span><span class="sxs-lookup"><span data-stu-id="f6226-158">1</span></span> | <span data-ttu-id="f6226-159">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f6226-159">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="f6226-160">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="f6226-160">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="f6226-161">2</span><span class="sxs-lookup"><span data-stu-id="f6226-161">2</span></span> | <span data-ttu-id="f6226-162">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f6226-162">This product type is not valid.</span></span> |

<span data-ttu-id="f6226-163">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6226-163">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="f6226-164">Anzahl der zu installierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="f6226-164">Number of licenses to install.</span></span>

<span data-ttu-id="f6226-165">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f6226-165">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="f6226-166">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f6226-166">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6226-167">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6226-167">Return value</span></span>

<span data-ttu-id="f6226-168">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f6226-168">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f6226-169">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6226-169">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f6226-170">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f6226-170">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6226-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6226-171">Remarks</span></span>

<span data-ttu-id="f6226-172">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f6226-172">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f6226-173">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f6226-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f6226-174">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f6226-174">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f6226-175">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6226-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f6226-176">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f6226-176">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6226-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6226-177">Requirements</span></span>

| <span data-ttu-id="f6226-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6226-178">Requirement</span></span> | <span data-ttu-id="f6226-179">Wert</span><span class="sxs-lookup"><span data-stu-id="f6226-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6226-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6226-180">Minimum supported client</span></span><br/> | <span data-ttu-id="f6226-181">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6226-181">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f6226-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6226-182">Minimum supported server</span></span><br/> | <span data-ttu-id="f6226-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6226-183">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f6226-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6226-184">Namespace</span></span><br/>                | <span data-ttu-id="f6226-185">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f6226-185">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f6226-186">MOF</span><span class="sxs-lookup"><span data-stu-id="f6226-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6226-187"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6226-187"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6226-188">DLL</span><span class="sxs-lookup"><span data-stu-id="f6226-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6226-189"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6226-189"><dt>TlsWmiProv.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="f6226-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6226-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6226-191">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="f6226-191">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

