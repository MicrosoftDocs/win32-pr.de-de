---
description: Die IPX- \_ Adressstruktur stellt eine Adresse auf IPX-Protokollebene bereit.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: IPX_ADDRESS Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525868"
---
# <a name="ipx_address-structure"></a><span data-ttu-id="a45f8-103">IPX- \_ Adressstruktur</span><span class="sxs-lookup"><span data-stu-id="a45f8-103">IPX\_ADDRESS structure</span></span>

<span data-ttu-id="a45f8-104">Die **IPX- \_ Adress** Struktur stellt eine Adresse auf IPX-Protokollebene bereit.</span><span class="sxs-lookup"><span data-stu-id="a45f8-104">The **IPX\_ADDRESS** structure provides an address at the IPX protocol level.</span></span>

## <a name="syntax"></a><span data-ttu-id="a45f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a45f8-105">Syntax</span></span>


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="a45f8-106">Member</span><span class="sxs-lookup"><span data-stu-id="a45f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a45f8-107">**Subnetz**</span><span class="sxs-lookup"><span data-stu-id="a45f8-107">**Subnet**</span></span>
</dt> <dd>

<span data-ttu-id="a45f8-108">Netzwerksubnetzbezeichner.</span><span class="sxs-lookup"><span data-stu-id="a45f8-108">Network subnet identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a45f8-109">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="a45f8-109">**Address**</span></span>
</dt> <dd>

<span data-ttu-id="a45f8-110">Subnetz-NIC-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a45f8-110">Subnet NIC identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a45f8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a45f8-111">Requirements</span></span>



| <span data-ttu-id="a45f8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a45f8-112">Requirement</span></span> | <span data-ttu-id="a45f8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a45f8-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a45f8-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a45f8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a45f8-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a45f8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a45f8-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a45f8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a45f8-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a45f8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a45f8-118">Header</span><span class="sxs-lookup"><span data-stu-id="a45f8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a45f8-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45f8-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




