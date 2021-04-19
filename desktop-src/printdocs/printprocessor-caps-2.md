---
description: Stellt Drucker Funktions Informationen dar.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: PRINTPROCESSOR_CAPS_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364120"
---
# <a name="printprocessor_caps_2-structure"></a><span data-ttu-id="7b7f5-103">PrintProcessor \_ Caps \_ 2-Struktur</span><span class="sxs-lookup"><span data-stu-id="7b7f5-103">PRINTPROCESSOR\_CAPS\_2 structure</span></span>

<span data-ttu-id="7b7f5-104">Stellt Drucker Funktions Informationen dar.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-104">Represents printer capability information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b7f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b7f5-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a><span data-ttu-id="7b7f5-106">Member</span><span class="sxs-lookup"><span data-stu-id="7b7f5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b7f5-107">**dwlevel**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-108">Ein-Wert, der die Versionsnummer der-Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-108">A value that indicates the structure's version number.</span></span>

</dd> <dt>

<span data-ttu-id="7b7f5-109">**dwnupoptions**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-109">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-110">Eine Bitmaske, die die verschiedenen Anzahl von Dokument Seiten darstellt, die der Drucker auf einer einzelnen Seite eines physischen Blatts drucken kann.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-110">A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet.</span></span> <span data-ttu-id="7b7f5-111">Das unwichtigste Bit stellt eine Dokument Seite pro Seite dar, das nächste Bit stellt 2 Dokument Seiten pro Seite dar usw.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-111">The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on.</span></span> <span data-ttu-id="7b7f5-112">Beispielsweise gibt 0x0000810b an, dass der Drucker jeweils 1, 2, 4, 9 und 16 Dokument Seiten pro physischer Seite unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-112">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.</span></span>

</dd> <dt>

<span data-ttu-id="7b7f5-113">**dwpaargeorderflags**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-113">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-114">Ein Flagwert, der die Reihenfolge angibt, in der Seiten gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-114">A flag value that indicates the order in which pages will be printed.</span></span> <span data-ttu-id="7b7f5-115">Dabei kann es sich um einen **normalen \_ Druck**, einen **umgekehrten \_ Druck** **oder einen Druck Druck \_** handeln.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-115">It can be **NORMAL\_PRINT**, **REVERSE\_PRINT**, or **BOOKLET\_PRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="7b7f5-116">**dwnumofkopien**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-116">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-117">Die maximale Anzahl von Kopien, die der Drucker verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-117">The maximum number of copies the printer can handle.</span></span>

</dd> <dt>

<span data-ttu-id="7b7f5-118">**dwnupdirectioncaps**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-118">**dwNupDirectionCaps**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-119">Die verfügbaren Muster, wenn mehrere Dokument Seiten auf derselben Seite eines Papier Blatts gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-119">The available patterns when multiple document pages are printed on the same side of a sheet of paper.</span></span> <span data-ttu-id="7b7f5-120">Folgende Flags sind möglich:</span><span class="sxs-lookup"><span data-stu-id="7b7f5-120">The possible flags are the following:</span></span>



| <span data-ttu-id="7b7f5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7b7f5-121">Value</span></span>                     | <span data-ttu-id="7b7f5-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7b7f5-122">Meaning</span></span>                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7f5-123">ppcaps \_ direkt \_ \_ nach unten</span><span class="sxs-lookup"><span data-stu-id="7b7f5-123">PPCAPS\_RIGHT\_THEN\_DOWN</span></span> | <span data-ttu-id="7b7f5-124">Die Seiten werden in Zeilen von rechts nach links angezeigt, und jede nachfolgende Zeile unter dem Vorgänger.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-124">Pages appear in rows from right to left, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="7b7f5-125">ppcaps \_ nach \_ \_ Rechts</span><span class="sxs-lookup"><span data-stu-id="7b7f5-125">PPCAPS\_DOWN\_THEN\_RIGHT</span></span> | <span data-ttu-id="7b7f5-126">Seiten werden in Spalten von oben nach unten angezeigt, wobei jede nachfolgende Spalte rechts neben dem Vorgänger angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-126">Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</span></span> |
| <span data-ttu-id="7b7f5-127">ppcaps \_ Links \_ \_ unten</span><span class="sxs-lookup"><span data-stu-id="7b7f5-127">PPCAPS\_LEFT\_THEN\_DOWN</span></span>  | <span data-ttu-id="7b7f5-128">Die Seiten werden in Zeilen von links nach rechts angezeigt, und jede nachfolgende Zeile unter dem Vorgänger.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-128">Pages appear in rows from left to right, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="7b7f5-129">ppcaps \_ nach \_ \_ Links</span><span class="sxs-lookup"><span data-stu-id="7b7f5-129">PPCAPS\_DOWN\_THEN\_LEFT</span></span>  | <span data-ttu-id="7b7f5-130">Seiten werden in Spalten von oben nach unten angezeigt, wobei jede nachfolgende Spalte links vom Vorgänger angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-130">Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="7b7f5-131">**dwnupbordercaps**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-131">**dwNupBorderCaps**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-132">Kann nur ein ppcaps-Rahmen \_ \_ Druck sein, was bedeutet, dass beim Drucken mehrerer Dokument Seiten auf einer einzelnen Seite eines physischen Blatts der Drucker informiert werden kann, ob ein Rahmen um den Druckbereich der einzelnen Dokument Seiten gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-132">Can be only PPCAPS\_BORDER\_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.</span></span>

