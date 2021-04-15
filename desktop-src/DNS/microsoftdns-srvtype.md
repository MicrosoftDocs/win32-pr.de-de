---
title: MicrosoftDNS_SRVType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Dienst (SRV)-Datensatz darstellt.
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- DNS-MicrosoftDNS_SRVType Klasse
- DNS-MicrosoftDNS_SRVType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477265"
---
# <a name="microsoftdns_srvtype-class"></a><span data-ttu-id="9d52d-105">MicrosoftDNS- \_ srvtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="9d52d-105">MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="9d52d-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Dienst (SRV)-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d52d-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Service (SRV) record.</span></span>

<span data-ttu-id="9d52d-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9d52d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d52d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d52d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a><span data-ttu-id="9d52d-109">Member</span><span class="sxs-lookup"><span data-stu-id="9d52d-109">Members</span></span>

<span data-ttu-id="9d52d-110">Die Klasse " **\_ srvtype" der MicrosoftDNS** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9d52d-110">The **MicrosoftDNS\_SRVType** class has these types of members:</span></span>

-   [<span data-ttu-id="9d52d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="9d52d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9d52d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d52d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9d52d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="9d52d-113">Methods</span></span>

<span data-ttu-id="9d52d-114">Die Klasse " **\_ srvtype" der MicrosoftDNS** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9d52d-114">The **MicrosoftDNS\_SRVType** class has these methods.</span></span>



| <span data-ttu-id="9d52d-115">Methode</span><span class="sxs-lookup"><span data-stu-id="9d52d-115">Method</span></span>                             | <span data-ttu-id="9d52d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d52d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d52d-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="9d52d-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="9d52d-118">Instanziiert einen SRV-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer/Zielname, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und die Priorität, die Gewichtung, der Port und der Domänen Name des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="9d52d-118">Instantiates an SRV Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/target Name, class (default = IN), time-to-live value, and target host's priority, weight, port, and domain name.</span></span> <span data-ttu-id="9d52d-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9d52d-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="9d52d-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="9d52d-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="9d52d-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="9d52d-121">**Modify**</span></span>                         | <span data-ttu-id="9d52d-122">Aktualisiert die TTL, Priorität, Gewichtung, den Port und den Domänen Namen auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9d52d-122">Updates the TTL, Priority, Weight, Port, and Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="9d52d-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="9d52d-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="9d52d-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="9d52d-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="9d52d-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="9d52d-125">Qualifiers: Implemented</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="9d52d-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d52d-126">Properties</span></span>

<span data-ttu-id="9d52d-127">Die Klasse **MicrosoftDNS \_ srvtype** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d52d-127">The **MicrosoftDNS\_SRVType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d52d-128">**Port**</span><span class="sxs-lookup"><span data-stu-id="9d52d-128">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52d-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d52d-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d52d-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d52d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d52d-131">Port, der auf dem Zielhost eines Protokoll Diensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d52d-131">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="9d52d-132">**Priority**</span><span class="sxs-lookup"><span data-stu-id="9d52d-132">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52d-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d52d-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d52d-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d52d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d52d-135">Priorität des im Besitzer Namen angegebenen Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="9d52d-135">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="9d52d-136">Niedrigere Zahlen implizieren höhere Prioritäten.</span><span class="sxs-lookup"><span data-stu-id="9d52d-136">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="9d52d-137">**Srvdomainname**</span><span class="sxs-lookup"><span data-stu-id="9d52d-137">**SRVDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52d-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d52d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d52d-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d52d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d52d-140">Der voll qualifizierte Namen des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="9d52d-140">FQDN of the target host.</span></span> <span data-ttu-id="9d52d-141">Ein Ziel von \\ . \\ bedeutet, dass der Dienst in dieser Domäne nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9d52d-141">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="9d52d-142">**Weight**</span><span class="sxs-lookup"><span data-stu-id="9d52d-142">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52d-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d52d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d52d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d52d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d52d-145">Gewichtung des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="9d52d-145">Weight of the target host.</span></span> <span data-ttu-id="9d52d-146">Dies ist hilfreich bei der Auswahl zwischen Hosts mit der gleichen Priorität.</span><span class="sxs-lookup"><span data-stu-id="9d52d-146">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="9d52d-147">Die Wahrscheinlichkeit, diesen Host zu verwenden, sollte proportional zu seiner Gewichtung sein.</span><span class="sxs-lookup"><span data-stu-id="9d52d-147">The chances of using this host should be proportional to its weight.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d52d-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d52d-148">Requirements</span></span>



| <span data-ttu-id="9d52d-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d52d-149">Requirement</span></span> | <span data-ttu-id="9d52d-150">Wert</span><span class="sxs-lookup"><span data-stu-id="9d52d-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d52d-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d52d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9d52d-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9d52d-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9d52d-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d52d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9d52d-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d52d-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9d52d-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d52d-155">Namespace</span></span><br/>                | <span data-ttu-id="9d52d-156">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="9d52d-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9d52d-157">MOF</span><span class="sxs-lookup"><span data-stu-id="9d52d-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d52d-158"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9d52d-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d52d-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d52d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d52d-160">**Die Methode "kreateinstancefrompropertydata" der Klasse "srvtype" von MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="9d52d-160">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9d52d-161">**Modify-Methode der MicrosoftDNS \_ srvtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d52d-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="9d52d-162">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="9d52d-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





