---
description: Enthält eine Portnummer, die für IP-oder IPX-Protokolle verwendet wird.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: GENERIC_PORT Union (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958723"
---
# <a name="generic_port-union"></a><span data-ttu-id="00d48-103">Generische \_ Port Union</span><span class="sxs-lookup"><span data-stu-id="00d48-103">GENERIC\_PORT union</span></span>

<span data-ttu-id="00d48-104">Die **generische \_ Port** Struktur enthält eine Portnummer, die für IP-oder IPX-Protokolle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00d48-104">The **GENERIC\_PORT** structure contains a port number used for IP or IPX protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d48-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00d48-105">Syntax</span></span>


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a><span data-ttu-id="00d48-106">Member</span><span class="sxs-lookup"><span data-stu-id="00d48-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="00d48-107">**IPPort**</span><span class="sxs-lookup"><span data-stu-id="00d48-107">**IPPort**</span></span>
</dt> <dd>

<span data-ttu-id="00d48-108">Die IP-Portnummer ist ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="00d48-108">IP port number filled in.</span></span>

</dd> <dt>

<span data-ttu-id="00d48-109">**Byteswappedipxport**</span><span class="sxs-lookup"><span data-stu-id="00d48-109">**ByteSwappedIPXPort**</span></span>
</dt> <dd>

<span data-ttu-id="00d48-110">Die IPX-Portnummer ist ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="00d48-110">IPX port number filled in.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00d48-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00d48-111">Requirements</span></span>



| <span data-ttu-id="00d48-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00d48-112">Requirement</span></span> | <span data-ttu-id="00d48-113">Wert</span><span class="sxs-lookup"><span data-stu-id="00d48-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00d48-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00d48-114">Minimum supported client</span></span><br/> | <span data-ttu-id="00d48-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00d48-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00d48-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00d48-116">Minimum supported server</span></span><br/> | <span data-ttu-id="00d48-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00d48-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00d48-118">Header</span><span class="sxs-lookup"><span data-stu-id="00d48-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d48-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="00d48-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




