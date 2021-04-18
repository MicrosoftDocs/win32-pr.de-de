---
description: Der Adresstyp identifiziert das Adressformat, z. b. die Standard Telefonnummer oder e-Mail-Adresse Nur Anwendungen, die TAPI-Version 3,0 oder höher aushandeln, können Adresstypen verwenden.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: LINEADDRESSTYPE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364949"
---
# <a name="lineaddresstype_-constants"></a><span data-ttu-id="e1710-104">Lineadresssstype- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="e1710-104">LINEADDRESSTYPE\_ Constants</span></span>

<span data-ttu-id="e1710-105">Der Adresstyp identifiziert das Adressformat, z. b. die Standard Telefonnummer oder e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="e1710-105">The address type identifies address format, such as standard phone number or e-mail address.</span></span> <span data-ttu-id="e1710-106">Nur Anwendungen, die TAPI-Version 3,0 oder höher aushandeln, können Adresstypen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1710-106">Only applications that negotiate TAPI version 3.0 or higher can use address types.</span></span>

<dl> <dt>

<span data-ttu-id="e1710-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**lineadresssstype \_ PhoneNumber**</span><span class="sxs-lookup"><span data-stu-id="e1710-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE\_PHONENUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1710-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e1710-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e1710-109">Address Type ist eine Standard Telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="e1710-109">Address type is a standard phone number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1710-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**lineadresssstype \_ SDP**</span><span class="sxs-lookup"><span data-stu-id="e1710-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE\_SDP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1710-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e1710-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e1710-112">Der Adresstyp ist die Sitzungs Beschreibungs-Protokoll Konferenz (SDP).</span><span class="sxs-lookup"><span data-stu-id="e1710-112">Address type is Session Description Protocol (SDP) conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1710-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**"lineadresstype \_ emailname"**</span><span class="sxs-lookup"><span data-stu-id="e1710-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE\_EMAILNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1710-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e1710-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e1710-115">Der Adresstyp ist ein e-Mail-Name.</span><span class="sxs-lookup"><span data-stu-id="e1710-115">Address type is an e-mail name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1710-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**Name der lineadresssstype- \_ Domäne**</span><span class="sxs-lookup"><span data-stu-id="e1710-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1710-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e1710-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="e1710-118">Der Adresstyp ist ein Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="e1710-118">Address type is a domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1710-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**lineadresssstype- \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="e1710-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE\_IPADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1710-120">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e1710-120">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="e1710-121">Address Type ist eine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e1710-121">Address type is an IP address.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1710-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1710-122">Requirements</span></span>



| <span data-ttu-id="e1710-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1710-123">Requirement</span></span> | <span data-ttu-id="e1710-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e1710-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e1710-125">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e1710-125">TAPI version</span></span><br/> | <span data-ttu-id="e1710-126">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e1710-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e1710-127">Header</span><span class="sxs-lookup"><span data-stu-id="e1710-127">Header</span></span><br/>       | <dl> <span data-ttu-id="e1710-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1710-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




