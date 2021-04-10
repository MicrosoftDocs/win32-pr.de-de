---
title: MicrosoftDNS_NXTType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen nächsten (NXT) RR darstellt.
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- DNS-MicrosoftDNS_NXTType Klasse
- DNS-MicrosoftDNS_NXTType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104163"
---
# <a name="microsoftdns_nxttype-class"></a><span data-ttu-id="6326d-105">MicrosoftDNS \_ nxttype-Klasse</span><span class="sxs-lookup"><span data-stu-id="6326d-105">MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="6326d-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen nächsten (NXT) RR darstellt.</span><span class="sxs-lookup"><span data-stu-id="6326d-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Next (NXT) RR.</span></span>

<span data-ttu-id="6326d-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6326d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6326d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6326d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a><span data-ttu-id="6326d-109">Member</span><span class="sxs-lookup"><span data-stu-id="6326d-109">Members</span></span>

<span data-ttu-id="6326d-110">Die **MicrosoftDNS- \_ nxttype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6326d-110">The **MicrosoftDNS\_NXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="6326d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6326d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6326d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6326d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6326d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="6326d-113">Methods</span></span>

<span data-ttu-id="6326d-114">Die **MicrosoftDNS- \_ nxttype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6326d-114">The **MicrosoftDNS\_NXTType** class has these methods.</span></span>



| <span data-ttu-id="6326d-115">Methode</span><span class="sxs-lookup"><span data-stu-id="6326d-115">Method</span></span>                             | <span data-ttu-id="6326d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6326d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6326d-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="6326d-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="6326d-118">Instanziiert einen NXT-Ressourcen Daten Satz basierend auf den Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standardwert = in), dem Wert für die Gültigkeitsdauer und dem WINS-ZuordnungsFlag, dem umgekehrten Nachschlage Timeout, dem WINS-Cache Timeout und dem anzufügende Domänen</span><span class="sxs-lookup"><span data-stu-id="6326d-118">Instantiates an NXT Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out, and domain name to append.</span></span> <span data-ttu-id="6326d-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6326d-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6326d-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="6326d-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="6326d-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="6326d-121">**Modify**</span></span>                         | <span data-ttu-id="6326d-122">Aktualisiert die Gültigkeitsdauer, das ZuordnungsFlag, das Nachschlage Timeout, den Cache Timeout und die Ergebnis Domäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6326d-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="6326d-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="6326d-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="6326d-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="6326d-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="6326d-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="6326d-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="6326d-126">**Windows Server 2003:** Diese Methode aktualisiert auch den nextdomainname-Typ und den-Typ auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6326d-126">**Windows Server 2003:** This method also updates the NextDomainName and Types to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="6326d-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6326d-127">Properties</span></span>

<span data-ttu-id="6326d-128">Die **MicrosoftDNS- \_ nxttype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6326d-128">The **MicrosoftDNS\_NXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6326d-129">**Nextdomainname**</span><span class="sxs-lookup"><span data-stu-id="6326d-129">**NextDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326d-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6326d-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6326d-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6326d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326d-132">Der nächste Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="6326d-132">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="6326d-133">**Typen**</span><span class="sxs-lookup"><span data-stu-id="6326d-133">**Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326d-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6326d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6326d-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6326d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326d-136">Durch Leerzeichen getrennte Liste der RR-Type-mnetmonics für den Besitzer Namen des NXT-Ressourcen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="6326d-136">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6326d-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6326d-137">Requirements</span></span>



| <span data-ttu-id="6326d-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6326d-138">Requirement</span></span> | <span data-ttu-id="6326d-139">Wert</span><span class="sxs-lookup"><span data-stu-id="6326d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6326d-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6326d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6326d-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6326d-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6326d-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6326d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6326d-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6326d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6326d-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="6326d-144">Namespace</span></span><br/>                | <span data-ttu-id="6326d-145">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="6326d-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6326d-146">MOF</span><span class="sxs-lookup"><span data-stu-id="6326d-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6326d-147"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6326d-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6326d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6326d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6326d-149">**Die Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ nxttype"**</span><span class="sxs-lookup"><span data-stu-id="6326d-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6326d-150">**Modify-Methode der MicrosoftDNS- \_ nxttype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6326d-150">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="6326d-151">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="6326d-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





