---
title: MicrosoftDNS_TXTType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Text Eintrag (txt) darstellt.
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- DNS-MicrosoftDNS_TXTType Klasse
- DNS-MicrosoftDNS_TXTType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342469"
---
# <a name="microsoftdns_txttype-class"></a><span data-ttu-id="03de8-105">MicrosoftDNS- \_ txttype-Klasse</span><span class="sxs-lookup"><span data-stu-id="03de8-105">MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="03de8-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Text Eintrag (txt) darstellt.</span><span class="sxs-lookup"><span data-stu-id="03de8-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Text (TXT) record.</span></span>

<span data-ttu-id="03de8-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="03de8-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="03de8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="03de8-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a><span data-ttu-id="03de8-109">Member</span><span class="sxs-lookup"><span data-stu-id="03de8-109">Members</span></span>

<span data-ttu-id="03de8-110">Die **MicrosoftDNS- \_ txttype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="03de8-110">The **MicrosoftDNS\_TXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="03de8-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="03de8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="03de8-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03de8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="03de8-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="03de8-113">Methods</span></span>

<span data-ttu-id="03de8-114">Die **MicrosoftDNS- \_ txttype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="03de8-114">The **MicrosoftDNS\_TXTType** class has these methods.</span></span>



| <span data-ttu-id="03de8-115">Methode</span><span class="sxs-lookup"><span data-stu-id="03de8-115">Method</span></span>                             | <span data-ttu-id="03de8-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03de8-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03de8-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="03de8-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="03de8-118">Instanziiert einen txt-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem Text des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="03de8-118">Instantiates a TXT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the record's text.</span></span> <span data-ttu-id="03de8-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03de8-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="03de8-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="03de8-120">Qualifiers: Implemented, static</span></span><br/>        |
| <span data-ttu-id="03de8-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="03de8-121">**Modify**</span></span>                         | <span data-ttu-id="03de8-122">Aktualisiert die Gültigkeitsdauer und den beschreibenden Text auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="03de8-122">Updates the TTL and Descriptive Text to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="03de8-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="03de8-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="03de8-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="03de8-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="03de8-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="03de8-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="03de8-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03de8-126">Properties</span></span>

<span data-ttu-id="03de8-127">Die **MicrosoftDNS- \_ txttype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="03de8-127">The **MicrosoftDNS\_TXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03de8-128">**Deskriptivetext**</span><span class="sxs-lookup"><span data-stu-id="03de8-128">**DescriptiveText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03de8-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="03de8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03de8-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03de8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03de8-131">Beschreibender Text, die Semantik, von der abhängig von der Besitzer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="03de8-131">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03de8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03de8-132">Requirements</span></span>



| <span data-ttu-id="03de8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03de8-133">Requirement</span></span> | <span data-ttu-id="03de8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="03de8-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03de8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03de8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="03de8-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="03de8-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="03de8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03de8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="03de8-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03de8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="03de8-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="03de8-139">Namespace</span></span><br/>                | <span data-ttu-id="03de8-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="03de8-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="03de8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="03de8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03de8-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="03de8-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03de8-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03de8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03de8-144">**Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "txttype"**</span><span class="sxs-lookup"><span data-stu-id="03de8-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="03de8-145">**Modify-Methode der MicrosoftDNS \_ txttype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="03de8-145">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="03de8-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="03de8-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





