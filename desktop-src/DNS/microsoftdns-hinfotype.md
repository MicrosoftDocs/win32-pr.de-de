---
title: MicrosoftDNS_HINFOType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen hinfo-Datensatz darstellt.
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- DNS-MicrosoftDNS_HINFOType Klasse
- DNS-MicrosoftDNS_HINFOType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339351"
---
# <a name="microsoftdns_hinfotype-class"></a><span data-ttu-id="a8466-105">MicrosoftDNS- \_ hinfotype-Klasse</span><span class="sxs-lookup"><span data-stu-id="a8466-105">MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="a8466-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen hinfo-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8466-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Host Information (HINFO) record.</span></span>

<span data-ttu-id="a8466-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="a8466-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8466-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8466-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a><span data-ttu-id="a8466-109">Member</span><span class="sxs-lookup"><span data-stu-id="a8466-109">Members</span></span>

<span data-ttu-id="a8466-110">Die **MicrosoftDNS- \_ hinfotype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a8466-110">The **MicrosoftDNS\_HINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="a8466-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a8466-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a8466-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8466-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a8466-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="a8466-113">Methods</span></span>

<span data-ttu-id="a8466-114">Die **MicrosoftDNS- \_ hinfotype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a8466-114">The **MicrosoftDNS\_HINFOType** class has these methods.</span></span>



| <span data-ttu-id="a8466-115">Methode</span><span class="sxs-lookup"><span data-stu-id="a8466-115">Method</span></span>                             | <span data-ttu-id="a8466-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8466-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8466-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="a8466-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a8466-118">Instanziiert eine hinfo von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name, die Klasse (Standard = in), der Gültigkeitsdauer Wert und die CPU-und Betriebssystem Typen des Hosts.</span><span class="sxs-lookup"><span data-stu-id="a8466-118">Instantiates an HINFO of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the host's CPU and operating system types.</span></span> <span data-ttu-id="a8466-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8466-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a8466-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="a8466-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a8466-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="a8466-121">**Modify**</span></span>                         | <span data-ttu-id="a8466-122">Aktualisiert die Gültigkeitsdauer, CPU und das Betriebssystem auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a8466-122">Updates the TTL, CPU, and operating system to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a8466-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="a8466-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a8466-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="a8466-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a8466-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="a8466-125">Qualifiers: Implemented</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="a8466-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8466-126">Properties</span></span>

<span data-ttu-id="a8466-127">Die **MicrosoftDNS- \_ hinfotype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a8466-127">The **MicrosoftDNS\_HINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8466-128">**CPU**</span><span class="sxs-lookup"><span data-stu-id="a8466-128">**CPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8466-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a8466-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8466-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a8466-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8466-131">Der CPU-Typ des Daten Satz Besitzers.</span><span class="sxs-lookup"><span data-stu-id="a8466-131">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="a8466-132">**Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="a8466-132">**OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8466-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a8466-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8466-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a8466-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8466-135">Das Betriebssystem des Daten Satz Besitzers.</span><span class="sxs-lookup"><span data-stu-id="a8466-135">Operating system of the record owner.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8466-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8466-136">Requirements</span></span>



| <span data-ttu-id="a8466-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8466-137">Requirement</span></span> | <span data-ttu-id="a8466-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a8466-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8466-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8466-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a8466-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a8466-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a8466-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8466-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a8466-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8466-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8466-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8466-143">Namespace</span></span><br/>                | <span data-ttu-id="a8466-144">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="a8466-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a8466-145">MOF</span><span class="sxs-lookup"><span data-stu-id="a8466-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8466-146"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a8466-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8466-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8466-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8466-148">**Methode "kreateinstancefrompropertydata" der "hinfotype"-Klasse von MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="a8466-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a8466-149">**Modify-Methode der MicrosoftDNS- \_ hinfotype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a8466-149">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="a8466-150">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="a8466-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





