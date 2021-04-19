---
description: Enthält eine einzelne Adresse eines beliebigen Typs unterstützter Adressen.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: ADDRESS2-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356139"
---
# <a name="address2-structure"></a><span data-ttu-id="e6654-103">ADDRESS2-Struktur</span><span class="sxs-lookup"><span data-stu-id="e6654-103">ADDRESS2 structure</span></span>

<span data-ttu-id="e6654-104">Die **Adress** Struktur enthält eine einzelne Adresse eines beliebigen Typs unterstützter Adressen.</span><span class="sxs-lookup"><span data-stu-id="e6654-104">The **ADDRESS** structure contains a single address of any type of supported addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6654-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6654-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a><span data-ttu-id="e6654-106">Member</span><span class="sxs-lookup"><span data-stu-id="e6654-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6654-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="e6654-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-108">Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="e6654-108">Address type.</span></span> <span data-ttu-id="e6654-109">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e6654-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="e6654-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="e6654-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="e6654-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="e6654-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="e6654-112">ADDRESS_TYPE_IP6</span><span class="sxs-lookup"><span data-stu-id="e6654-112">ADDRESS_TYPE_IP6</span></span></dd> <dd><span data-ttu-id="e6654-113">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="e6654-113">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="e6654-114">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="e6654-114">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="e6654-115">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="e6654-115">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="e6654-116">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="e6654-116">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="e6654-117">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="e6654-117">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="e6654-118">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="e6654-118">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="e6654-119">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="e6654-119">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="e6654-120">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="e6654-120">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="e6654-121">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="e6654-121">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="e6654-122">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="e6654-122">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="e6654-123">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="e6654-123">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="e6654-124">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-124">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-125">Anzeigen der Daten, die als unformatierte Mac-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-125">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-126">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-126">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-127">Sicht der Daten, die als unformatierte IP-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-127">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-128">**IP6Address**</span><span class="sxs-lookup"><span data-stu-id="e6654-128">**IP6Address**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-129">Anzeigen der Daten, die als Rohdaten der IP-Version 6 ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-129">View of the data expressed as a raw IP version 6 address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-130">**Ipxrawaddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-130">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-131">Sicht der Daten, die als unformatierte IPX-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-131">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-132">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-132">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-133">Sicht der Daten, die als decodierte IPX-Adress Werte ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-133">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-134">**Vinesiprawaddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-134">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-135">Anzeigen der Daten, die als Rohdaten für die Reben-IP-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-135">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-136">**Vinesipaddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-136">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-137">Ansicht der Daten, die als decodierte IP-Adresse für die Reben ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-137">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-138">**Ethernetzrcaddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-138">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-139">Sicht der Daten, die als Ethernet-Quelladresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-139">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-140">**Ethernetdstaddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-140">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-141">Sicht der Daten, die als Ethernet-Zieladresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-141">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-142">**"Dekenringsrcaddress"**</span><span class="sxs-lookup"><span data-stu-id="e6654-142">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-143">Eine Ansicht der Daten als Quelladresse für den Tokenring.</span><span class="sxs-lookup"><span data-stu-id="e6654-143">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-144">**Verzeichnis-dstaddress**</span><span class="sxs-lookup"><span data-stu-id="e6654-144">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-145">Eine Ansicht der Daten als Zieladresse für den Tokenring.</span><span class="sxs-lookup"><span data-stu-id="e6654-145">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-146">**"Rddisrcaddress"**</span><span class="sxs-lookup"><span data-stu-id="e6654-146">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-147">Sicht der Daten, die als eine "f"-Quelladresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-147">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-148">**"F"**</span><span class="sxs-lookup"><span data-stu-id="e6654-148">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e6654-149">Die Ansicht der Daten, die als eine Adresse für ein BDI-Ziel ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e6654-149">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="e6654-150">**Flags**</span><span class="sxs-lookup"><span data-stu-id="e6654-150">**Flags**</span></span>
<span data-ttu-id="e6654-151"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e6654-151"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e6654-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6654-152">Requirements</span></span>



| <span data-ttu-id="e6654-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6654-153">Requirement</span></span> | <span data-ttu-id="e6654-154">Wert</span><span class="sxs-lookup"><span data-stu-id="e6654-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6654-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6654-155">Minimum supported client</span></span><br/> | <span data-ttu-id="e6654-156">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6654-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e6654-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6654-157">Minimum supported server</span></span><br/> | <span data-ttu-id="e6654-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6654-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6654-159">Header</span><span class="sxs-lookup"><span data-stu-id="e6654-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6654-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6654-160"><dt>Netmon.h</dt></span></span> </dl> |



 

 




