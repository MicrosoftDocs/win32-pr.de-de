---
title: MicrosoftDNS_AFSDBType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen AFSDB-Datensatz (Andrew File System Database Server) darstellt.
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- DNS-MicrosoftDNS_AFSDBType Klasse
- DNS-MicrosoftDNS_AFSDBType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040624"
---
# <a name="microsoftdns_afsdbtype-class"></a><span data-ttu-id="e10ec-105">MicrosoftDNS \_ afsdbtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="e10ec-105">MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="e10ec-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen AFSDB-Datensatz (Andrew File System Database Server) darstellt.</span><span class="sxs-lookup"><span data-stu-id="e10ec-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an Andrew File System Database Server (AFSDB) record.</span></span>

<span data-ttu-id="e10ec-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e10ec-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e10ec-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a><span data-ttu-id="e10ec-109">Member</span><span class="sxs-lookup"><span data-stu-id="e10ec-109">Members</span></span>

<span data-ttu-id="e10ec-110">Die **MicrosoftDNS \_ afsdbtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e10ec-110">The **MicrosoftDNS\_AFSDBType** class has these types of members:</span></span>

-   [<span data-ttu-id="e10ec-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="e10ec-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e10ec-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e10ec-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e10ec-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="e10ec-113">Methods</span></span>

<span data-ttu-id="e10ec-114">Die **MicrosoftDNS \_ afsdbtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e10ec-114">The **MicrosoftDNS\_AFSDBType** class has these methods.</span></span>



| <span data-ttu-id="e10ec-115">Methode</span><span class="sxs-lookup"><span data-stu-id="e10ec-115">Method</span></span>                             | <span data-ttu-id="e10ec-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e10ec-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10ec-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="e10ec-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e10ec-118">Instanziiert einen AFSDB-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: DNS-Servername des Datensatzes, Container Name, Besitzer/Zellen Name, Klasse (Standard = in), Time-to-Live-Wert und Host-AFS-Server Untertyp und-Name.</span><span class="sxs-lookup"><span data-stu-id="e10ec-118">Instantiates an AFSDB Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Cell Name, class (default = IN), time-to-live value, and host AFS server subtype and name.</span></span> <span data-ttu-id="e10ec-119">Gibt einen Verweis auf das neue-Objekt als Ausgabeparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="e10ec-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e10ec-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="e10ec-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e10ec-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="e10ec-121">**Modify**</span></span>                         | <span data-ttu-id="e10ec-122">Diese Methode aktualisiert die TTL-, Untertyp-und Server Namen auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e10ec-122">This method updates the TTL, Subtype and Server Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e10ec-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="e10ec-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e10ec-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="e10ec-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e10ec-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="e10ec-125">Qualifiers: Implemented</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="e10ec-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e10ec-126">Properties</span></span>

<span data-ttu-id="e10ec-127">Die **MicrosoftDNS \_ afsdbtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e10ec-127">The **MicrosoftDNS\_AFSDBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e10ec-128">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="e10ec-128">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ec-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e10ec-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10ec-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e10ec-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ec-131">Ein voll qualifizierter Host, der einen Host mit einem Server für die im Besitzer Namen angegebene AFS-Zelle angibt.</span><span class="sxs-lookup"><span data-stu-id="e10ec-131">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="e10ec-132">**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="e10ec-132">**Subtype**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ec-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e10ec-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e10ec-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e10ec-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ec-135">Der Untertyp des Host-AFS-Servers.</span><span class="sxs-lookup"><span data-stu-id="e10ec-135">Subtype of the host AFS server.</span></span> <span data-ttu-id="e10ec-136">Für den Untertyp 1 (Wert = 1) verfügt der Host über einen mespeicherort-Server der Version 3,0 für die benannte AFS-Zelle.</span><span class="sxs-lookup"><span data-stu-id="e10ec-136">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="e10ec-137">Im Fall von Untertyp 2 (Wert = 2) verfügt der Host über einen authentifizierten Namen Server, der den Zellen Stammverzeichnis-Knoten für die benannte DCE/NCA-Zelle enthält.</span><span class="sxs-lookup"><span data-stu-id="e10ec-137">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e10ec-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e10ec-138">Requirements</span></span>



| <span data-ttu-id="e10ec-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e10ec-139">Requirement</span></span> | <span data-ttu-id="e10ec-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e10ec-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e10ec-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e10ec-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e10ec-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e10ec-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e10ec-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e10ec-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e10ec-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e10ec-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e10ec-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="e10ec-145">Namespace</span></span><br/>                | <span data-ttu-id="e10ec-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="e10ec-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e10ec-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e10ec-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e10ec-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e10ec-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e10ec-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e10ec-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10ec-150">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ afsdbtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e10ec-150">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e10ec-151">**Modify-Methode der MicrosoftDNS \_ afsdbtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e10ec-151">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="e10ec-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="e10ec-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





