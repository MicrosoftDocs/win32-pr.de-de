---
title: Importagreementlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und die automatische Verbindung über das Internet, um die Key Pack-Lizenz zu überprüfen.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Importagreementlicenskeypack-Methode Remotedesktopdienste
- Importagreementlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, importagreementlicenskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106076"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="0ddbb-106">Importagreementlicenskeypack-Methode der Win32-Klasse "" der \_ Klasse "zlicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="0ddbb-106">ImportAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="0ddbb-107">Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und die automatische Verbindung über das Internet, um die Key Pack-Lizenz zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddbb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ddbb-108">Syntax</span></span>


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="0ddbb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ddbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ddbb-110">*Agreementtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-111">Vertragstyp.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="0ddbb-112">0</span><span class="sxs-lookup"><span data-stu-id="0ddbb-112">0</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-113">Das Lizenzschlüssel Paket wird von einem SELECT-Volumenlizenzvertrag (für Kunden mit 250 oder mehr Computern) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="0ddbb-114">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-115">1</span><span class="sxs-lookup"><span data-stu-id="0ddbb-115">1</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-116">Das Lizenzschlüssel Paket basiert auf einem Enterprise-Volumenlizenzvertrag für Kunden mit 250 oder mehr Computern.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="0ddbb-117">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-118">2</span><span class="sxs-lookup"><span data-stu-id="0ddbb-118">2</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-119">Das Lizenzschlüssel Paket basiert auf einem Campus-Volumenlizenzvertrag für eine höhere Bildungseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="0ddbb-120">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-121">3</span><span class="sxs-lookup"><span data-stu-id="0ddbb-121">3</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-122">Das Lizenzschlüssel Paket wird von einem Schul-Volumenlizenzvertrag für primäre und sekundäre Einrichtungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="0ddbb-123">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-124">4</span><span class="sxs-lookup"><span data-stu-id="0ddbb-124">4</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-125">Das Lizenzschlüssel Paket wird von einem Dienstanbieter-Lizenzvertrag für Dienstanbieter zum Lizenzieren von Microsoft-Software auf monatlicher Basis.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="0ddbb-126">Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-127">5</span><span class="sxs-lookup"><span data-stu-id="0ddbb-127">5</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-128">Das Lizenzschlüssel Paket ist aus einem anderen Lizenzvertrag, wie z. b. Open Value, Open-Year-Lizenz und Open-Abonnement-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="0ddbb-129">Der *sagreementnumber* -Parameter ist die Vertragsnummer, die mit ihren Programminformationen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ddbb-130">*sagreementnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-131">Vertragsnummer oder Registrierungsnummer.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="0ddbb-132">Der *sagreementnumber* -Parameter ist eine siebenstellige numerische Zeichenfolge ohne Bindestriche.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-133">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-134">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-134">Product version.</span></span>

<dt>

<span data-ttu-id="0ddbb-135">0</span><span class="sxs-lookup"><span data-stu-id="0ddbb-135">0</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-136">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-137">1</span><span class="sxs-lookup"><span data-stu-id="0ddbb-137">1</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-138">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-139">2</span><span class="sxs-lookup"><span data-stu-id="0ddbb-139">2</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ddbb-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ddbb-141">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-142">Produkttyp.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-142">Product type.</span></span>

<dt>

<span data-ttu-id="0ddbb-143">0</span><span class="sxs-lookup"><span data-stu-id="0ddbb-143">0</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-144">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="0ddbb-145">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-146">1</span><span class="sxs-lookup"><span data-stu-id="0ddbb-146">1</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-147">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="0ddbb-148">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-149">2</span><span class="sxs-lookup"><span data-stu-id="0ddbb-149">2</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-150">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ddbb-151">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-152">Anzahl der zu importierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-152">Number of licenses to import.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-153">*ssourcelsname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-153">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-154">Der Name der Quelle Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-154">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="0ddbb-155">Dies ist entweder der voll qualifizierte Distinguished Name oder die IP-Adresse des Servers.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-155">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-156">*ssourcelsproductid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-156">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-157">Der Bezeichner des Remotedesktop-Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-157">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="0ddbb-158">Bei handelt es sich um eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-158">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="0ddbb-159">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0ddbb-159">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ddbb-160">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-160">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ddbb-161">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ddbb-161">Return value</span></span>

<span data-ttu-id="0ddbb-162">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0ddbb-163">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ddbb-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0ddbb-164">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0ddbb-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddbb-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ddbb-165">Requirements</span></span>



| <span data-ttu-id="0ddbb-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ddbb-166">Requirement</span></span> | <span data-ttu-id="0ddbb-167">Wert</span><span class="sxs-lookup"><span data-stu-id="0ddbb-167">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddbb-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ddbb-168">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddbb-169">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0ddbb-169">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="0ddbb-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ddbb-170">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddbb-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ddbb-171">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="0ddbb-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ddbb-172">Namespace</span></span><br/>                | <span data-ttu-id="0ddbb-173">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="0ddbb-173">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="0ddbb-174">MOF</span><span class="sxs-lookup"><span data-stu-id="0ddbb-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ddbb-175"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0ddbb-175"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ddbb-176">DLL</span><span class="sxs-lookup"><span data-stu-id="0ddbb-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ddbb-177"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ddbb-177"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddbb-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ddbb-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddbb-179">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="0ddbb-179">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





