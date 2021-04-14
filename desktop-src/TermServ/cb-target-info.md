---
title: CB_TARGET_INFO Struktur (cbclient. h)
description: Enthält Informationen über den Zielcomputer und die IP-Adressen, an die eingehende Verbindungen umgeleitet werden sollen.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO Struktur Remotedesktopdienste
- PCB_TARGET_INFO Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391688"
---
# <a name="cb_target_info-structure"></a><span data-ttu-id="2df10-105">CB- \_ Ziel \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="2df10-105">CB\_TARGET\_INFO structure</span></span>

<span data-ttu-id="2df10-106">Enthält Informationen über den Zielcomputer und die IP-Adressen, an die eingehende Verbindungen umgeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2df10-106">Contains information about the target computer and IP addresses where incoming connections should be redirected.</span></span> <span data-ttu-id="2df10-107">Diese Struktur wird mit der [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="2df10-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df10-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df10-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="2df10-109">Member</span><span class="sxs-lookup"><span data-stu-id="2df10-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2df10-110">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="2df10-110">**ServerName**</span></span>
</dt> <dd>

<span data-ttu-id="2df10-111">Stellt den voll qualifizierten Domänen Namen des Zielservers dar.</span><span class="sxs-lookup"><span data-stu-id="2df10-111">Represents the fully qualified domain name of the target server.</span></span> <span data-ttu-id="2df10-112">Bei einem Remotedesktop Virtualisierungsszenario (RDV) ist dieser Member **null**.</span><span class="sxs-lookup"><span data-stu-id="2df10-112">For a Remote Desktop virtualization (RDV) scenario, this member is **NULL**.</span></span> <span data-ttu-id="2df10-113">Bei einem Remotedesktop-Sitzungs Host Szenario (RDSH) enthält dieser Member den Namen des Servers, auf den die eingehende Verbindung umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2df10-113">For a Remote Desktop session host (RDSH) scenario, this member contains the server name where the incoming connection is redirected.</span></span>

</dd> <dt>

<span data-ttu-id="2df10-114">**Addresscount**</span><span class="sxs-lookup"><span data-stu-id="2df10-114">**AddressCount**</span></span>
</dt> <dd>

<span data-ttu-id="2df10-115">Die Anzahl der gültigen Einträge im **Adress** Array.</span><span class="sxs-lookup"><span data-stu-id="2df10-115">The number of valid entries in the **Addresses** array.</span></span>

</dd> <dt>

<span data-ttu-id="2df10-116">**Adresses**</span><span class="sxs-lookup"><span data-stu-id="2df10-116">**Addresses**</span></span>
</dt> <dd>

<span data-ttu-id="2df10-117">Ein Array von Zeichen folgen, die die IP-Adressen enthalten, an die die eingehenden Verbindungen umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="2df10-117">An array of strings that contain the IP addresses where the incoming connections are redirected.</span></span> <span data-ttu-id="2df10-118">Die Anzahl der gültigen Elemente in diesem Array wird im **addresscount** -Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="2df10-118">The number of valid elements in this array is specified in the **AddressCount** member.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2df10-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df10-119">Requirements</span></span>



| <span data-ttu-id="2df10-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2df10-120">Requirement</span></span> | <span data-ttu-id="2df10-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2df10-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2df10-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2df10-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2df10-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2df10-123">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="2df10-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2df10-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2df10-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2df10-125">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="2df10-126">Header</span><span class="sxs-lookup"><span data-stu-id="2df10-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2df10-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2df10-127"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2df10-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2df10-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df10-129">**Iconnectionbrokerclient:: gettargetinfo**</span><span class="sxs-lookup"><span data-stu-id="2df10-129">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





