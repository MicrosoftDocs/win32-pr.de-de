---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_ATMAType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen Atma-Ressourcen Eintrag (ATM Address to Name).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_ATMAType
- DNS-MicrosoftDNS_ATMAType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340333"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="9d59d-106">Methode "kreateinzustancefrompropertydata" der MicrosoftDNS \_ atmatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="9d59d-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="9d59d-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen Atma-Ressourcen Eintrag (ATM Address to Name).</span><span class="sxs-lookup"><span data-stu-id="9d59d-107">The **CreateInstanceFromPropertyData** method instantiates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d59d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d59d-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9d59d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d59d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d59d-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="9d59d-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9d59d-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="9d59d-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9d59d-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="9d59d-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="9d59d-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="9d59d-117">Class of the RR.</span></span> <span data-ttu-id="9d59d-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="9d59d-118">Default value is 1.</span></span> <span data-ttu-id="9d59d-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="9d59d-119">The following values are valid.</span></span>



| <span data-ttu-id="9d59d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9d59d-120">Value</span></span>                                                                                                | <span data-ttu-id="9d59d-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9d59d-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="9d59d-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9d59d-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9d59d-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="9d59d-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="9d59d-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9d59d-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9d59d-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="9d59d-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="9d59d-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9d59d-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9d59d-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="9d59d-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="9d59d-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9d59d-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9d59d-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="9d59d-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="9d59d-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9d59d-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9d59d-132">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-133">ATM-Adressformat.</span><span class="sxs-lookup"><span data-stu-id="9d59d-133">ATM address format.</span></span> <span data-ttu-id="9d59d-134">Zwei mögliche Werte für das Format sind: 0, was das AESA-Format (ATM End System Address) angibt, und 1 gibt das E. 164-Format an.</span><span class="sxs-lookup"><span data-stu-id="9d59d-134">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="9d59d-135">*Atmaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-135">*ATMAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-136">Zeichenfolge mit variabler Länge von Oktetten, die die ATM-Adresse des Knotens bzw. Besitzers enthält, auf den sich diese RR bezieht.</span><span class="sxs-lookup"><span data-stu-id="9d59d-136">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="9d59d-137">Die ersten vier Bytes des Arrays werden verwendet, um die Größe der Oktett-Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9d59d-137">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="9d59d-138">Das signifikanteste Byte wird in Byte 0 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d59d-138">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="9d59d-139">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59d-140">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9d59d-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d59d-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d59d-141">Return value</span></span>

<span data-ttu-id="9d59d-142">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9d59d-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d59d-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d59d-143">Requirements</span></span>



| <span data-ttu-id="9d59d-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d59d-144">Requirement</span></span> | <span data-ttu-id="9d59d-145">Wert</span><span class="sxs-lookup"><span data-stu-id="9d59d-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d59d-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d59d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9d59d-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9d59d-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9d59d-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d59d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9d59d-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d59d-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9d59d-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d59d-150">Namespace</span></span><br/>                | <span data-ttu-id="9d59d-151">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="9d59d-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9d59d-152">MOF</span><span class="sxs-lookup"><span data-stu-id="9d59d-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d59d-153"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9d59d-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d59d-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d59d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d59d-155">**MicrosoftDNS- \_ atmatype**</span><span class="sxs-lookup"><span data-stu-id="9d59d-155">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="9d59d-156">**Modify-Methode der MicrosoftDNS \_ atmatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d59d-156">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="9d59d-157">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="9d59d-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





