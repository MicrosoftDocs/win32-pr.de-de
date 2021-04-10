---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_KEYType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Schlüsselressourcen Daten Satz.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_KEYType
- DNS-MicrosoftDNS_KEYType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040975"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="12d29-106">Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ KeyType-Klasse</span><span class="sxs-lookup"><span data-stu-id="12d29-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="12d29-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Schlüsselressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="12d29-107">The **CreateInstanceFromPropertyData** method instantiates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d29-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="12d29-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="12d29-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="12d29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d29-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12d29-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="12d29-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="12d29-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12d29-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="12d29-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="12d29-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12d29-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="12d29-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="12d29-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="12d29-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="12d29-117">Class of the RR.</span></span> <span data-ttu-id="12d29-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="12d29-118">Default value is 1.</span></span> <span data-ttu-id="12d29-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="12d29-119">The following values are valid.</span></span>



| <span data-ttu-id="12d29-120">Wert</span><span class="sxs-lookup"><span data-stu-id="12d29-120">Value</span></span>                                                                                                | <span data-ttu-id="12d29-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="12d29-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="12d29-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="12d29-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="12d29-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="12d29-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="12d29-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="12d29-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="12d29-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="12d29-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="12d29-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="12d29-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="12d29-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="12d29-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="12d29-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="12d29-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="12d29-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="12d29-132">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="12d29-132">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-133">Flags, die zum Angeben der Zuordnung verwendet werden, wie in IETF RFC 2535 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="12d29-133">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="12d29-134">*Protokoll* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12d29-134">*Protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-135">Das Protokoll, für das der im Ressourcen Daten Satz angegebene Schlüssel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="12d29-135">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="12d29-136">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="12d29-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="12d29-137">Wert</span><span class="sxs-lookup"><span data-stu-id="12d29-137">Value</span></span>                                                                                                    | <span data-ttu-id="12d29-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="12d29-138">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="12d29-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-139"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="12d29-140">TLS</span><span class="sxs-lookup"><span data-stu-id="12d29-140">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="12d29-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-141"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="12d29-142">E-Mail</span><span class="sxs-lookup"><span data-stu-id="12d29-142">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="12d29-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-143"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="12d29-144">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="12d29-144">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="12d29-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-145"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="12d29-146">IPsec</span><span class="sxs-lookup"><span data-stu-id="12d29-146">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="12d29-147"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-147"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="12d29-148">Alle Protokolle</span><span class="sxs-lookup"><span data-stu-id="12d29-148">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="12d29-149">*Algorithmus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12d29-149">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-150">Der Algorithmus, der mit dem im Ressourcen Daten Satz angegebenen Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12d29-150">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="12d29-151">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="12d29-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="12d29-152">Wert</span><span class="sxs-lookup"><span data-stu-id="12d29-152">Value</span></span>                                                                                                | <span data-ttu-id="12d29-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="12d29-153">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="12d29-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-154"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="12d29-155">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="12d29-155">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="12d29-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-156"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="12d29-157">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="12d29-157">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="12d29-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-158"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="12d29-159">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="12d29-159">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="12d29-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-160"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="12d29-161">Kryptografie mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="12d29-161">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="12d29-162">*PublicKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12d29-162">*PublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-163">Öffentlicher Schlüssel, dargestellt in Basis 64, wie in Anhang A von RFC 2535 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="12d29-163">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="12d29-164">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="12d29-164">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="12d29-165">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="12d29-165">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d29-166">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12d29-166">Return value</span></span>

<span data-ttu-id="12d29-167">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="12d29-167">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d29-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12d29-168">Requirements</span></span>



| <span data-ttu-id="12d29-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12d29-169">Requirement</span></span> | <span data-ttu-id="12d29-170">Wert</span><span class="sxs-lookup"><span data-stu-id="12d29-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12d29-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12d29-171">Minimum supported client</span></span><br/> | <span data-ttu-id="12d29-172">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="12d29-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="12d29-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12d29-173">Minimum supported server</span></span><br/> | <span data-ttu-id="12d29-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12d29-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="12d29-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="12d29-175">Namespace</span></span><br/>                | <span data-ttu-id="12d29-176">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="12d29-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="12d29-177">MOF</span><span class="sxs-lookup"><span data-stu-id="12d29-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12d29-178"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="12d29-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d29-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12d29-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d29-180">**MicrosoftDNS- \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="12d29-180">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="12d29-181">**Modify-Methode der MicrosoftDNS- \_ KeyType-Klasse**</span><span class="sxs-lookup"><span data-stu-id="12d29-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="12d29-182">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="12d29-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





