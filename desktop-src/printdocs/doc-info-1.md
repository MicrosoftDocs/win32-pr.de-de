---
description: In der doc \_ Info \_ 1-Struktur wird ein Dokument beschrieben, das gedruckt wird.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: DOC_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215860"
---
# <a name="doc_info_1-structure"></a><span data-ttu-id="d066f-103">DOC \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="d066f-103">DOC\_INFO\_1 structure</span></span>

<span data-ttu-id="d066f-104">In der **doc \_ Info \_ 1** -Struktur wird ein Dokument beschrieben, das gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="d066f-104">The **DOC\_INFO\_1** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d066f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d066f-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a><span data-ttu-id="d066f-106">Member</span><span class="sxs-lookup"><span data-stu-id="d066f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d066f-107">**pdocname**</span><span class="sxs-lookup"><span data-stu-id="d066f-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="d066f-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Dokuments angibt.</span><span class="sxs-lookup"><span data-stu-id="d066f-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="d066f-109">**poutputfile**</span><span class="sxs-lookup"><span data-stu-id="d066f-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="d066f-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen einer Ausgabedatei angibt.</span><span class="sxs-lookup"><span data-stu-id="d066f-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span> <span data-ttu-id="d066f-111">Legen Sie diese Einstellung auf **null** fest, um Sie auf einen Drucker zu drucken.</span><span class="sxs-lookup"><span data-stu-id="d066f-111">To print to a printer, set this to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d066f-112">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="d066f-112">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="d066f-113">Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen des Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d066f-113">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d066f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d066f-114">Requirements</span></span>



| <span data-ttu-id="d066f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d066f-115">Requirement</span></span> | <span data-ttu-id="d066f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d066f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d066f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d066f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d066f-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d066f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d066f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d066f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d066f-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d066f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d066f-121">Header</span><span class="sxs-lookup"><span data-stu-id="d066f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d066f-122"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d066f-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d066f-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d066f-124">**\_ Doc \_ Info \_ 1W** (Unicode) und **\_ doc \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d066f-124">**\_DOC\_INFO\_1W** (Unicode) and **\_DOC\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="d066f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d066f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d066f-126">Drucken</span><span class="sxs-lookup"><span data-stu-id="d066f-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d066f-127">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d066f-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="d066f-128">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="d066f-128">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




