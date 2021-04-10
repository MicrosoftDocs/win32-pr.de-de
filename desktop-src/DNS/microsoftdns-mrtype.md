---
title: MicrosoftDNS_MRType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Post Fach Umbenennungs Eintrag (Mr) darstellt.
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- DNS-MicrosoftDNS_MRType Klasse
- DNS-MicrosoftDNS_MRType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105255"
---
# <a name="microsoftdns_mrtype-class"></a><span data-ttu-id="11301-105">MicrosoftDNS- \_ mrtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="11301-105">MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="11301-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Post Fach Umbenennungs Eintrag (Mr) darstellt.</span><span class="sxs-lookup"><span data-stu-id="11301-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox Rename (MR) record.</span></span>

<span data-ttu-id="11301-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="11301-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="11301-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="11301-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a><span data-ttu-id="11301-109">Member</span><span class="sxs-lookup"><span data-stu-id="11301-109">Members</span></span>

<span data-ttu-id="11301-110">Die **MicrosoftDNS- \_ mrtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11301-110">The **MicrosoftDNS\_MRType** class has these types of members:</span></span>

-   [<span data-ttu-id="11301-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="11301-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="11301-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11301-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="11301-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="11301-113">Methods</span></span>

<span data-ttu-id="11301-114">Die **MicrosoftDNS- \_ mrtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="11301-114">The **MicrosoftDNS\_MRType** class has these methods.</span></span>



| <span data-ttu-id="11301-115">Methode</span><span class="sxs-lookup"><span data-stu-id="11301-115">Method</span></span>                             | <span data-ttu-id="11301-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11301-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11301-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="11301-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="11301-118">Diese Methode instanziiert einen ' Mr '-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name des Postfachs, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und die Umbenennen des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="11301-118">This method instantiates an 'MR' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox rename.</span></span> <span data-ttu-id="11301-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11301-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="11301-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="11301-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="11301-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="11301-121">**Modify**</span></span>                         | <span data-ttu-id="11301-122">Diese Methode aktualisiert das TTL-und Mr-Postfach auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="11301-122">This method updates the TTL and MR Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="11301-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="11301-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="11301-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="11301-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="11301-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="11301-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="11301-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11301-126">Properties</span></span>

<span data-ttu-id="11301-127">Die **MicrosoftDNS- \_ mrtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11301-127">The **MicrosoftDNS\_MRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11301-128">**Mrmailbox**</span><span class="sxs-lookup"><span data-stu-id="11301-128">**MRMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11301-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11301-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11301-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11301-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11301-131">Der voll qualifizierte Name des Postfachs, bei dem es sich um den ordnungsgemäßen Umbenennen des im Namen des Datensatzes angegebenen Postfachs handelt</span><span class="sxs-lookup"><span data-stu-id="11301-131">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11301-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11301-132">Requirements</span></span>



| <span data-ttu-id="11301-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11301-133">Requirement</span></span> | <span data-ttu-id="11301-134">Wert</span><span class="sxs-lookup"><span data-stu-id="11301-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11301-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11301-135">Minimum supported client</span></span><br/> | <span data-ttu-id="11301-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11301-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="11301-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11301-137">Minimum supported server</span></span><br/> | <span data-ttu-id="11301-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11301-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="11301-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="11301-139">Namespace</span></span><br/>                | <span data-ttu-id="11301-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="11301-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="11301-141">MOF</span><span class="sxs-lookup"><span data-stu-id="11301-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11301-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="11301-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11301-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11301-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11301-144">**Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ mrtype"**</span><span class="sxs-lookup"><span data-stu-id="11301-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="11301-145">**Modify-Methode der MicrosoftDNS- \_ mrtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="11301-145">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="11301-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="11301-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





