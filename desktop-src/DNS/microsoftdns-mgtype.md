---
title: MicrosoftDNS_MGType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen e-Mail-Datensatz (mg) darstellt.
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- DNS-MicrosoftDNS_MGType Klasse
- DNS-MicrosoftDNS_MGType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518971"
---
# <a name="microsoftdns_mgtype-class"></a><span data-ttu-id="f236c-105">MicrosoftDNS- \_ mgtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="f236c-105">MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="f236c-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen e-Mail-Datensatz (mg) darstellt.</span><span class="sxs-lookup"><span data-stu-id="f236c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Group (MG) record.</span></span>

<span data-ttu-id="f236c-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f236c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f236c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f236c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a><span data-ttu-id="f236c-109">Member</span><span class="sxs-lookup"><span data-stu-id="f236c-109">Members</span></span>

<span data-ttu-id="f236c-110">Die **MicrosoftDNS- \_ mgtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f236c-110">The **MicrosoftDNS\_MGType** class has these types of members:</span></span>

-   [<span data-ttu-id="f236c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f236c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f236c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f236c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f236c-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="f236c-113">Methods</span></span>

<span data-ttu-id="f236c-114">Die **MicrosoftDNS- \_ mgtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f236c-114">The **MicrosoftDNS\_MGType** class has these methods.</span></span>



| <span data-ttu-id="f236c-115">Methode</span><span class="sxs-lookup"><span data-stu-id="f236c-115">Method</span></span>                             | <span data-ttu-id="f236c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f236c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f236c-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="f236c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="f236c-118">Diese Methode instanziiert einen mg-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name der Mail Gruppe, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und der Name des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="f236c-118">This method instantiates an MG Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail group, class (default = IN), time-to-live value and the mailbox name.</span></span> <span data-ttu-id="f236c-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f236c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="f236c-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="f236c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="f236c-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="f236c-121">**Modify**</span></span>                         | <span data-ttu-id="f236c-122">Diese Methode aktualisiert das TTL-und mg-Postfach auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f236c-122">This method updates the TTL and MG Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="f236c-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="f236c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="f236c-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f236c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="f236c-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="f236c-125">Qualifiers: Implemented</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="f236c-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f236c-126">Properties</span></span>

<span data-ttu-id="f236c-127">Die **MicrosoftDNS- \_ mgtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f236c-127">The **MicrosoftDNS\_MGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f236c-128">**Mgmailbox**</span><span class="sxs-lookup"><span data-stu-id="f236c-128">**MGMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f236c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f236c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f236c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f236c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f236c-131">FQDN, der ein Postfach angibt, das Mitglied der durch den Besitzer Namen des Datensatzes angegebenen e-Mail-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="f236c-131">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f236c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f236c-132">Requirements</span></span>



| <span data-ttu-id="f236c-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f236c-133">Requirement</span></span> | <span data-ttu-id="f236c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f236c-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f236c-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f236c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f236c-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f236c-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f236c-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f236c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f236c-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f236c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f236c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f236c-139">Namespace</span></span><br/>                | <span data-ttu-id="f236c-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f236c-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f236c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f236c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f236c-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f236c-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f236c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f236c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f236c-144">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mgtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f236c-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f236c-145">**Modify-Methode der MicrosoftDNS- \_ mgtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f236c-145">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="f236c-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="f236c-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





