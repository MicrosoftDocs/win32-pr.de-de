---
title: MicrosoftDNS_WKSType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Well-Known Services (Wert)-Datensatz darstellt.
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- DNS-MicrosoftDNS_WKSType Klasse
- DNS-MicrosoftDNS_WKSType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7fde08721bb8bb62b93f72b792060b06c15dad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956707"
---
# <a name="microsoftdns_wkstype-class"></a><span data-ttu-id="54ae2-105">MicrosoftDNS- \_ wkstype-Klasse</span><span class="sxs-lookup"><span data-stu-id="54ae2-105">MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="54ae2-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Well-Known Services (Wert)-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="54ae2-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Well-Known Services (WKS) record.</span></span>

<span data-ttu-id="54ae2-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="54ae2-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ae2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="54ae2-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a><span data-ttu-id="54ae2-109">Member</span><span class="sxs-lookup"><span data-stu-id="54ae2-109">Members</span></span>

<span data-ttu-id="54ae2-110">Die **MicrosoftDNS- \_ wkstype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="54ae2-110">The **MicrosoftDNS\_WKSType** class has these types of members:</span></span>

-   [<span data-ttu-id="54ae2-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="54ae2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="54ae2-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ae2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="54ae2-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="54ae2-113">Methods</span></span>

<span data-ttu-id="54ae2-114">Die **MicrosoftDNS- \_ wkstype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="54ae2-114">The **MicrosoftDNS\_WKSType** class has these methods.</span></span>



| <span data-ttu-id="54ae2-115">Methode</span><span class="sxs-lookup"><span data-stu-id="54ae2-115">Method</span></span>                             | <span data-ttu-id="54ae2-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54ae2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ae2-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="54ae2-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="54ae2-118">Instanziiert einen WLS-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und die Internet Adresse, das IP-Protokoll und die Port-Bitmaske des Besitzers.</span><span class="sxs-lookup"><span data-stu-id="54ae2-118">Instantiates a WKS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the owner's Internet Address, IP protocol and port bit mask.</span></span> <span data-ttu-id="54ae2-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54ae2-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="54ae2-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="54ae2-120">Qualifiers: Implemented, static</span></span><br/>  |
| <span data-ttu-id="54ae2-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="54ae2-121">**Modify**</span></span>                         | <span data-ttu-id="54ae2-122">Diese Methode aktualisiert die TTL, die Internet Adresse, das IP-Protokoll und die Dienste auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54ae2-122">This method updates the TTL, Internet Address, IP Protocol, and Services to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="54ae2-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="54ae2-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="54ae2-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="54ae2-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="54ae2-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="54ae2-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="54ae2-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ae2-126">Properties</span></span>

<span data-ttu-id="54ae2-127">Die **MicrosoftDNS- \_ wkstype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54ae2-127">The **MicrosoftDNS\_WKSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54ae2-128">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="54ae2-128">**InternetAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ae2-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54ae2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54ae2-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ae2-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54ae2-131">Internet-IP-Adresse für den Besitzer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="54ae2-131">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="54ae2-132">**IPProtocol**</span><span class="sxs-lookup"><span data-stu-id="54ae2-132">**IPProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ae2-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54ae2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54ae2-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ae2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54ae2-135">Zeichenfolge, die das IP-Protokoll für diesen Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="54ae2-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="54ae2-136">Gültige Werte sind UDP oder TCP.</span><span class="sxs-lookup"><span data-stu-id="54ae2-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="54ae2-137">**Dienste**</span><span class="sxs-lookup"><span data-stu-id="54ae2-137">**Services**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ae2-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54ae2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54ae2-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ae2-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54ae2-140">Eine Zeichenfolge, die alle Dienste enthält, die vom Wi-Datensatz (well known Service) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54ae2-140">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54ae2-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54ae2-141">Requirements</span></span>



| <span data-ttu-id="54ae2-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54ae2-142">Requirement</span></span> | <span data-ttu-id="54ae2-143">Wert</span><span class="sxs-lookup"><span data-stu-id="54ae2-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54ae2-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54ae2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="54ae2-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="54ae2-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54ae2-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54ae2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="54ae2-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54ae2-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54ae2-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="54ae2-148">Namespace</span></span><br/>                | <span data-ttu-id="54ae2-149">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="54ae2-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="54ae2-150">MOF</span><span class="sxs-lookup"><span data-stu-id="54ae2-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54ae2-151"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="54ae2-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ae2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54ae2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ae2-153">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "wkstype"**</span><span class="sxs-lookup"><span data-stu-id="54ae2-153">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="54ae2-154">**Modify-Methode der MicrosoftDNS- \_ Klasse "wkstype"**</span><span class="sxs-lookup"><span data-stu-id="54ae2-154">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="54ae2-155">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="54ae2-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





