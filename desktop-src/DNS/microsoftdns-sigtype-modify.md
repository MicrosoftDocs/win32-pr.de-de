---
title: Modify-Methode der MicrosoftDNS_SIGType-Klasse
description: Die Modify-Methode aktualisiert eine Signatur (SIG) RR.
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_SIGType-Klasse
- DNS-MicrosoftDNS_SIGType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475543"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="a6808-106">Modify-Methode der MicrosoftDNS- \_ sigtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="a6808-106">Modify method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="a6808-107">Die **Modify** -Methode aktualisiert eine Signatur (SIG) RR.</span><span class="sxs-lookup"><span data-stu-id="a6808-107">The **Modify** method updates a Signature (SIG) RR.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6808-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6808-108">Syntax</span></span>


```mof
void Modify(
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



## <a name="parameters"></a><span data-ttu-id="a6808-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6808-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6808-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a6808-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6808-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-112">*Typecovered* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-112">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-113">Der Typ von RR, der von diesem SIG abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="a6808-113">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-114">*Algorithmus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-114">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-115">Der Algorithmus, der mit dem im Ressourcen Daten Satz angegebenen Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6808-115">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="a6808-116">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6808-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="a6808-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a6808-117">Value</span></span>                                                                                                | <span data-ttu-id="a6808-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a6808-118">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a6808-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a6808-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a6808-120">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="a6808-120">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="a6808-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a6808-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a6808-122">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="a6808-122">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="a6808-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a6808-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a6808-124">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="a6808-124">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="a6808-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="a6808-125"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a6808-126">Kryptografie mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="a6808-126">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a6808-127">*Bezeichnungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-127">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-128">Anzahl nicht signierter Bezeichnungen im ursprünglichen SIG RR-Besitzer Namen.</span><span class="sxs-lookup"><span data-stu-id="a6808-128">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="a6808-129">Die Anzahl enthält nicht die NULL-Bezeichnung für den Stamm und keine anfänglichen Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="a6808-129">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-130">*Originalttl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-130">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-131">Gültigkeitsdauer der von SIG signierten RR-Menge.</span><span class="sxs-lookup"><span data-stu-id="a6808-131">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-132">*Signatureablauf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-132">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-133">Das Ablaufdatum der Signatur, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.</span><span class="sxs-lookup"><span data-stu-id="a6808-133">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-134">*SignatureInception* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-134">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-135">Datum und Uhrzeit, zu der die Signatur gültig wird, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), mit Ausnahme von Schaltsekunden.</span><span class="sxs-lookup"><span data-stu-id="a6808-135">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-136">*Keytag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-136">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-137">Methode, die zum Auswählen eines Schlüssels verwendet wird, der einen SIG überprüft.</span><span class="sxs-lookup"><span data-stu-id="a6808-137">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="a6808-138">Informationen zur Methode, mit der ein keytag berechnet wird, finden Sie in RFC 2535, Anhang C.</span><span class="sxs-lookup"><span data-stu-id="a6808-138">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-139">*Signatur Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-139">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-140">Der Domänen Name des Signatur Gebers, der die SIG RR generiert hat.</span><span class="sxs-lookup"><span data-stu-id="a6808-140">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-141">*Signatur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6808-141">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-142">Die in Basis 64 dargestellte Signatur, wie in RFC 2535, Anhang A, formatiert.</span><span class="sxs-lookup"><span data-stu-id="a6808-142">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="a6808-143">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a6808-143">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a6808-144">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a6808-144">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6808-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6808-145">Return value</span></span>

<span data-ttu-id="a6808-146">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a6808-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6808-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6808-147">Remarks</span></span>

<span data-ttu-id="a6808-148">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="a6808-148">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6808-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6808-149">Requirements</span></span>



| <span data-ttu-id="a6808-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6808-150">Requirement</span></span> | <span data-ttu-id="a6808-151">Wert</span><span class="sxs-lookup"><span data-stu-id="a6808-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6808-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6808-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a6808-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a6808-153">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a6808-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6808-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a6808-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6808-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a6808-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6808-156">Namespace</span></span><br/>                | <span data-ttu-id="a6808-157">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="a6808-157">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a6808-158">MOF</span><span class="sxs-lookup"><span data-stu-id="a6808-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6808-159"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a6808-159"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6808-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6808-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6808-161">**MicrosoftDNS- \_ sigtype**</span><span class="sxs-lookup"><span data-stu-id="a6808-161">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="a6808-162">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Signatur Type-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a6808-162">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a6808-163">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="a6808-163">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