</dd> <dt>

<span data-ttu-id="7b7f5-133">**dwbooklethandlingcaps**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-133">**dwBookletHandlingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-134">Es kann nur ein ppcaps-Formatierungs \_ \_ Rand angegeben werden, der angibt, dass der Drucker den Schrift Schnitt drucken kann</span><span class="sxs-lookup"><span data-stu-id="7b7f5-134">Can only be PPCAPS\_BOOKLET\_EDGE, indicating that the printer can print booklet style.</span></span>

<span data-ttu-id="7b7f5-135"></dd> <dt>**dwduplexhandlingcaps**</dt> </span><span class="sxs-lookup"><span data-stu-id="7b7f5-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span></span><dd> 

| <span data-ttu-id="7b7f5-136">Wert</span><span class="sxs-lookup"><span data-stu-id="7b7f5-136">Value</span></span>                                         | <span data-ttu-id="7b7f5-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7b7f5-137">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7f5-138">ppcaps \_ umgekehrter \_ Seiten \_ für \_ Reverse- \_ Duplex</span><span class="sxs-lookup"><span data-stu-id="7b7f5-138">PPCAPS\_REVERSE\_PAGES\_FOR\_REVERSE\_DUPLEX</span></span>  | <span data-ttu-id="7b7f5-139">Beim Drucken in umgekehrter Reihenfolge und Duplexing kann der Prozessor die Reihenfolge der einzelnen Seiten Paare austauschen, sodass Sie nicht in der Reihenfolge 4, 3, 2, 1 gedruckt werden, sondern in der Reihenfolge 3, 4, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-139">When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</span></span>                                                                                                       |
| <span data-ttu-id="7b7f5-140">ppcaps \_ \_ senden keine \_ zusätzlichen \_ Seiten \_ für \_ Duplex</span><span class="sxs-lookup"><span data-stu-id="7b7f5-140">PPCAPS\_DONT\_SEND\_EXTRA\_PAGES\_FOR\_DUPLEX</span></span> | <span data-ttu-id="7b7f5-141">Beim Duplexing kann dem Druck Prozessor mitgeteilt werden, dass keine zusätzliche Seite gesendet wird, wenn eine ungerade Anzahl von Dokument Seiten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-141">When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages.</span></span> <span data-ttu-id="7b7f5-142">Der Prozessor berücksichtigt den Wert so gut wie möglich. in Fällen, in denen das verhindern einer zusätzlichen leeren Seite zu einer unsachgemäßen Ausgabe führen würde, werden die zusätzlichen Seiten möglicherweise dennoch gesendet.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-142">The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7b7f5-143">**dwscalingcaps**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-143">**dwScalingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="7b7f5-144">Kann nur eine quadratische Skalierung mit ppcaps sein \_ \_ , was darauf hinweist, dass der Drucker das Seitenbild skalieren kann.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-144">Can only be PPCAPS\_SQUARE\_SCALING, indicating that the printer can scale the page image.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b7f5-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b7f5-145">Remarks</span></span>

<span data-ttu-id="7b7f5-146">Werte für alle Strukturmember werden von der Funktion **getprintprocessorfunctions** bereitgestellt, die im Windows-Treiberkit dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-146">Values for all structure members are supplied by the **GetPrintProcessorCapabilities** function which is documented in the Windows Driver Kit.</span></span>

<span data-ttu-id="7b7f5-147">Wenn eine Anwendung [**getprinterdata**](getprinterdata.md)aufruft, ruft der Spooler die **getprintprocessorfunctions** -Funktion eines Druck Prozessors auf und gibt einen Wertnamen an, der das Format **printproccaps \_**_Datentyp_ hat, wobei *Datentyp* der Name eines Eingabe Datentyps ist.</span><span class="sxs-lookup"><span data-stu-id="7b7f5-147">When an application calls [**GetPrinterData**](getprinterdata.md), the spooler calls a print processor's **GetPrintProcessorCapabilities** function and specifies a value name that has a format of **PrintProcCaps\_**_datatype_, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b7f5-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b7f5-148">Requirements</span></span>



| <span data-ttu-id="7b7f5-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b7f5-149">Requirement</span></span> | <span data-ttu-id="7b7f5-150">Wert</span><span class="sxs-lookup"><span data-stu-id="7b7f5-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7f5-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b7f5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7b7f5-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b7f5-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7b7f5-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b7f5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7b7f5-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b7f5-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7b7f5-155">Header</span><span class="sxs-lookup"><span data-stu-id="7b7f5-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b7f5-156"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b7f5-156"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b7f5-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b7f5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b7f5-158">Drucken</span><span class="sxs-lookup"><span data-stu-id="7b7f5-158">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7b7f5-159">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7b7f5-159">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7b7f5-160">**Getprinterdata**</span><span class="sxs-lookup"><span data-stu-id="7b7f5-160">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

 




