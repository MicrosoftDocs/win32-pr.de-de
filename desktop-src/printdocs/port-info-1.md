---
description: Die \_ Struktur Port Info \_ 1 identifiziert einen unterstützten Druckerport.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: PORT_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350210"
---
# <a name="port_info_1-structure"></a><span data-ttu-id="938dc-103">Port \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="938dc-103">PORT\_INFO\_1 structure</span></span>

<span data-ttu-id="938dc-104">Die Struktur **Port \_ Info \_ 1** identifiziert einen unterstützten Druckerport.</span><span class="sxs-lookup"><span data-stu-id="938dc-104">The **PORT\_INFO\_1** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="938dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="938dc-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a><span data-ttu-id="938dc-106">Member</span><span class="sxs-lookup"><span data-stu-id="938dc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="938dc-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="938dc-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="938dc-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen unterstützten Druckerport identifiziert (z. b. "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="938dc-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="938dc-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="938dc-109">Requirements</span></span>



| <span data-ttu-id="938dc-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="938dc-110">Requirement</span></span> | <span data-ttu-id="938dc-111">Wert</span><span class="sxs-lookup"><span data-stu-id="938dc-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="938dc-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="938dc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="938dc-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="938dc-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="938dc-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="938dc-114">Minimum supported server</span></span><br/> | <span data-ttu-id="938dc-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="938dc-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="938dc-116">Header</span><span class="sxs-lookup"><span data-stu-id="938dc-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="938dc-117"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="938dc-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="938dc-118">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="938dc-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="938dc-119">**\_ Port \_ Info \_ 1W** (Unicode) und **\_ Port \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="938dc-119">**\_PORT\_INFO\_1W** (Unicode) and **\_PORT\_INFO\_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="938dc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="938dc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="938dc-121">Drucken</span><span class="sxs-lookup"><span data-stu-id="938dc-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="938dc-122">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="938dc-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="938dc-123">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="938dc-123">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




