---
title: MicrosoftDNS_MINFOType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen e-Mail-Informations Eintrag (MINFO) darstellt.
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- DNS-MicrosoftDNS_MINFOType Klasse
- DNS-MicrosoftDNS_MINFOType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105938"
---
# <a name="microsoftdns_minfotype-class"></a><span data-ttu-id="cbd0c-105">MicrosoftDNS- \_ minfotype-Klasse</span><span class="sxs-lookup"><span data-stu-id="cbd0c-105">MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="cbd0c-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen e-Mail-Informations Eintrag (MINFO) darstellt.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Information (MINFO) record.</span></span>

<span data-ttu-id="cbd0c-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd0c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbd0c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a><span data-ttu-id="cbd0c-109">Member</span><span class="sxs-lookup"><span data-stu-id="cbd0c-109">Members</span></span>

<span data-ttu-id="cbd0c-110">Die **MicrosoftDNS- \_ minfotype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cbd0c-110">The **MicrosoftDNS\_MINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="cbd0c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="cbd0c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cbd0c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbd0c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cbd0c-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="cbd0c-113">Methods</span></span>

<span data-ttu-id="cbd0c-114">Die **MicrosoftDNS- \_ minfotype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-114">The **MicrosoftDNS\_MINFOType** class has these methods.</span></span>



| <span data-ttu-id="cbd0c-115">Methode</span><span class="sxs-lookup"><span data-stu-id="cbd0c-115">Method</span></span>                             | <span data-ttu-id="cbd0c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbd0c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd0c-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="cbd0c-118">Instanziiert einen MINFO-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name des e-Mail-Listen/-Felds, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und die entsprechenden Postfächer.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-118">Instantiates an MINFO Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail list/box, class (default = IN), time-to-live value and the responsible and error mailboxes.</span></span> <span data-ttu-id="cbd0c-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="cbd0c-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="cbd0c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="cbd0c-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-121">**Modify**</span></span>                         | <span data-ttu-id="cbd0c-122">Diese Methode aktualisiert die TTL, das verantwortliche Postfach und das Fehler Postfach auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-122">This method updates the TTL, Responsible Mailbox, and Error Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="cbd0c-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="cbd0c-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="cbd0c-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="cbd0c-125">Qualifiers: Implemented</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="cbd0c-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbd0c-126">Properties</span></span>

<span data-ttu-id="cbd0c-127">Die **MicrosoftDNS- \_ minfotype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-127">The **MicrosoftDNS\_MINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbd0c-128">**Errormailbox**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-128">**ErrorMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbd0c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbd0c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbd0c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbd0c-131">FQDN, der ein Postfach für den Empfang von Fehlermeldungen in Bezug auf die Mailingliste oder das Postfach angibt, das durch den Besitzer Namen des MINFO-Datensatzes angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-131">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="cbd0c-132">**"Verantworblemailbox"**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-132">**ResponsibleMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbd0c-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbd0c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbd0c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbd0c-135">Der voll qualifizierte Name ist ein Postfach, das für die Mailingliste oder das Postfach zuständig ist, die im Besitzer Namen des Datensatzes angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cbd0c-135">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbd0c-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbd0c-136">Requirements</span></span>



| <span data-ttu-id="cbd0c-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbd0c-137">Requirement</span></span> | <span data-ttu-id="cbd0c-138">Wert</span><span class="sxs-lookup"><span data-stu-id="cbd0c-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd0c-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbd0c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd0c-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cbd0c-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cbd0c-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbd0c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd0c-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbd0c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cbd0c-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbd0c-143">Namespace</span></span><br/>                | <span data-ttu-id="cbd0c-144">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="cbd0c-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cbd0c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="cbd0c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbd0c-146"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cbd0c-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd0c-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbd0c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd0c-148">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ minfotype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cbd0c-149">**Modify-Methode der MicrosoftDNS- \_ minfotype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-149">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="cbd0c-150">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





