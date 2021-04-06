---
title: MicrosoftDNS_KEYType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Schlüsselressourcen Daten Satz darstellt.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- DNS-MicrosoftDNS_KEYType Klasse
- DNS-MicrosoftDNS_KEYType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e814af1d22820f1722e5812dd314dd1c7f6e0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858995"
---
# <a name="microsoftdns_keytype-class"></a><span data-ttu-id="d98ea-105">MicrosoftDNS- \_ KeyType-Klasse</span><span class="sxs-lookup"><span data-stu-id="d98ea-105">MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="d98ea-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Schlüsselressourcen Daten Satz darstellt.</span><span class="sxs-lookup"><span data-stu-id="d98ea-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a KEY Resource Record.</span></span>

<span data-ttu-id="d98ea-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="d98ea-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98ea-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d98ea-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a><span data-ttu-id="d98ea-109">Member</span><span class="sxs-lookup"><span data-stu-id="d98ea-109">Members</span></span>

<span data-ttu-id="d98ea-110">Die **MicrosoftDNS- \_ KeyType** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d98ea-110">The **MicrosoftDNS\_KEYType** class has these types of members:</span></span>

-   [<span data-ttu-id="d98ea-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d98ea-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d98ea-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d98ea-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d98ea-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d98ea-113">Methods</span></span>

<span data-ttu-id="d98ea-114">Die **MicrosoftDNS- \_ KeyType** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d98ea-114">The **MicrosoftDNS\_KEYType** class has these methods.</span></span>



| <span data-ttu-id="d98ea-115">Methode</span><span class="sxs-lookup"><span data-stu-id="d98ea-115">Method</span></span>                             | <span data-ttu-id="d98ea-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d98ea-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98ea-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="d98ea-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="d98ea-118">Instanziiert einen Schlüsselressourcen Daten Satz basierend auf den Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem WINS-ZuordnungsFlag, dem Reverse-Nachschlage Timeout, dem WINS-Cache Timeout und dem anzufügenden Domänen Namen.</span><span class="sxs-lookup"><span data-stu-id="d98ea-118">Instantiates a KEY Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="d98ea-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d98ea-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="d98ea-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="d98ea-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="d98ea-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="d98ea-121">**Modify**</span></span>                         | <span data-ttu-id="d98ea-122">Aktualisiert die Gültigkeitsdauer, das ZuordnungsFlag, das Nachschlage Timeout, den Cache Timeout und die Ergebnis Domäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d98ea-122">Updates the TTL, mapping flag, look-up time out, cache time out, and result domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="d98ea-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d98ea-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="d98ea-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="d98ea-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="d98ea-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="d98ea-125">Qualifiers: Implemented</span></span><br/>                          |



 

### <a name="properties"></a><span data-ttu-id="d98ea-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d98ea-126">Properties</span></span>

<span data-ttu-id="d98ea-127">Die **MicrosoftDNS- \_ KeyType** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d98ea-127">The **MicrosoftDNS\_KEYType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d98ea-128">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="d98ea-128">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ea-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ea-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ea-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d98ea-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ea-131">Der Algorithmus, der mit dem im Ressourcen Daten Satz angegebenen Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d98ea-131">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="d98ea-132">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d98ea-132">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="d98ea-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d98ea-133">Value</span></span>                                                                                                | <span data-ttu-id="d98ea-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d98ea-134">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d98ea-135"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-135"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d98ea-136">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="d98ea-136">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="d98ea-137"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-137"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d98ea-138">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="d98ea-138">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="d98ea-139"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-139"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d98ea-140">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="d98ea-140">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="d98ea-141"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-141"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d98ea-142">Kryptografie mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="d98ea-142">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d98ea-143">**Flags**</span><span class="sxs-lookup"><span data-stu-id="d98ea-143">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ea-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ea-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ea-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d98ea-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ea-146">Flags, die zum Angeben der Zuordnung verwendet werden, wie in IETF RFC 2535 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d98ea-146">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="d98ea-147">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="d98ea-147">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ea-148">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ea-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ea-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d98ea-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ea-150">Das Protokoll, für das der im Ressourcen Daten Satz angegebene Schlüssel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d98ea-150">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="d98ea-151">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d98ea-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="d98ea-152">Wert</span><span class="sxs-lookup"><span data-stu-id="d98ea-152">Value</span></span>                                                                                                    | <span data-ttu-id="d98ea-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d98ea-153">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d98ea-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-154"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="d98ea-155">TLS</span><span class="sxs-lookup"><span data-stu-id="d98ea-155">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="d98ea-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-156"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="d98ea-157">E-Mail</span><span class="sxs-lookup"><span data-stu-id="d98ea-157">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="d98ea-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-158"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="d98ea-159">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="d98ea-159">DNSSEC</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="d98ea-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-160"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="d98ea-161">IPsec</span><span class="sxs-lookup"><span data-stu-id="d98ea-161">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="d98ea-162"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-162"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="d98ea-163">Alle Protokolle</span><span class="sxs-lookup"><span data-stu-id="d98ea-163">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d98ea-164">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="d98ea-164">**PublicKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ea-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d98ea-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ea-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d98ea-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ea-167">Öffentlicher Schlüssel, dargestellt in Basis 64, wie in Anhang A von RFC 2535 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d98ea-167">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d98ea-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d98ea-168">Requirements</span></span>



| <span data-ttu-id="d98ea-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d98ea-169">Requirement</span></span> | <span data-ttu-id="d98ea-170">Wert</span><span class="sxs-lookup"><span data-stu-id="d98ea-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d98ea-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d98ea-171">Minimum supported client</span></span><br/> | <span data-ttu-id="d98ea-172">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d98ea-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d98ea-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d98ea-173">Minimum supported server</span></span><br/> | <span data-ttu-id="d98ea-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d98ea-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d98ea-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="d98ea-175">Namespace</span></span><br/>                | <span data-ttu-id="d98ea-176">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="d98ea-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d98ea-177">MOF</span><span class="sxs-lookup"><span data-stu-id="d98ea-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d98ea-178"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d98ea-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98ea-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d98ea-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98ea-180">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ KeyType-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d98ea-180">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d98ea-181">**Modify-Methode der MicrosoftDNS- \_ KeyType-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d98ea-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="d98ea-182">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="d98ea-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





