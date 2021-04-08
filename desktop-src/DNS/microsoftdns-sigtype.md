---
title: MicrosoftDNS_SIGType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Daten Satz der Signatur (SIG) darstellt.
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- DNS-MicrosoftDNS_SIGType Klasse
- DNS-MicrosoftDNS_SIGType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740264"
---
# <a name="microsoftdns_sigtype-class"></a><span data-ttu-id="c2895-105">MicrosoftDNS- \_ sigtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="c2895-105">MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="c2895-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Daten Satz der Signatur (SIG) darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2895-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Signature (SIG) Resource Record.</span></span>

<span data-ttu-id="c2895-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c2895-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2895-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2895-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a><span data-ttu-id="c2895-109">Member</span><span class="sxs-lookup"><span data-stu-id="c2895-109">Members</span></span>

<span data-ttu-id="c2895-110">Die **MicrosoftDNS- \_ sigtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c2895-110">The **MicrosoftDNS\_SIGType** class has these types of members:</span></span>

-   [<span data-ttu-id="c2895-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c2895-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c2895-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2895-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2895-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="c2895-113">Methods</span></span>

<span data-ttu-id="c2895-114">Die **MicrosoftDNS- \_ sigtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c2895-114">The **MicrosoftDNS\_SIGType** class has these methods.</span></span>



| <span data-ttu-id="c2895-115">Methode</span><span class="sxs-lookup"><span data-stu-id="c2895-115">Method</span></span>                             | <span data-ttu-id="c2895-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2895-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2895-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="c2895-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c2895-118">Instanziiert eine SIG RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Wert für die Gültigkeitsdauer und dem WINS-ZuordnungsFlag, dem Reverse-Nachschlage Timeout, dem WINS-Cache Timeout und dem anzufügende Domänen Namen.</span><span class="sxs-lookup"><span data-stu-id="c2895-118">Instantiates an SIG RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="c2895-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2895-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c2895-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="c2895-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c2895-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="c2895-121">**Modify**</span></span>                         | <span data-ttu-id="c2895-122">Aktualisiert die Gültigkeitsdauer, das ZuordnungsFlag, das Nachschlage Timeout, den Cache Timeout und die Ergebnis Domäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c2895-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c2895-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c2895-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c2895-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="c2895-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c2895-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="c2895-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="c2895-126">**Windows Server 2003:** Diese Methode aktualisiert auch typecovered, Algorithmus, Labels, originalttl, signatureablauf, SignatureInception, keytag, signername und Signature auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2895-126">**Windows Server 2003:** This method also updates the TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName and Signature to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="c2895-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2895-127">Properties</span></span>

<span data-ttu-id="c2895-128">Die **MicrosoftDNS- \_ sigtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2895-128">The **MicrosoftDNS\_SIGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2895-129">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="c2895-129">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2895-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-132">Der Algorithmus, der mit dem im Ressourcen Daten Satz angegebenen Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2895-132">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="c2895-133">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2895-133">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="c2895-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c2895-134">Value</span></span>                                                                                                | <span data-ttu-id="c2895-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2895-135">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c2895-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c2895-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c2895-137">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="c2895-137">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="c2895-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c2895-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c2895-139">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="c2895-139">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="c2895-140"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c2895-140"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c2895-141">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="c2895-141">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="c2895-142"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c2895-142"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c2895-143">Kryptografie mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="c2895-143">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c2895-144">**Keytag**</span><span class="sxs-lookup"><span data-stu-id="c2895-144">**KeyTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2895-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-147">Methode, die zum Auswählen eines Schlüssels verwendet wird, der einen SIG überprüft.</span><span class="sxs-lookup"><span data-stu-id="c2895-147">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="c2895-148">Informationen zur Methode, mit der ein keytag berechnet wird, finden Sie in RFC 2535, Anhang C.</span><span class="sxs-lookup"><span data-stu-id="c2895-148">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="c2895-149">**Bezeichnungen**</span><span class="sxs-lookup"><span data-stu-id="c2895-149">**Labels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2895-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-152">Anzahl nicht signierter Bezeichnungen im ursprünglichen SIG RR-Besitzer Namen.</span><span class="sxs-lookup"><span data-stu-id="c2895-152">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="c2895-153">Die Anzahl enthält nicht die NULL-Bezeichnung für den Stamm und keine anfänglichen Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="c2895-153">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="c2895-154">**Originalttl**</span><span class="sxs-lookup"><span data-stu-id="c2895-154">**OriginalTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2895-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-157">Gültigkeitsdauer der von SIG signierten RR-Menge.</span><span class="sxs-lookup"><span data-stu-id="c2895-157">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="c2895-158">**Signature**</span><span class="sxs-lookup"><span data-stu-id="c2895-158">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2895-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-161">Die in Basis 64 dargestellte Signatur, wie in RFC 2535, Anhang A, formatiert.</span><span class="sxs-lookup"><span data-stu-id="c2895-161">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="c2895-162">**Signatureablauf**</span><span class="sxs-lookup"><span data-stu-id="c2895-162">**SignatureExpiration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2895-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-165">Das Ablaufdatum der Signatur, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.</span><span class="sxs-lookup"><span data-stu-id="c2895-165">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c2895-166">**SignatureInception**</span><span class="sxs-lookup"><span data-stu-id="c2895-166">**SignatureInception**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2895-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-169">Datum und Uhrzeit, zu der die Signatur gültig wird, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), mit Ausnahme von Schaltsekunden.</span><span class="sxs-lookup"><span data-stu-id="c2895-169">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c2895-170">**Signatur Name**</span><span class="sxs-lookup"><span data-stu-id="c2895-170">**SignerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2895-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-173">Der Domänen Name des Signatur Gebers, der die SIG RR generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c2895-173">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="c2895-174">**Typecovered**</span><span class="sxs-lookup"><span data-stu-id="c2895-174">**TypeCovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2895-175">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2895-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2895-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2895-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2895-177">Der Typ von RR, der von diesem SIG abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="c2895-177">Type of RR covered by this SIG.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2895-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2895-178">Requirements</span></span>



| <span data-ttu-id="c2895-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2895-179">Requirement</span></span> | <span data-ttu-id="c2895-180">Wert</span><span class="sxs-lookup"><span data-stu-id="c2895-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2895-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2895-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c2895-182">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2895-182">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c2895-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2895-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c2895-184">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2895-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2895-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2895-185">Namespace</span></span><br/>                | <span data-ttu-id="c2895-186">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="c2895-186">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c2895-187">MOF</span><span class="sxs-lookup"><span data-stu-id="c2895-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2895-188"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2895-188"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2895-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2895-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2895-190">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Signatur Type-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c2895-190">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c2895-191">**Modify-Methode der MicrosoftDNS- \_ sigtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c2895-191">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="c2895-192">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="c2895-192">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





