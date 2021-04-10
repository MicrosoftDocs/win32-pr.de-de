---
title: MicrosoftDNS_MXType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen e-Mail-Austausch (Mr) RR darstellt.
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- DNS-MicrosoftDNS_MXType Klasse
- DNS-MicrosoftDNS_MXType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956470"
---
# <a name="microsoftdns_mxtype-class"></a><span data-ttu-id="fb4b1-105">MicrosoftDNS- \_ mxtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb4b1-105">MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="fb4b1-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen e-Mail-Austausch (Mr) RR darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Exchanger (MR) RR.</span></span>

<span data-ttu-id="fb4b1-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4b1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb4b1-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a><span data-ttu-id="fb4b1-109">Member</span><span class="sxs-lookup"><span data-stu-id="fb4b1-109">Members</span></span>

<span data-ttu-id="fb4b1-110">Die **MicrosoftDNS- \_ mxtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb4b1-110">The **MicrosoftDNS\_MXType** class has these types of members:</span></span>

-   [<span data-ttu-id="fb4b1-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="fb4b1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fb4b1-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb4b1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fb4b1-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="fb4b1-113">Methods</span></span>

<span data-ttu-id="fb4b1-114">Die **MicrosoftDNS- \_ mxtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-114">The **MicrosoftDNS\_MXType** class has these methods.</span></span>



| <span data-ttu-id="fb4b1-115">Methode</span><span class="sxs-lookup"><span data-stu-id="fb4b1-115">Method</span></span>                             | <span data-ttu-id="fb4b1-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb4b1-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4b1-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fb4b1-118">Instanziiert einen MX-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer, die Daten Satz Präferenz und der Hostname, der als e-Mail-Austausch bereit ist.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-118">Instantiates an MX Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, record preference, and host name willing to be a mail exchange.</span></span> <span data-ttu-id="fb4b1-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fb4b1-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="fb4b1-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fb4b1-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-121">**Modify**</span></span>                         | <span data-ttu-id="fb4b1-122">Aktualisiert die Gültigkeitsdauer, die Präferenz und den e-Mail-Austausch auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-122">Updates the TTL, Preference, and Mail Exchange to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fb4b1-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fb4b1-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fb4b1-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="fb4b1-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="fb4b1-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb4b1-126">Properties</span></span>

<span data-ttu-id="fb4b1-127">Die **MicrosoftDNS- \_ mxtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-127">The **MicrosoftDNS\_MXType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb4b1-128">**Mailexchange**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-128">**MailExchange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb4b1-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb4b1-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb4b1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb4b1-131">FQDN, der einen Host angibt, der als e-Mail-Austausch für den Namen des Besitzers fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-131">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="fb4b1-132">**Bevorzu**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb4b1-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb4b1-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb4b1-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb4b1-135">Die Einstellung, die diesem RR unter anderem beim gleichen Besitzer zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="fb4b1-136">Niedrigere Werte werden bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="fb4b1-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb4b1-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb4b1-137">Requirements</span></span>



| <span data-ttu-id="fb4b1-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb4b1-138">Requirement</span></span> | <span data-ttu-id="fb4b1-139">Wert</span><span class="sxs-lookup"><span data-stu-id="fb4b1-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4b1-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb4b1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4b1-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fb4b1-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fb4b1-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb4b1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4b1-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb4b1-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fb4b1-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb4b1-144">Namespace</span></span><br/>                | <span data-ttu-id="fb4b1-145">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="fb4b1-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fb4b1-146">MOF</span><span class="sxs-lookup"><span data-stu-id="fb4b1-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb4b1-147"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb4b1-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb4b1-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb4b1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4b1-149">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mxtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fb4b1-150">**Modify-Methode der MicrosoftDNS- \_ mxtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-150">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="fb4b1-151">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="fb4b1-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





