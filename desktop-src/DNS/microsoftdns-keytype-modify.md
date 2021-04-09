---
title: Modify-Methode der MicrosoftDNS_KEYType-Klasse
description: Die Modify-Methode aktualisiert einen Schlüsselressourcen Daten Satz.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_KEYType-Klasse
- DNS-MicrosoftDNS_KEYType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106125"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="f0c81-106">Modify-Methode der MicrosoftDNS- \_ KeyType-Klasse</span><span class="sxs-lookup"><span data-stu-id="f0c81-106">Modify method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="f0c81-107">Die **Modify** -Methode aktualisiert einen Schlüsselressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="f0c81-107">The **Modify** method updates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c81-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0c81-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f0c81-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0c81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c81-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c81-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0c81-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f0c81-112">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-112">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c81-113">Flags, die zum Angeben der Zuordnung verwendet werden, wie in IETF RFC 2535 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f0c81-113">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="f0c81-114">*Protokoll* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-114">*Protocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c81-115">Das Protokoll, für das der in RR angegebene Schlüssel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0c81-115">Protocol for which the key specified in the RR can be used.</span></span> <span data-ttu-id="f0c81-116">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0c81-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="f0c81-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f0c81-117">Value</span></span>                                                                                                    | <span data-ttu-id="f0c81-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0c81-118">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f0c81-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-119"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="f0c81-120">TLS</span><span class="sxs-lookup"><span data-stu-id="f0c81-120">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="f0c81-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-121"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="f0c81-122">E-Mail</span><span class="sxs-lookup"><span data-stu-id="f0c81-122">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="f0c81-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-123"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="f0c81-124">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="f0c81-124">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="f0c81-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-125"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="f0c81-126">IPsec</span><span class="sxs-lookup"><span data-stu-id="f0c81-126">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="f0c81-127"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-127"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="f0c81-128">Alle Protokolle</span><span class="sxs-lookup"><span data-stu-id="f0c81-128">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0c81-129">*Algorithmus* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-129">*Algorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c81-130">Der Algorithmus, der mit dem im Ressourcen Daten Satz angegebenen Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0c81-130">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="f0c81-131">Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0c81-131">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="f0c81-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f0c81-132">Value</span></span>                                                                                                | <span data-ttu-id="f0c81-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0c81-133">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f0c81-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f0c81-135">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="f0c81-135">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="f0c81-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f0c81-137">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="f0c81-137">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="f0c81-138"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-138"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f0c81-139">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="f0c81-139">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="f0c81-140"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-140"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f0c81-141">Kryptografie mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="f0c81-141">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0c81-142">*PublicKey* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-142">*PublicKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c81-143">Öffentlicher Schlüssel, dargestellt in Basis 64, wie in Anhang A von RFC 2535 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f0c81-143">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="f0c81-144">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c81-145">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f0c81-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c81-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0c81-146">Return value</span></span>

<span data-ttu-id="f0c81-147">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f0c81-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0c81-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0c81-148">Remarks</span></span>

<span data-ttu-id="f0c81-149">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="f0c81-149">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c81-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0c81-150">Requirements</span></span>



| <span data-ttu-id="f0c81-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0c81-151">Requirement</span></span> | <span data-ttu-id="f0c81-152">Wert</span><span class="sxs-lookup"><span data-stu-id="f0c81-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c81-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0c81-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c81-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0c81-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f0c81-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0c81-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c81-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f0c81-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0c81-157">Namespace</span></span><br/>                | <span data-ttu-id="f0c81-158">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f0c81-158">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f0c81-159">MOF</span><span class="sxs-lookup"><span data-stu-id="f0c81-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0c81-160"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-160"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c81-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0c81-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c81-162">**MicrosoftDNS- \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="f0c81-162">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="f0c81-163">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ KeyType-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f0c81-163">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0c81-164">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="f0c81-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





