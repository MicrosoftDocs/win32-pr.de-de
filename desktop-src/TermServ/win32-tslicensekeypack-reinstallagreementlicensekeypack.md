---
title: Reinstallagreementlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüssel Paket neu, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.
ms.assetid: BC3C966B-E6CE-45E2-BC1D-2439B75D4C3C
ms.tgt_platform: multiple
keywords:
- Reinstallagreementlicenskeypack-Methode Remotedesktopdienste
- Reinstallagreementlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, reinstallagreementlicenskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821ff6dc538a670e03757253b616ff16489dc108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517867"
---
# <a name="reinstallagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="bec45-106">Reinstallagreementlicenskeypack-Methode der Win32- \_ Klasse "zlicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="bec45-106">ReinstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="bec45-107">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket neu, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bec45-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec45-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bec45-108">Syntax</span></span>


```mof
uint32 ReinstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="bec45-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bec45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec45-110">*Agreementtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec45-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec45-111">Vertragstyp.</span><span class="sxs-lookup"><span data-stu-id="bec45-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="bec45-112">0</span><span class="sxs-lookup"><span data-stu-id="bec45-112">0</span></span>
</dt> <dd>

<span data-ttu-id="bec45-113">Das Lizenzschlüssel Paket wird von einem SELECT-Volumenlizenzvertrag (für Kunden mit 250 oder mehr Computern) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bec45-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="bec45-114">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="bec45-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-115">1</span><span class="sxs-lookup"><span data-stu-id="bec45-115">1</span></span>
</dt> <dd>

<span data-ttu-id="bec45-116">Das Lizenzschlüssel Paket basiert auf einem Enterprise-Volumenlizenzvertrag für Kunden mit 250 oder mehr Computern.</span><span class="sxs-lookup"><span data-stu-id="bec45-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="bec45-117">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="bec45-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-118">2</span><span class="sxs-lookup"><span data-stu-id="bec45-118">2</span></span>
</dt> <dd>

<span data-ttu-id="bec45-119">Das Lizenzschlüssel Paket basiert auf einem Campus-Volumenlizenzvertrag für eine höhere Bildungseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="bec45-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="bec45-120">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="bec45-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-121">3</span><span class="sxs-lookup"><span data-stu-id="bec45-121">3</span></span>
</dt> <dd>

<span data-ttu-id="bec45-122">Das Lizenzschlüssel Paket wird von einem Schul-Volumenlizenzvertrag für primäre und sekundäre Einrichtungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bec45-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="bec45-123">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="bec45-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-124">4</span><span class="sxs-lookup"><span data-stu-id="bec45-124">4</span></span>
</dt> <dd>

<span data-ttu-id="bec45-125">Das Lizenzschlüssel Paket wird von einem Dienstanbieter-Lizenzvertrag für Dienstanbieter zum Lizenzieren von Microsoft-Software auf monatlicher Basis.</span><span class="sxs-lookup"><span data-stu-id="bec45-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="bec45-126">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="bec45-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-127">5</span><span class="sxs-lookup"><span data-stu-id="bec45-127">5</span></span>
</dt> <dd>

<span data-ttu-id="bec45-128">Das Lizenzschlüssel Paket ist aus einem anderen Lizenzvertrag, wie z. b. Open Value, Open-Year-Lizenz und Open-Abonnement-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="bec45-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="bec45-129">Der *sagreementnumber* -Parameter ist die Vertragsnummer, die mit ihren Programminformationen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bec45-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bec45-130">*sagreementnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec45-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec45-131">Vertragsnummer oder Registrierungsnummer.</span><span class="sxs-lookup"><span data-stu-id="bec45-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="bec45-132">Der *sagreementnumber* -Parameter ist eine siebenstellige numerische Zeichenfolge ohne Bindestriche.</span><span class="sxs-lookup"><span data-stu-id="bec45-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-133">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec45-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec45-134">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="bec45-134">Product version.</span></span>

<dt>

<span data-ttu-id="bec45-135">0</span><span class="sxs-lookup"><span data-stu-id="bec45-135">0</span></span>
</dt> <dd>

<span data-ttu-id="bec45-136">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bec45-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-137">1</span><span class="sxs-lookup"><span data-stu-id="bec45-137">1</span></span>
</dt> <dd>

<span data-ttu-id="bec45-138">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bec45-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-139">2</span><span class="sxs-lookup"><span data-stu-id="bec45-139">2</span></span>
</dt> <dd>

<span data-ttu-id="bec45-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bec45-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bec45-141">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec45-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec45-142">Produkttyp.</span><span class="sxs-lookup"><span data-stu-id="bec45-142">Product type.</span></span>

<dt>

<span data-ttu-id="bec45-143">0</span><span class="sxs-lookup"><span data-stu-id="bec45-143">0</span></span>
</dt> <dd>

<span data-ttu-id="bec45-144">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="bec45-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="bec45-145">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="bec45-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-146">1</span><span class="sxs-lookup"><span data-stu-id="bec45-146">1</span></span>
</dt> <dd>

<span data-ttu-id="bec45-147">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bec45-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="bec45-148">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="bec45-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-149">2</span><span class="sxs-lookup"><span data-stu-id="bec45-149">2</span></span>
</dt> <dd>

<span data-ttu-id="bec45-150">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bec45-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bec45-151">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec45-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec45-152">Anzahl der zu installierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="bec45-152">Number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="bec45-153">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bec45-153">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bec45-154">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="bec45-154">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec45-155">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bec45-155">Return value</span></span>

<span data-ttu-id="bec45-156">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="bec45-156">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bec45-157">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bec45-157">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bec45-158">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bec45-158">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bec45-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bec45-159">Requirements</span></span>



| <span data-ttu-id="bec45-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bec45-160">Requirement</span></span> | <span data-ttu-id="bec45-161">Wert</span><span class="sxs-lookup"><span data-stu-id="bec45-161">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec45-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bec45-162">Minimum supported client</span></span><br/> | <span data-ttu-id="bec45-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bec45-163">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="bec45-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bec45-164">Minimum supported server</span></span><br/> | <span data-ttu-id="bec45-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bec45-165">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bec45-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="bec45-166">Namespace</span></span><br/>                | <span data-ttu-id="bec45-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="bec45-167">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="bec45-168">MOF</span><span class="sxs-lookup"><span data-stu-id="bec45-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bec45-169"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bec45-169"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bec45-170">DLL</span><span class="sxs-lookup"><span data-stu-id="bec45-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bec45-171"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bec45-171"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bec45-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bec45-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec45-173">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="bec45-173">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





