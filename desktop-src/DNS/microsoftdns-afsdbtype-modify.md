---
title: Modify-Methode der MicrosoftDNS_AFSDBType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für den Andrew File System Database Server (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_AFSDBType-Klasse
- DNS-MicrosoftDNS_AFSDBType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339155"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="752f0-106">Modify-Methode der MicrosoftDNS \_ afsdbtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="752f0-106">Modify method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="752f0-107">Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für den Andrew File System Database Server (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="752f0-107">The **Modify** method updates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="752f0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="752f0-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="752f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="752f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="752f0-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="752f0-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="752f0-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="752f0-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="752f0-112">*Untertyp* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="752f0-112">*Subtype* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="752f0-113">Der Untertyp des Host-AFS-Servers.</span><span class="sxs-lookup"><span data-stu-id="752f0-113">Subtype of the host AFS server.</span></span> <span data-ttu-id="752f0-114">Für den Untertyp 1 (Wert = 1) verfügt der Host über einen mespeicherort-Server der Version 3,0 für die benannte AFS-Zelle.</span><span class="sxs-lookup"><span data-stu-id="752f0-114">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="752f0-115">Im Fall von Untertyp 2 (Wert = 2) verfügt der Host über einen authentifizierten Namen Server, der den Zellen Stammverzeichnis-Knoten für die benannte DCE/NCA-Zelle enthält.</span><span class="sxs-lookup"><span data-stu-id="752f0-115">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="752f0-116">*Servername* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="752f0-116">*ServerName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="752f0-117">Ein voll qualifizierter Host, der einen Host mit einem Server für die im Besitzer Namen angegebene AFS-Zelle angibt.</span><span class="sxs-lookup"><span data-stu-id="752f0-117">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="752f0-118">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="752f0-118">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="752f0-119">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="752f0-119">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="752f0-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="752f0-120">Return value</span></span>

<span data-ttu-id="752f0-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="752f0-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="752f0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="752f0-122">Remarks</span></span>

<span data-ttu-id="752f0-123">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="752f0-123">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="752f0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="752f0-124">Requirements</span></span>



| <span data-ttu-id="752f0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="752f0-125">Requirement</span></span> | <span data-ttu-id="752f0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="752f0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="752f0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="752f0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="752f0-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="752f0-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="752f0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="752f0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="752f0-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="752f0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="752f0-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="752f0-131">Namespace</span></span><br/>                | <span data-ttu-id="752f0-132">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="752f0-132">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="752f0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="752f0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="752f0-134"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="752f0-134"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="752f0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="752f0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="752f0-136">**MicrosoftDNS \_ afsdbtype**</span><span class="sxs-lookup"><span data-stu-id="752f0-136">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="752f0-137">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ afsdbtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="752f0-137">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="752f0-138">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="752f0-138">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





