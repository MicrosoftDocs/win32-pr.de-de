---
description: Die PrintProcessor \_ Info \_ 1-Struktur gibt den Namen eines installierten Druck Prozessors an.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: PRINTPROCESSOR_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350802"
---
# <a name="printprocessor_info_1-structure"></a><span data-ttu-id="bded9-103">PrintProcessor \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="bded9-103">PRINTPROCESSOR\_INFO\_1 structure</span></span>

<span data-ttu-id="bded9-104">Die **PrintProcessor \_ Info \_ 1** -Struktur gibt den Namen eines installierten Druck Prozessors an.</span><span class="sxs-lookup"><span data-stu-id="bded9-104">The **PRINTPROCESSOR\_INFO\_1** structure specifies the name of an installed print processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bded9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bded9-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="bded9-106">Member</span><span class="sxs-lookup"><span data-stu-id="bded9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bded9-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="bded9-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="bded9-108">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen eines installierten Druck Prozessors angibt.</span><span class="sxs-lookup"><span data-stu-id="bded9-108">Pointer to a null-terminated string that specifies the name of an installed print processor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bded9-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bded9-109">Requirements</span></span>



| <span data-ttu-id="bded9-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bded9-110">Requirement</span></span> | <span data-ttu-id="bded9-111">Wert</span><span class="sxs-lookup"><span data-stu-id="bded9-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bded9-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bded9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bded9-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bded9-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bded9-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bded9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bded9-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bded9-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bded9-116">Header</span><span class="sxs-lookup"><span data-stu-id="bded9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="bded9-117"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bded9-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bded9-118">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bded9-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bded9-119">**\_ PrintProcessor \_ Info \_ 1W** (Unicode) und **\_ PrintProcessor \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bded9-119">**\_PRINTPROCESSOR\_INFO\_1W** (Unicode) and **\_PRINTPROCESSOR\_INFO\_1A** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bded9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bded9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bded9-121">Drucken</span><span class="sxs-lookup"><span data-stu-id="bded9-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bded9-122">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="bded9-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="bded9-123">**Enumprintprozessoren**</span><span class="sxs-lookup"><span data-stu-id="bded9-123">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

 




