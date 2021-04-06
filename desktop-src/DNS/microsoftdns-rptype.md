---
title: MicrosoftDNS_RPType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen verantwortlichen Person-Datensatz (RP) darstellt.
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- DNS-MicrosoftDNS_RPType Klasse
- DNS-MicrosoftDNS_RPType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858990"
---
# <a name="microsoftdns_rptype-class"></a><span data-ttu-id="fe38b-105">MicrosoftDNS \_ rptype-Klasse</span><span class="sxs-lookup"><span data-stu-id="fe38b-105">MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="fe38b-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen verantwortlichen Person-Datensatz (RP) darstellt.</span><span class="sxs-lookup"><span data-stu-id="fe38b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Responsible Person (RP) record.</span></span>

<span data-ttu-id="fe38b-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="fe38b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe38b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe38b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a><span data-ttu-id="fe38b-109">Member</span><span class="sxs-lookup"><span data-stu-id="fe38b-109">Members</span></span>

<span data-ttu-id="fe38b-110">Die **MicrosoftDNS \_ rptype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fe38b-110">The **MicrosoftDNS\_RPType** class has these types of members:</span></span>

-   [<span data-ttu-id="fe38b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="fe38b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fe38b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe38b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fe38b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="fe38b-113">Methods</span></span>

<span data-ttu-id="fe38b-114">Die **MicrosoftDNS- \_ rptype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fe38b-114">The **MicrosoftDNS\_RPType** class has these methods.</span></span>



| <span data-ttu-id="fe38b-115">Methode</span><span class="sxs-lookup"><span data-stu-id="fe38b-115">Method</span></span>                             | <span data-ttu-id="fe38b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe38b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe38b-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="fe38b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fe38b-118">Instanziiert einen RP-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: DNS-Server Name des Datensatzes, Container Name, Besitzer/verantwortlicher Personen Name, Klasse (Standardwert = in), Gültigkeitsdauer und die Domänen Namen für das Postfach der Person und die txt-RR-Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="fe38b-118">Instantiates an RP Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/responsible person Name, class (default = IN), time-to-live value and the domain names for the person's mailbox and TXT RR locations.</span></span> <span data-ttu-id="fe38b-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe38b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fe38b-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="fe38b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fe38b-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="fe38b-121">**Modify**</span></span>                         | <span data-ttu-id="fe38b-122">Diese Methode aktualisiert die TTL-, RP-und txt-Domänen Namen auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fe38b-122">This method updates the TTL, RP Mailbox and TXT Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fe38b-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="fe38b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fe38b-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fe38b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fe38b-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="fe38b-125">Qualifiers: Implemented</span></span><br/>                                  |



 

### <a name="properties"></a><span data-ttu-id="fe38b-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe38b-126">Properties</span></span>

<span data-ttu-id="fe38b-127">Die **MicrosoftDNS \_ rptype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe38b-127">The **MicrosoftDNS\_RPType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe38b-128">**Rpmailbox**</span><span class="sxs-lookup"><span data-stu-id="fe38b-128">**RPMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe38b-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe38b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe38b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe38b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe38b-131">Vollständiger vollständiger vollständiger Name des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="fe38b-131">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="fe38b-132">**TxtDomainName**</span><span class="sxs-lookup"><span data-stu-id="fe38b-132">**TXTDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe38b-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe38b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe38b-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe38b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe38b-135">Der voll qualifizierte Daten Satz, für den txt-Ressourcen Einträge vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fe38b-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe38b-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe38b-136">Requirements</span></span>



| <span data-ttu-id="fe38b-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe38b-137">Requirement</span></span> | <span data-ttu-id="fe38b-138">Wert</span><span class="sxs-lookup"><span data-stu-id="fe38b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe38b-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe38b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fe38b-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe38b-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fe38b-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe38b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fe38b-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe38b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fe38b-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe38b-143">Namespace</span></span><br/>                | <span data-ttu-id="fe38b-144">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="fe38b-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fe38b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fe38b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe38b-146"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fe38b-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe38b-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe38b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe38b-148">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ rptype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fe38b-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fe38b-149">**Modify-Methode der MicrosoftDNS- \_ rptype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fe38b-149">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="fe38b-150">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="fe38b-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





