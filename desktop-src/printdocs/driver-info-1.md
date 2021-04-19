---
description: Die Struktur der Treiber \_ Informationen \_ 1 identifiziert einen Druckertreiber.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: DRIVER_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360790"
---
# <a name="driver_info_1-structure"></a><span data-ttu-id="df0b4-103">Struktur der Treiber \_ Info \_ 1</span><span class="sxs-lookup"><span data-stu-id="df0b4-103">DRIVER\_INFO\_1 structure</span></span>

<span data-ttu-id="df0b4-104">Die Struktur der **Treiber \_ Informationen \_ 1** identifiziert einen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="df0b4-104">The **DRIVER\_INFO\_1** structure identifies a printer driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df0b4-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="df0b4-106">Member</span><span class="sxs-lookup"><span data-stu-id="df0b4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="df0b4-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="df0b4-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="df0b4-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen eines Druckertreibers angibt.</span><span class="sxs-lookup"><span data-stu-id="df0b4-108">Pointer to a null-terminated string that specifies the name of a printer driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df0b4-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df0b4-109">Requirements</span></span>



| <span data-ttu-id="df0b4-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df0b4-110">Requirement</span></span> | <span data-ttu-id="df0b4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="df0b4-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0b4-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df0b4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="df0b4-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df0b4-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df0b4-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df0b4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="df0b4-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df0b4-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df0b4-116">Header</span><span class="sxs-lookup"><span data-stu-id="df0b4-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="df0b4-117"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df0b4-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="df0b4-118">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="df0b4-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="df0b4-119">**\_ Treiber \_ Informationen \_ 1W** (Unicode) und **\_ Treiber \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="df0b4-119">**\_DRIVER\_INFO\_1W** (Unicode) and **\_DRIVER\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="df0b4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df0b4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0b4-121">Drucken</span><span class="sxs-lookup"><span data-stu-id="df0b4-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="df0b4-122">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="df0b4-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="df0b4-123">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="df0b4-123">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

 




