---
description: Die networkinfo-Struktur beschreibt eine NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Networkinfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760129"
---
# <a name="networkinfo-structure"></a><span data-ttu-id="d6438-103">Networkinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="d6438-103">NETWORKINFO structure</span></span>

<span data-ttu-id="d6438-104">Die networkinfo-Struktur beschreibt eine NIC.</span><span class="sxs-lookup"><span data-stu-id="d6438-104">The NETWORKINFO structure describes a NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6438-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6438-105">Syntax</span></span>


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a><span data-ttu-id="d6438-106">Member</span><span class="sxs-lookup"><span data-stu-id="d6438-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d6438-107">**Permanent addr**</span><span class="sxs-lookup"><span data-stu-id="d6438-107">**PermanentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-108">Permanente Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d6438-108">Permanent MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-109">**Currentaddr**</span><span class="sxs-lookup"><span data-stu-id="d6438-109">**CurrentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-110">Aktuelle Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d6438-110">Current MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-111">**OtherAddress**</span><span class="sxs-lookup"><span data-stu-id="d6438-111">**OtherAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-112">Weitere Adresse, die dies unterstützt (z. b. IP, IPX).</span><span class="sxs-lookup"><span data-stu-id="d6438-112">Other address that support this (for example IP, IPX).</span></span>

</dd> <dt>

<span data-ttu-id="d6438-113">**LinkSpeed**</span><span class="sxs-lookup"><span data-stu-id="d6438-113">**LinkSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-114">Verbindungsgeschwindigkeit in Mbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6438-114">Link speed, in Mbps.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="d6438-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-116">Medientyp.</span><span class="sxs-lookup"><span data-stu-id="d6438-116">Media type.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-117">**MaxFrameSize**</span><span class="sxs-lookup"><span data-stu-id="d6438-117">**MaxFrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-118">Maximale Frame Größe zulässig.</span><span class="sxs-lookup"><span data-stu-id="d6438-118">Maximum frame size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-119">**Flags**</span><span class="sxs-lookup"><span data-stu-id="d6438-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-120">Dieser Parameter kann eine der folgenden informationsflags sein:</span><span class="sxs-lookup"><span data-stu-id="d6438-120">This parameter can be one of the following informational flags:</span></span>



| <span data-ttu-id="d6438-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d6438-121">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="d6438-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d6438-122">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <span data-ttu-id="d6438-123"><dt>**networkinfo- \_ Flags \_ pmode \_ \_ wird nicht unterstützt.**</dt></span><span class="sxs-lookup"><span data-stu-id="d6438-123"><dt>**NETWORKINFO\_FLAGS\_PMODE\_NOT\_SUPPORTED**</dt></span></span> </dl>    | <span data-ttu-id="d6438-124">Die Netzwerkkarte unterstützt den gemischten-Modus nicht. Dies bedeutet, dass nur Datenverkehr erfasst wird, der in der Natur übertragen wird, oder nur den lokalen Computer einbezieht.</span><span class="sxs-lookup"><span data-stu-id="d6438-124">The network card does not support promiscuous mode, meaning that it will only capture traffic which is broadcast in nature or only involves the local machine.</span></span><br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <span data-ttu-id="d6438-125"><dt>**networkinfo- \_ Flags ( \_ RAS)**</dt></span><span class="sxs-lookup"><span data-stu-id="d6438-125"><dt>**NETWORKINFO\_FLAGS\_RAS**</dt></span></span> </dl>                                                      | <span data-ttu-id="d6438-126">Dies ist eine virtuelle Netzwerkkarte, bei der es sich um eine RAS-Verbindung (RAS-Server) über ein Modem oder eine andere Netzwerkkarte handelt.</span><span class="sxs-lookup"><span data-stu-id="d6438-126">This is a virtual network card that is a RAS (Remote Access Server) connection through a modem or another network card.</span></span><br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <span data-ttu-id="d6438-127"><dt>**networkinfo- \_ Flags- \_ Remote \_ Karte**</dt></span><span class="sxs-lookup"><span data-stu-id="d6438-127"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_CARD**</dt></span></span> </dl>                             | <span data-ttu-id="d6438-128">Die Netzwerkkarte befindet sich nicht auf dem lokalen Computer, sondern wird auf einem Remote Computer auf dem Weg des lokalen Computers erfasst.</span><span class="sxs-lookup"><span data-stu-id="d6438-128">The network card is not on the local computer, but is capturing on a remote machine at the bequest of the local computer.</span></span><br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <span data-ttu-id="d6438-129"><dt>**networkinfo- \_ Flags \_ Remote- \_ nal**</dt></span><span class="sxs-lookup"><span data-stu-id="d6438-129"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL**</dt></span></span> </dl>                                | <span data-ttu-id="d6438-130">Veralteten Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="d6438-130">Obsolete; do not use.</span></span><br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <span data-ttu-id="d6438-131"><dt>**networkinfo \_ Flags \_ Remote- \_ nal- \_ Verbindung**</dt></span><span class="sxs-lookup"><span data-stu-id="d6438-131"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d6438-132">Veralteten Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="d6438-132">Obsolete; do not use.</span></span><br/>                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="d6438-133">**Timestampscalefactor**</span><span class="sxs-lookup"><span data-stu-id="d6438-133">**TimestampScaleFactor**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-134">Der Wert 1 gibt z. b. 1/1 MS an, 10 gibt 1/10 MS an, 100 gibt 1/100 MS an usw.</span><span class="sxs-lookup"><span data-stu-id="d6438-134">For example, a value of 1 indicates 1/1 ms, 10 indicates 1/10 ms, 100 indicates 1/100 ms, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-135">**NodeName**</span><span class="sxs-lookup"><span data-stu-id="d6438-135">**NodeName**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-136">Name der Remote Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="d6438-136">Name of remote workstation.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-137">**Pmodesupported**</span><span class="sxs-lookup"><span data-stu-id="d6438-137">**PModeSupported**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-138">Support Indikator für den NIC-P-Modus.</span><span class="sxs-lookup"><span data-stu-id="d6438-138">NIC P-mode support indicator.</span></span>

</dd> <dt>

<span data-ttu-id="d6438-139">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="d6438-139">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="d6438-140">Feld für den Adapter Kommentar.</span><span class="sxs-lookup"><span data-stu-id="d6438-140">Adapter comment field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6438-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6438-141">Requirements</span></span>



| <span data-ttu-id="d6438-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6438-142">Requirement</span></span> | <span data-ttu-id="d6438-143">Wert</span><span class="sxs-lookup"><span data-stu-id="d6438-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d6438-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6438-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d6438-145">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6438-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d6438-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6438-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d6438-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6438-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d6438-148">Header</span><span class="sxs-lookup"><span data-stu-id="d6438-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6438-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6438-149"><dt>Netmon.h</dt></span></span> </dl> |



 

 




