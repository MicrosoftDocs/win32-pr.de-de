---
description: Die providor \_ Info \_ 2-Struktur fügt einen Druckanbieter an die Auftragsliste des Druck Anbieters an.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: PROVIDOR_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350827"
---
# <a name="providor_info_2-structure"></a><span data-ttu-id="6409c-103">Providor \_ Info \_ 2-Struktur</span><span class="sxs-lookup"><span data-stu-id="6409c-103">PROVIDOR\_INFO\_2 structure</span></span>

<span data-ttu-id="6409c-104">Die **providor \_ Info \_ 2** -Struktur fügt einen Druckanbieter an die Auftragsliste des Druck Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="6409c-104">The **PROVIDOR\_INFO\_2** structure appends a print provider to the print provider order list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6409c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6409c-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="6409c-106">Member</span><span class="sxs-lookup"><span data-stu-id="6409c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6409c-107">**Porder**</span><span class="sxs-lookup"><span data-stu-id="6409c-107">**pOrder**</span></span>
</dt> <dd>

<span data-ttu-id="6409c-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Druck Anbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="6409c-108">Pointer to a null-terminated string that specifies the name of the print provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6409c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6409c-109">Remarks</span></span>

<span data-ttu-id="6409c-110">Diese Struktur wird beim Aufrufen von [**addprintprovidor**](addprintprovidor.md), Ebene 2, zum Hinzufügen des angegebenen Druck Anbieters am Ende der Auftragsliste des Druck Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="6409c-110">This structure is used when calling [**AddPrintProvidor**](addprintprovidor.md), level 2, to add the specified print provider to the end of the print provider order list.</span></span> <span data-ttu-id="6409c-111">Der Anbieter wird sofort für das Routing verwendet, wenn der-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6409c-111">The provider is immediately used for routing if the call succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="6409c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6409c-112">Requirements</span></span>



| <span data-ttu-id="6409c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6409c-113">Requirement</span></span> | <span data-ttu-id="6409c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6409c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6409c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6409c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6409c-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6409c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6409c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6409c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6409c-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6409c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6409c-119">Header</span><span class="sxs-lookup"><span data-stu-id="6409c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6409c-120"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6409c-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6409c-121">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="6409c-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6409c-122">**\_ Providor \_ Info \_ 2W** (Unicode) und **\_ providor \_ Info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6409c-122">**\_PROVIDOR\_INFO\_2W** (Unicode) and **\_PROVIDOR\_INFO\_2A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="6409c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6409c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6409c-124">Drucken</span><span class="sxs-lookup"><span data-stu-id="6409c-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6409c-125">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6409c-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="6409c-126">**Addprintprovidor**</span><span class="sxs-lookup"><span data-stu-id="6409c-126">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




