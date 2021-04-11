---
description: Die \_ IP- \_ Adressstruktur der Reben ist eine IP-Adresse in einem Reben Netzwerk.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: VINES_IP_ADDRESS Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346298"
---
# <a name="vines_ip_address-structure"></a><span data-ttu-id="f2144-103">\_IP- \_ Adressstruktur der Reben</span><span class="sxs-lookup"><span data-stu-id="f2144-103">VINES\_IP\_ADDRESS structure</span></span>

<span data-ttu-id="f2144-104">Die **\_ IP- \_ Adress** Struktur der Reben ist eine IP-Adresse in einem Reben Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f2144-104">The **VINES\_IP\_ADDRESS** structure is an IP address on a Vines network.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2144-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2144-105">Syntax</span></span>


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="f2144-106">Member</span><span class="sxs-lookup"><span data-stu-id="f2144-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2144-107">**"Ntid"**</span><span class="sxs-lookup"><span data-stu-id="f2144-107">**NetID**</span></span>
</dt> <dd>

<span data-ttu-id="f2144-108">Der Bezeichner eines bestimmten Computers in einem bestimmten Subnetz.</span><span class="sxs-lookup"><span data-stu-id="f2144-108">The identifier of a specific machine on a specific subnet.</span></span>

</dd> <dt>

<span data-ttu-id="f2144-109">**SubnetID**</span><span class="sxs-lookup"><span data-stu-id="f2144-109">**SubnetID**</span></span>
</dt> <dd>

<span data-ttu-id="f2144-110">Der Bezeichner eines bestimmten Subnetzes im gesamten Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f2144-110">The identifier of a specific subnet on the whole network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2144-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2144-111">Requirements</span></span>



| <span data-ttu-id="f2144-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2144-112">Requirement</span></span> | <span data-ttu-id="f2144-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f2144-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f2144-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2144-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f2144-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2144-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f2144-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2144-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f2144-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2144-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f2144-118">Header</span><span class="sxs-lookup"><span data-stu-id="f2144-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2144-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2144-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




