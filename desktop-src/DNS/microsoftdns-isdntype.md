---
title: MicrosoftDNS_ISDNType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen ISDN-Datensatz darstellt.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- DNS-MicrosoftDNS_ISDNType Klasse
- DNS-MicrosoftDNS_ISDNType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e8b50d75f7b6d57226247c978ced45e07b1acc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102958"
---
# <a name="microsoftdns_isdntype-class"></a><span data-ttu-id="735fd-105">MicrosoftDNS \_ isdntype-Klasse</span><span class="sxs-lookup"><span data-stu-id="735fd-105">MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="735fd-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen ISDN-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="735fd-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ISDN record.</span></span>

<span data-ttu-id="735fd-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="735fd-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="735fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="735fd-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a><span data-ttu-id="735fd-109">Member</span><span class="sxs-lookup"><span data-stu-id="735fd-109">Members</span></span>

<span data-ttu-id="735fd-110">Die **MicrosoftDNS- \_ isdntype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="735fd-110">The **MicrosoftDNS\_ISDNType** class has these types of members:</span></span>

-   [<span data-ttu-id="735fd-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="735fd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="735fd-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="735fd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="735fd-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="735fd-113">Methods</span></span>

<span data-ttu-id="735fd-114">Die **MicrosoftDNS- \_ isdntype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="735fd-114">The **MicrosoftDNS\_ISDNType** class has these methods.</span></span>



| <span data-ttu-id="735fd-115">Methode</span><span class="sxs-lookup"><span data-stu-id="735fd-115">Method</span></span>                             | <span data-ttu-id="735fd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="735fd-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="735fd-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="735fd-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="735fd-118">Instanziiert einen ISDN-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und der ISDN-Nummer und der unter Adresse des Besitzers.</span><span class="sxs-lookup"><span data-stu-id="735fd-118">Instantiates an ISDN Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the ISDN number and subaddress of the owner.</span></span> <span data-ttu-id="735fd-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="735fd-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="735fd-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="735fd-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="735fd-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="735fd-121">**Modify**</span></span>                         | <span data-ttu-id="735fd-122">Aktualisiert die Gültigkeitsdauer, die ISDN-Nummer und die unter Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="735fd-122">Updates the TTL, ISDN Number, and Subaddress to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="735fd-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="735fd-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="735fd-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="735fd-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="735fd-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="735fd-125">Qualifiers: Implemented</span></span><br/>                   |



 

### <a name="properties"></a><span data-ttu-id="735fd-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="735fd-126">Properties</span></span>

<span data-ttu-id="735fd-127">Die **MicrosoftDNS- \_ isdntype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="735fd-127">The **MicrosoftDNS\_ISDNType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="735fd-128">**Isdnnumber**</span><span class="sxs-lookup"><span data-stu-id="735fd-128">**ISDNNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="735fd-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="735fd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="735fd-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="735fd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="735fd-131">ISDN-Nummer und DDI für den Besitzer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="735fd-131">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="735fd-132">**Unter Adresse**</span><span class="sxs-lookup"><span data-stu-id="735fd-132">**SubAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="735fd-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="735fd-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="735fd-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="735fd-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="735fd-135">Die untergeordnete Adresse des Besitzers, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="735fd-135">Subaddress of the owner, if defined.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="735fd-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="735fd-136">Requirements</span></span>



| <span data-ttu-id="735fd-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="735fd-137">Requirement</span></span> | <span data-ttu-id="735fd-138">Wert</span><span class="sxs-lookup"><span data-stu-id="735fd-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="735fd-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="735fd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="735fd-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="735fd-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="735fd-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="735fd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="735fd-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="735fd-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="735fd-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="735fd-143">Namespace</span></span><br/>                | <span data-ttu-id="735fd-144">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="735fd-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="735fd-145">MOF</span><span class="sxs-lookup"><span data-stu-id="735fd-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="735fd-146"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="735fd-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="735fd-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="735fd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735fd-148">**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ isdntype"**</span><span class="sxs-lookup"><span data-stu-id="735fd-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="735fd-149">**Modify-Methode der MicrosoftDNS- \_ isdntype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="735fd-149">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="735fd-150">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="735fd-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





