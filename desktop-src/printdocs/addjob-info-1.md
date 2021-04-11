---
description: Die Struktur AddJob \_ Info \_ 1 identifiziert einen Druckauftrag sowie das Verzeichnis und die Datei, in der eine Anwendung den Auftrag speichern kann.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: ADDJOB_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218228"
---
# <a name="addjob_info_1-structure"></a><span data-ttu-id="badf4-103">AddJob \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="badf4-103">ADDJOB\_INFO\_1 structure</span></span>

<span data-ttu-id="badf4-104">Die Struktur **AddJob \_ Info \_ 1** identifiziert einen Druckauftrag sowie das Verzeichnis und die Datei, in der eine Anwendung den Auftrag speichern kann.</span><span class="sxs-lookup"><span data-stu-id="badf4-104">The **ADDJOB\_INFO\_1** structure identifies a print job as well as the directory and file in which an application can store that job.</span></span>

## <a name="syntax"></a><span data-ttu-id="badf4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="badf4-105">Syntax</span></span>


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="badf4-106">Member</span><span class="sxs-lookup"><span data-stu-id="badf4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="badf4-107">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="badf4-107">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="badf4-108">Zeiger auf eine auf NULL endende Zeichenfolge, die den Pfad und den Dateinamen enthält, die die Anwendung zum Speichern des Druckauftrags verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="badf4-108">Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.</span></span>

</dd> <dt>

<span data-ttu-id="badf4-109">**JobId**</span><span class="sxs-lookup"><span data-stu-id="badf4-109">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="badf4-110">Ein Handle für den Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="badf4-110">A handle to the print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="badf4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="badf4-111">Requirements</span></span>



| <span data-ttu-id="badf4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="badf4-112">Requirement</span></span> | <span data-ttu-id="badf4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="badf4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="badf4-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="badf4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="badf4-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="badf4-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="badf4-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="badf4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="badf4-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="badf4-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="badf4-118">Header</span><span class="sxs-lookup"><span data-stu-id="badf4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="badf4-119"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="badf4-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="badf4-120">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="badf4-120">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="badf4-121">**\_ AddJob \_ Info \_ 1W** (Unicode) und **\_ AddJob \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="badf4-121">**\_ADDJOB\_INFO\_1W** (Unicode) and **\_ADDJOB\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="badf4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="badf4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badf4-123">Drucken</span><span class="sxs-lookup"><span data-stu-id="badf4-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="badf4-124">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="badf4-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="badf4-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="badf4-125">**AddJob**</span></span>](addjob.md)
</dt> </dl>

 

 




