---
title: MicrosoftDNS_MBType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Post Fach Ressourcen Eintrag (MB) darstellt.
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- DNS-MicrosoftDNS_MBType Klasse
- DNS-MicrosoftDNS_MBType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956625"
---
# <a name="microsoftdns_mbtype-class"></a><span data-ttu-id="eee96-105">MicrosoftDNS- \_ mbtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="eee96-105">MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="eee96-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Post Fach Ressourcen Eintrag (MB) darstellt.</span><span class="sxs-lookup"><span data-stu-id="eee96-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox (MB) resource record.</span></span>

<span data-ttu-id="eee96-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="eee96-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eee96-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a><span data-ttu-id="eee96-109">Member</span><span class="sxs-lookup"><span data-stu-id="eee96-109">Members</span></span>

<span data-ttu-id="eee96-110">Die **MicrosoftDNS- \_ mbtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eee96-110">The **MicrosoftDNS\_MBType** class has these types of members:</span></span>

-   [<span data-ttu-id="eee96-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="eee96-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="eee96-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eee96-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eee96-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="eee96-113">Methods</span></span>

<span data-ttu-id="eee96-114">Die **MicrosoftDNS- \_ mbtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eee96-114">The **MicrosoftDNS\_MBType** class has these methods.</span></span>



| <span data-ttu-id="eee96-115">Methode</span><span class="sxs-lookup"><span data-stu-id="eee96-115">Method</span></span>                             | <span data-ttu-id="eee96-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eee96-116">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee96-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="eee96-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="eee96-118">Instanziiert eine MB RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name des Postfachs, die Klasse (Standardwert = in), der Wert für die Gültigkeitsdauer und der Post Fach Host.</span><span class="sxs-lookup"><span data-stu-id="eee96-118">Instantiates an MB RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox host.</span></span> <span data-ttu-id="eee96-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eee96-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="eee96-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="eee96-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="eee96-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="eee96-121">**Modify**</span></span>                         | <span data-ttu-id="eee96-122">Aktualisiert den TTL-und den MB-Host auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eee96-122">Updates the TTL and MB host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="eee96-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="eee96-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="eee96-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="eee96-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="eee96-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="eee96-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="eee96-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eee96-126">Properties</span></span>

<span data-ttu-id="eee96-127">Die **MicrosoftDNS- \_ mbtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eee96-127">The **MicrosoftDNS\_MBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eee96-128">**Mbhost**</span><span class="sxs-lookup"><span data-stu-id="eee96-128">**MBHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee96-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eee96-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eee96-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eee96-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eee96-131">Ein voll qualifizierter Datentyp, der einen Host des Postfachs angibt, der im Besitzer Namen des Datensatzes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="eee96-131">FQDN that specifies a host of the mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eee96-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eee96-132">Requirements</span></span>



| <span data-ttu-id="eee96-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eee96-133">Requirement</span></span> | <span data-ttu-id="eee96-134">Wert</span><span class="sxs-lookup"><span data-stu-id="eee96-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eee96-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eee96-135">Minimum supported client</span></span><br/> | <span data-ttu-id="eee96-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eee96-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eee96-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eee96-137">Minimum supported server</span></span><br/> | <span data-ttu-id="eee96-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eee96-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eee96-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="eee96-139">Namespace</span></span><br/>                | <span data-ttu-id="eee96-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="eee96-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="eee96-141">MOF</span><span class="sxs-lookup"><span data-stu-id="eee96-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eee96-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eee96-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee96-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eee96-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee96-144">**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ mbtype"**</span><span class="sxs-lookup"><span data-stu-id="eee96-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="eee96-145">**Modify-Methode der MicrosoftDNS- \_ Klasse von mbtype**</span><span class="sxs-lookup"><span data-stu-id="eee96-145">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="eee96-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="eee96-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





