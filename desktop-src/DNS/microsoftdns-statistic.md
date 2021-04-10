---
title: MicrosoftDNS_Statistic-Klasse
description: Die MicrosoftDNS- \_ Statistik Klasse stellt eine einzelne DNS-Server Statistik dar.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- DNS-MicrosoftDNS_Statistic Klasse
- DNS-MicrosoftDNS_Statistic Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040884"
---
# <a name="microsoftdns_statistic-class"></a><span data-ttu-id="48162-105">MicrosoftDNS- \_ Statistik Klasse</span><span class="sxs-lookup"><span data-stu-id="48162-105">MicrosoftDNS\_Statistic class</span></span>

<span data-ttu-id="48162-106">Die **MicrosoftDNS- \_ Statistik** Klasse stellt eine einzelne DNS-Server Statistik dar.</span><span class="sxs-lookup"><span data-stu-id="48162-106">The **MicrosoftDNS\_Statistic** class represents a single DNS Server statistic.</span></span>

<span data-ttu-id="48162-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="48162-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="48162-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="48162-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a><span data-ttu-id="48162-109">Member</span><span class="sxs-lookup"><span data-stu-id="48162-109">Members</span></span>

<span data-ttu-id="48162-110">Die **MicrosoftDNS- \_ Statistik** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="48162-110">The **MicrosoftDNS\_Statistic** class has these types of members:</span></span>

-   [<span data-ttu-id="48162-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48162-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48162-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48162-112">Properties</span></span>

<span data-ttu-id="48162-113">Die **MicrosoftDNS- \_ Statistik** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48162-113">The **MicrosoftDNS\_Statistic** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48162-114">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="48162-114">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48162-115">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48162-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48162-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48162-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48162-117">Numerische Darstellung von **CollectionName**.</span><span class="sxs-lookup"><span data-stu-id="48162-117">Numeric representation of **CollectionName**.</span></span>

</dd> <dt>

<span data-ttu-id="48162-118">**CollectionName**</span><span class="sxs-lookup"><span data-stu-id="48162-118">**CollectionName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48162-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48162-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48162-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48162-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48162-121">Der Name der Sammlung, zu der die Statistik gehört.</span><span class="sxs-lookup"><span data-stu-id="48162-121">Name of the collection to which the statistic belongs.</span></span>

</dd> <dt>

<span data-ttu-id="48162-122">**Dnsservername**</span><span class="sxs-lookup"><span data-stu-id="48162-122">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48162-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48162-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48162-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48162-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48162-125">Gibt den voll qualifizierten Namen oder die IP-Adresse des DNS-Servers an, der die Statistik enthält.</span><span class="sxs-lookup"><span data-stu-id="48162-125">Indicates the FQDN or IP address of the DNS Server that contains the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="48162-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="48162-126">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48162-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48162-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48162-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48162-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48162-129">Der Name der Statistik.</span><span class="sxs-lookup"><span data-stu-id="48162-129">Name of the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="48162-130">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="48162-130">**StringValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48162-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48162-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48162-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48162-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48162-133">Der Zeichen folgen Wert der Statistik, der nur verwendet wird, wenn der Statistik Wert nicht als DWORD dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="48162-133">String value of the statistic, used only when the statistic value is not represented as a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="48162-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="48162-134">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48162-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48162-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48162-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48162-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48162-137">Numerischer Wert der Statistik, dargestellt als DWORD.</span><span class="sxs-lookup"><span data-stu-id="48162-137">Numeric value of the statistic, represented as a DWORD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48162-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48162-138">Requirements</span></span>



| <span data-ttu-id="48162-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48162-139">Requirement</span></span> | <span data-ttu-id="48162-140">Wert</span><span class="sxs-lookup"><span data-stu-id="48162-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48162-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48162-141">Minimum supported client</span></span><br/> | <span data-ttu-id="48162-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="48162-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="48162-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48162-143">Minimum supported server</span></span><br/> | <span data-ttu-id="48162-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48162-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="48162-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="48162-145">Namespace</span></span><br/>                | <span data-ttu-id="48162-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="48162-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="48162-147">MOF</span><span class="sxs-lookup"><span data-stu-id="48162-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48162-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48162-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48162-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48162-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48162-150">MicrosoftDNS \_ statisticcollection</span><span class="sxs-lookup"><span data-stu-id="48162-150">MicrosoftDNS\_StatisticCollection</span></span>](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





