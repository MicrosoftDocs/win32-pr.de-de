---
description: Die Struktur von Datatypes \_ Info \_ 1 enthält Informationen zum Datentyp, der zum Aufzeichnen eines Druckauftrags verwendet wird.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: DATATYPES_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215981"
---
# <a name="datatypes_info_1-structure"></a><span data-ttu-id="d3ee1-103">Datatypes \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="d3ee1-103">DATATYPES\_INFO\_1 structure</span></span>

<span data-ttu-id="d3ee1-104">Die Struktur von **Datatypes \_ Info \_ 1** enthält Informationen zum Datentyp, der zum Aufzeichnen eines Druckauftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-104">The **DATATYPES\_INFO\_1** structure contains information about the data type used to record a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ee1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3ee1-105">Syntax</span></span>


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a><span data-ttu-id="d3ee1-106">Member</span><span class="sxs-lookup"><span data-stu-id="d3ee1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3ee1-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="d3ee1-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="d3ee1-108">Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen eines Druckauftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-108">Pointer to a null-terminated string that identifies the data type used to record a print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3ee1-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3ee1-109">Requirements</span></span>



| <span data-ttu-id="d3ee1-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3ee1-110">Requirement</span></span> | <span data-ttu-id="d3ee1-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d3ee1-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ee1-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3ee1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ee1-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3ee1-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d3ee1-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3ee1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ee1-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3ee1-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d3ee1-116">Header</span><span class="sxs-lookup"><span data-stu-id="d3ee1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ee1-117"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3ee1-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d3ee1-118">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d3ee1-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d3ee1-119">**\_ Datatypes \_ Info \_ 1W** (Unicode) und **\_ Datatypes \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d3ee1-119">**\_DATATYPES\_INFO\_1W** (Unicode) and **\_DATATYPES\_INFO\_1A** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d3ee1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3ee1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ee1-121">Drucken</span><span class="sxs-lookup"><span data-stu-id="d3ee1-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d3ee1-122">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d3ee1-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="d3ee1-123">**Enumprintprocessordatatypes**</span><span class="sxs-lookup"><span data-stu-id="d3ee1-123">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




