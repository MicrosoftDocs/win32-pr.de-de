---
description: In der doc \_ Info \_ 2-Struktur wird ein Dokument beschrieben, das gedruckt wird.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: DOC_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364150"
---
# <a name="doc_info_2-structure"></a><span data-ttu-id="415fa-103">DOC \_ Info \_ 2-Struktur</span><span class="sxs-lookup"><span data-stu-id="415fa-103">DOC\_INFO\_2 structure</span></span>

<span data-ttu-id="415fa-104">In der **doc \_ Info \_ 2** -Struktur wird ein Dokument beschrieben, das gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="415fa-104">The **DOC\_INFO\_2** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="415fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="415fa-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a><span data-ttu-id="415fa-106">Member</span><span class="sxs-lookup"><span data-stu-id="415fa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="415fa-107">**pdocname**</span><span class="sxs-lookup"><span data-stu-id="415fa-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="415fa-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Dokuments angibt.</span><span class="sxs-lookup"><span data-stu-id="415fa-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="415fa-109">**poutputfile**</span><span class="sxs-lookup"><span data-stu-id="415fa-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="415fa-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen einer Ausgabedatei angibt.</span><span class="sxs-lookup"><span data-stu-id="415fa-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="415fa-111">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="415fa-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="415fa-112">Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp identifiziert, der zum Aufzeichnen des Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="415fa-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="415fa-113">**dwmode**</span><span class="sxs-lookup"><span data-stu-id="415fa-113">**dwMode**</span></span>
</dt> <dd>

<span data-ttu-id="415fa-114">Informiert den Druck Spooler über die Art der Daten, die befolgt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="415fa-114">Informs the print spooler of the nature of the data to follow.</span></span> <span data-ttu-id="415fa-115">Wenn dieser Wert 0 (null) ist, behandelt der Druck Spooler die Daten, die durch nachfolgende Aufrufe an den [**Schreib Drucker**](writeprinter.md) als normaler Druckauftrag gesendet werden (unabhängig davon, ob er gespooltet ist, hängt von der Drucker Eigenschaft ab).</span><span class="sxs-lookup"><span data-stu-id="415fa-115">If this value is zero, the print spooler treats the data sent by subsequent calls to [**WritePrinter**](writeprinter.md) as a normal print job (whether or not it is spooled depends on the printer property).</span></span> <span data-ttu-id="415fa-116">Wenn dieser Wert di- \_ Channel ist, wird nur ein Kommunikationskanal geöffnet.</span><span class="sxs-lookup"><span data-stu-id="415fa-116">If this value is DI\_CHANNEL, only a communications channel is opened.</span></span> <span data-ttu-id="415fa-117">In diesem Fall werden die an nachfolgende Aufrufe von " **Write Printer** " übergebenen Daten an den Drucker gesendet, oder bei nachfolgenden Aufrufen von "read [**Printer**](readprinter.md) " werden Daten vom Drucker abgerufen.</span><span class="sxs-lookup"><span data-stu-id="415fa-117">In this case, the data passed into subsequent calls to **WritePrinter** is sent to the printer or subsequent calls to [**ReadPrinter**](readprinter.md) retrieve data from the printer.</span></span> <span data-ttu-id="415fa-118">Dieser Modus bleibt wirksam, bis [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="415fa-118">This mode remains effective until [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) is called.</span></span>

</dd> <dt>

<span data-ttu-id="415fa-119">**JobId**</span><span class="sxs-lookup"><span data-stu-id="415fa-119">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="415fa-120">Für die interne Verwendung reserviert. muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="415fa-120">Reserved for internal use; should be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="415fa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="415fa-121">Requirements</span></span>



| <span data-ttu-id="415fa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="415fa-122">Requirement</span></span> | <span data-ttu-id="415fa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="415fa-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415fa-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="415fa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="415fa-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="415fa-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="415fa-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="415fa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="415fa-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="415fa-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="415fa-128">Header</span><span class="sxs-lookup"><span data-stu-id="415fa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="415fa-129"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="415fa-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="415fa-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="415fa-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="415fa-131">**\_ Doc \_ Info \_ 2W** (Unicode) und **\_ doc \_ Info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="415fa-131">**\_DOC\_INFO\_2W** (Unicode) and **\_DOC\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="415fa-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="415fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415fa-133">Drucken</span><span class="sxs-lookup"><span data-stu-id="415fa-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="415fa-134">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="415fa-134">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="415fa-135">**EndDoc**</span><span class="sxs-lookup"><span data-stu-id="415fa-135">**EndDoc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[<span data-ttu-id="415fa-136">**Lesen von Druckern**</span><span class="sxs-lookup"><span data-stu-id="415fa-136">**ReadPrinter**</span></span>](readprinter.md)
</dt> <dt>

[<span data-ttu-id="415fa-137">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="415fa-137">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="415fa-138">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="415fa-138">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




