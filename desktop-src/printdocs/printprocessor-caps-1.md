---
description: Die PrintProcessor \_ Caps \_ 1-Struktur ist das Format für die Drucker Funktions Informationen, die von der getprinterdata-Funktion in dem Puffer zurückgegeben werden, der von der pData-Variablen angegeben wird.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: PRINTPROCESSOR_CAPS_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364149"
---
# <a name="printprocessor_caps_1-structure"></a><span data-ttu-id="c8ef7-103">PrintProcessor-Ober \_ Grenzen \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="c8ef7-103">PRINTPROCESSOR\_CAPS\_1 structure</span></span>

<span data-ttu-id="c8ef7-104">Die **PrintProcessor \_ Caps \_ 1** -Struktur ist das Format für die Drucker Funktions Informationen, die von der [**getprinterdata**](getprinterdata.md) -Funktion in dem Puffer zurückgegeben werden, der von der *pData* -Variablen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-104">The **PRINTPROCESSOR\_CAPS\_1** structure is the format for the printer capability information that is returned by the [**GetPrinterData**](getprinterdata.md) function in the buffer specified by the *pData* variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ef7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8ef7-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a><span data-ttu-id="c8ef7-106">Member</span><span class="sxs-lookup"><span data-stu-id="c8ef7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8ef7-107">**dwlevel**</span><span class="sxs-lookup"><span data-stu-id="c8ef7-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="c8ef7-108">Die Versionsnummer der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-108">The structure's version number.</span></span> <span data-ttu-id="c8ef7-109">Dieser Wert muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-109">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef7-110">**dwnupoptions**</span><span class="sxs-lookup"><span data-stu-id="c8ef7-110">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="c8ef7-111">Eine Bitmaske, die die verschiedenen Anzahl von Dokument Seiten darstellt, die der Drucker auf einer physischen Seite drucken kann.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-111">A bit mask representing the various numbers of document pages the printer can print on a physical page.</span></span> <span data-ttu-id="c8ef7-112">Das unwichtigste Bit stellt eine Dokument Seite pro Seite dar, das nächste Bit stellt 2 Dokument Seiten pro Seite dar usw.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-112">The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on.</span></span> <span data-ttu-id="c8ef7-113">Beispielsweise gibt 0x0000810b an, dass der Drucker jeweils 1, 2, 4, 9 und 16 Dokument Seiten pro physischer Seite unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-113">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef7-114">**dwpaargeorderflags**</span><span class="sxs-lookup"><span data-stu-id="c8ef7-114">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c8ef7-115">Die Reihenfolge, in der Seiten gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-115">The order in which pages will be printed.</span></span> <span data-ttu-id="c8ef7-116">Bei diesem Wert kann es sich um einen normalen \_ Druck, einen umgekehrten \_ Druck oder einen \_ Drucker Druck handeln.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-116">This value can be NORMAL\_PRINT, REVERSE\_PRINT, or BOOKLET\_PRINT.</span></span>

</dd> <dt>

<span data-ttu-id="c8ef7-117">**dwnumofkopien**</span><span class="sxs-lookup"><span data-stu-id="c8ef7-117">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="c8ef7-118">Die maximale Anzahl von Kopien, die der Drucker verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-118">The maximum number of copies the printer can handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8ef7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8ef7-119">Remarks</span></span>

<span data-ttu-id="c8ef7-120">Werte für alle Strukturmember werden von der Funktion [**getprintprocessorfunctions**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) bereitgestellt, die im Windows-Treiberkit (WDK) dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-120">Values for all structure members are supplied by the [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function, which is documented in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="c8ef7-121">Der Spooler Ruft die [**getprintprocessorfunctions**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) -Funktion eines Druck Prozessors auf, wenn eine Anwendung [**getprinterdata**](getprinterdata.md)aufruft und einen Wertnamen mit dem Format printproccaps \_ *Datentyp* angibt, wobei *Datentyp* der Name eines Eingabe Datentyps ist.</span><span class="sxs-lookup"><span data-stu-id="c8ef7-121">The spooler calls a print processor's [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function when an application calls [**GetPrinterData**](getprinterdata.md), specifying a value name with a format of PrintProcCaps\_*datatype*, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ef7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8ef7-122">Requirements</span></span>



| <span data-ttu-id="c8ef7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8ef7-123">Requirement</span></span> | <span data-ttu-id="c8ef7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c8ef7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ef7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8ef7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ef7-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8ef7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8ef7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8ef7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ef7-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8ef7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8ef7-129">Header</span><span class="sxs-lookup"><span data-stu-id="c8ef7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ef7-130"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8ef7-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ef7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ef7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ef7-132">Drucken</span><span class="sxs-lookup"><span data-stu-id="c8ef7-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c8ef7-133">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c8ef7-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c8ef7-134">**Getprinterdata**</span><span class="sxs-lookup"><span data-stu-id="c8ef7-134">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

