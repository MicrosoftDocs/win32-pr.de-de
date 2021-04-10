---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_SIGType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Ressourcen Eintrag der Signatur (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_SIGType
- DNS-MicrosoftDNS_SIGType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040229"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="c7fc0-106">Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Signatur Type-Klasse</span><span class="sxs-lookup"><span data-stu-id="c7fc0-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="c7fc0-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag der Signatur (SIG).</span><span class="sxs-lookup"><span data-stu-id="c7fc0-107">The **CreateInstanceFromPropertyData** method instantiates a Signature (SIG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fc0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7fc0-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c7fc0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7fc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fc0-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-117">Class of the RR.</span></span> <span data-ttu-id="c7fc0-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-118">Default value is 1.</span></span> <span data-ttu-id="c7fc0-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-119">The following values are valid.</span></span>



| <span data-ttu-id="c7fc0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c7fc0-120">Value</span></span>                                                                                                | <span data-ttu-id="c7fc0-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7fc0-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c7fc0-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c7fc0-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c7fc0-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c7fc0-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c7fc0-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-132">*Typecovered* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-132">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-133">Der Typ von RR, der von diesem SIG abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-133">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-134">*Algorithmus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-134">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-135">Der Algorithmus, der mit dem im Ressourcen Daten Satz angegebenen Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-135">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="c7fc0-136">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="c7fc0-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c7fc0-137">Value</span></span>                                                                                                | <span data-ttu-id="c7fc0-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7fc0-138">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c7fc0-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-139"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-140">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-140">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="c7fc0-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-141"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-142">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-142">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="c7fc0-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-143"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-144">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-144">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="c7fc0-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-145"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c7fc0-146">Kryptografie mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="c7fc0-146">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c7fc0-147">*Bezeichnungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-147">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-148">Anzahl nicht signierter Bezeichnungen im ursprünglichen SIG RR-Besitzer Namen.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-148">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="c7fc0-149">Die Anzahl enthält nicht die NULL-Bezeichnung für den Stamm und keine anfänglichen Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-149">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-150">*Originalttl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-150">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-151">Gültigkeitsdauer der von SIG signierten RR-Menge.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-151">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-152">*Signatureablauf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-152">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-153">Das Ablaufdatum der Signatur, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-153">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-154">*SignatureInception* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-154">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-155">Datum und Uhrzeit, zu der die Signatur gültig wird, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), mit Ausnahme von Schaltsekunden.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-155">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-156">*Keytag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-156">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-157">Methode, die zum Auswählen eines Schlüssels verwendet wird, der einen SIG überprüft.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-157">Method used to choose a key that verifies an SIG.</span></span> <span data-ttu-id="c7fc0-158">Informationen zur Methode, mit der ein keytag berechnet wird, finden Sie in RFC 2535, Anhang C.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-158">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-159">*Signatur Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-159">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-160">Der Domänen Name des Signatur Gebers, der die SIG RR generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-160">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-161">*Signatur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-161">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-162">Die in Basis 64 dargestellte Signatur, wie in RFC 2535, Anhang A, formatiert.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-162">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="c7fc0-163">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-163">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc0-164">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-164">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fc0-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7fc0-165">Return value</span></span>

<span data-ttu-id="c7fc0-166">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c7fc0-166">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fc0-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7fc0-167">Requirements</span></span>



| <span data-ttu-id="c7fc0-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7fc0-168">Requirement</span></span> | <span data-ttu-id="c7fc0-169">Wert</span><span class="sxs-lookup"><span data-stu-id="c7fc0-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fc0-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-170">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fc0-171">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c7fc0-171">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c7fc0-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7fc0-172">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fc0-173">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7fc0-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c7fc0-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7fc0-174">Namespace</span></span><br/>                | <span data-ttu-id="c7fc0-175">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="c7fc0-175">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c7fc0-176">MOF</span><span class="sxs-lookup"><span data-stu-id="c7fc0-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7fc0-177"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc0-177"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fc0-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7fc0-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fc0-179">**MicrosoftDNS- \_ sigtype**</span><span class="sxs-lookup"><span data-stu-id="c7fc0-179">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="c7fc0-180">**Modify-Methode der MicrosoftDNS- \_ sigtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c7fc0-180">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="c7fc0-181">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="c7fc0-181">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





