---
description: In der doc \_ Info \_ 3-Struktur wird ein Dokument beschrieben, das gedruckt wird.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: DOC_INFO_3 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347557"
---
# <a name="doc_info_3-structure"></a><span data-ttu-id="9579a-103">DOC \_ Info \_ 3-Struktur</span><span class="sxs-lookup"><span data-stu-id="9579a-103">DOC\_INFO\_3 structure</span></span>

<span data-ttu-id="9579a-104">In der **doc \_ Info \_ 3** -Struktur wird ein Dokument beschrieben, das gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="9579a-104">The **DOC\_INFO\_3** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9579a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9579a-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a><span data-ttu-id="9579a-106">Member</span><span class="sxs-lookup"><span data-stu-id="9579a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9579a-107">**pdocname**</span><span class="sxs-lookup"><span data-stu-id="9579a-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="9579a-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Dokuments angibt.</span><span class="sxs-lookup"><span data-stu-id="9579a-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="9579a-109">**poutputfile**</span><span class="sxs-lookup"><span data-stu-id="9579a-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="9579a-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen einer Ausgabedatei angibt.</span><span class="sxs-lookup"><span data-stu-id="9579a-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="9579a-111">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="9579a-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="9579a-112">Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen des Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9579a-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="9579a-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="9579a-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9579a-114">Fahren.</span><span class="sxs-lookup"><span data-stu-id="9579a-114">Flags.</span></span> <span data-ttu-id="9579a-115">Derzeit kann der Wert **null** oder der folgende sein.</span><span class="sxs-lookup"><span data-stu-id="9579a-115">Currently, it can be **NULL** or the following.</span></span>



| <span data-ttu-id="9579a-116">Flag</span><span class="sxs-lookup"><span data-stu-id="9579a-116">Flag</span></span>                 | <span data-ttu-id="9579a-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9579a-117">Meaning</span></span>                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9579a-118">DI \_ memorymap \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="9579a-118">DI\_MEMORYMAP\_WRITE</span></span> | <span data-ttu-id="9579a-119">Bewirkt, dass [**StartDocPrinter**](startdocprinter.md) [**AddJob**](addjob.md) und [**schedulejob**](schedulejob.md) nicht für das lokale Drucken verwendet.</span><span class="sxs-lookup"><span data-stu-id="9579a-119">Causes [**StartDocPrinter**](startdocprinter.md) to not use [**AddJob**](addjob.md) and [**ScheduleJob**](schedulejob.md) for local printing.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9579a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9579a-120">Remarks</span></span>

<span data-ttu-id="9579a-121">Die \_ Schreib Einstellung di memorymap \_ in **doc \_ Info \_ 3** ist eine Optimierung.</span><span class="sxs-lookup"><span data-stu-id="9579a-121">The DI\_MEMORYMAP\_WRITE setting in **DOC\_INFO\_3** is an optimization.</span></span> <span data-ttu-id="9579a-122">Dadurch kann GDI Spooldateien in der Anwendung zuordnen und die Aufzeichnung beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="9579a-122">This allows GDI to map spool files in the application and speed up the recording.</span></span>

## <a name="requirements"></a><span data-ttu-id="9579a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9579a-123">Requirements</span></span>



| <span data-ttu-id="9579a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9579a-124">Requirement</span></span> | <span data-ttu-id="9579a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9579a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9579a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9579a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9579a-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9579a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9579a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9579a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9579a-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9579a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9579a-130">Header</span><span class="sxs-lookup"><span data-stu-id="9579a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9579a-131"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9579a-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9579a-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9579a-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9579a-133">**\_ Doc \_ Info \_ 3W** (Unicode) und **\_ doc \_ Info \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9579a-133">**\_DOC\_INFO\_3W** (Unicode) and **\_DOC\_INFO\_3A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="9579a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9579a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9579a-135">Drucken</span><span class="sxs-lookup"><span data-stu-id="9579a-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9579a-136">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9579a-136">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9579a-137">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="9579a-137">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="9579a-138">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="9579a-138">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="9579a-139">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="9579a-139">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




