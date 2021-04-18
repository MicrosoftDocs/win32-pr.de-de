---
description: Ist veraltet und sollte nicht verwendet werden.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Adressstruktur (Netmon. h)
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358494"
---
# <a name="address-structure"></a><span data-ttu-id="ca6d8-103">Adressstruktur</span><span class="sxs-lookup"><span data-stu-id="ca6d8-103">ADDRESS structure</span></span>

<span data-ttu-id="ca6d8-104">Die **Adress** Struktur ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-104">The **ADDRESS** structure is obsolete and should not be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca6d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca6d8-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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



## <a name="members"></a><span data-ttu-id="ca6d8-106">Member</span><span class="sxs-lookup"><span data-stu-id="ca6d8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca6d8-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-108">Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-108">Address type.</span></span> <span data-ttu-id="ca6d8-109">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ca6d8-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="ca6d8-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="ca6d8-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="ca6d8-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="ca6d8-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="ca6d8-112">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="ca6d8-112">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="ca6d8-113">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="ca6d8-113">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="ca6d8-114">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="ca6d8-114">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="ca6d8-115">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="ca6d8-115">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="ca6d8-116">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="ca6d8-116">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="ca6d8-117">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="ca6d8-117">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="ca6d8-118">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="ca6d8-118">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="ca6d8-119">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="ca6d8-119">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="ca6d8-120">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="ca6d8-120">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="ca6d8-121">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="ca6d8-121">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="ca6d8-122">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="ca6d8-122">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="ca6d8-123">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-123">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-124">Anzeigen der Daten, die als unformatierte Mac-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-124">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-125">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-125">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-126">Sicht der Daten, die als unformatierte IP-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-126">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-127">**Ipxrawaddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-127">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-128">Sicht der Daten, die als unformatierte IPX-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-128">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-129">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-129">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-130">Sicht der Daten, die als decodierte IPX-Adress Werte ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-130">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-131">**Vinesiprawaddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-131">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-132">Anzeigen der Daten, die als Rohdaten für die Reben-IP-Adresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-132">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-133">**Vinesipaddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-133">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-134">Ansicht der Daten, die als decodierte IP-Adresse für die Reben ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-134">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-135">**Ethernetzrcaddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-135">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-136">Sicht der Daten, die als Ethernet-Quelladresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-136">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-137">**Ethernetdstaddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-137">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-138">Sicht der Daten, die als Ethernet-Zieladresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-138">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-139">**"Dekenringsrcaddress"**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-139">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-140">Eine Ansicht der Daten als Quelladresse für den Tokenring.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-140">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-141">**Verzeichnis-dstaddress**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-141">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-142">Eine Ansicht der Daten als Zieladresse für den Tokenring.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-142">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-143">**"Rddisrcaddress"**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-143">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-144">Sicht der Daten, die als eine "f"-Quelladresse ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-144">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-145">**"F"**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-145">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-146">Die Ansicht der Daten, die als eine Adresse für ein BDI-Ziel ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-146">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ca6d8-147">**Flags**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-147">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ca6d8-148">Ein Satz von Flags, die die Adress Eigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-148">A set of flags that modify the address properties.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca6d8-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca6d8-149">Requirements</span></span>



| <span data-ttu-id="ca6d8-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca6d8-150">Requirement</span></span> | <span data-ttu-id="ca6d8-151">Wert</span><span class="sxs-lookup"><span data-stu-id="ca6d8-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6d8-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca6d8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ca6d8-153">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca6d8-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ca6d8-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca6d8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ca6d8-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca6d8-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ca6d8-156">Header</span><span class="sxs-lookup"><span data-stu-id="ca6d8-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca6d8-157"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca6d8-157"><dt>Netmon.h</dt></span></span> </dl> |



 

 




