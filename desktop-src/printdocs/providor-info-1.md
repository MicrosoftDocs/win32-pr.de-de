---
description: Die providor \_ Info \_ 1-Struktur identifiziert einen Druckanbieter.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: PROVIDOR_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347488"
---
# <a name="providor_info_1-structure"></a><span data-ttu-id="3800d-103">Providor \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="3800d-103">PROVIDOR\_INFO\_1 structure</span></span>

<span data-ttu-id="3800d-104">Die **providor \_ Info \_ 1** -Struktur identifiziert einen Druckanbieter.</span><span class="sxs-lookup"><span data-stu-id="3800d-104">The **PROVIDOR\_INFO\_1** structure identifies a print provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="3800d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3800d-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="3800d-106">Member</span><span class="sxs-lookup"><span data-stu-id="3800d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3800d-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="3800d-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="3800d-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Druck Anbieters ist.</span><span class="sxs-lookup"><span data-stu-id="3800d-108">Pointer to a null-terminated string that is the name of the print provider.</span></span>

</dd> <dt>

<span data-ttu-id="3800d-109">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="3800d-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="3800d-110">Zeiger auf eine mit NULL endenden Umgebungs Zeichenfolge, die die Umgebung angibt, in der die Anbieter-DLL (Dynamic-Link Library) ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3800d-110">Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.</span></span>

</dd> <dt>

<span data-ttu-id="3800d-111">**pdllname**</span><span class="sxs-lookup"><span data-stu-id="3800d-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="3800d-112">Zeiger auf eine mit NULL endenden Zeichenfolge, die der Name der Anbieter. dll ist.</span><span class="sxs-lookup"><span data-stu-id="3800d-112">Pointer to a null-terminated string that is the name of the provider .dll.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3800d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3800d-113">Requirements</span></span>



| <span data-ttu-id="3800d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3800d-114">Requirement</span></span> | <span data-ttu-id="3800d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3800d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3800d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3800d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3800d-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3800d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3800d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3800d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3800d-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3800d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3800d-120">Header</span><span class="sxs-lookup"><span data-stu-id="3800d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3800d-121"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3800d-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3800d-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3800d-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3800d-123">**\_ Providor \_ Info \_ 1W** (Unicode) und **\_ providor \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3800d-123">**\_PROVIDOR\_INFO\_1W** (Unicode) and **\_PROVIDOR\_INFO\_1A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="3800d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3800d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3800d-125">Drucken</span><span class="sxs-lookup"><span data-stu-id="3800d-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3800d-126">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3800d-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="3800d-127">**Addprintprovidor**</span><span class="sxs-lookup"><span data-stu-id="3800d-127">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




