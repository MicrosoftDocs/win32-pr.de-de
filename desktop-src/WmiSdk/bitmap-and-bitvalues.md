---
description: Eine ganze Zahl, die mit der Bitmap-und BitValue-Qualifizierer mit einer Eigenschaft verknüpft ist.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Bitmap-und BitValue-Qualifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358820"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a><span data-ttu-id="1eaa9-103">Bitmap-und BitValue-Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="1eaa9-103">BitMap and BitValue Qualifiers</span></span>

<span data-ttu-id="1eaa9-104">Eine Bitmap ist eine Ganzzahl, die mit einer Eigenschaft verknüpft ist, die die **Bitmap** -und **BitValue** -Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="1eaa9-104">A bitmap is an integer linked to a property with the **BitMap** and **BitValue** qualifiers.</span></span> <span data-ttu-id="1eaa9-105">Jedes Bit des Eigenschafts Werts fungiert als Index in das Array von Werten in der **BitValue** -Liste.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-105">Each bit of the property value acts as an index into the array of values in the **BitValue** list.</span></span> <span data-ttu-id="1eaa9-106">Da mehrere Bits im Eigenschafts Wert gleichzeitig "on" sein können, kann ein einzelner Eigenschafts Wert verwendet werden, um mehrere gleichzeitige Werte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-106">Because multiple bits in the property value can be "on" at the same time, it is possible to use a single property value to indicate multiple concurrent values.</span></span>

<span data-ttu-id="1eaa9-107">Beispielsweise wird mit dem folgenden MOF-Codebeispiel die **filetype** -Eigenschaft so eingerichtet, dass Sie über die Qualifizierer **Bitmap** und **BitValues** verfügt.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-107">For example, the following MOF code example establishes the **FileType** property as having the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="1eaa9-108">Außerdem wird festgelegt, dass das niedrig wertige Bit (Bit 0) dem Wert "Read only" entspricht.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-108">It further establishes that the low-order bit (bit 0) corresponds to the value "Read Only".</span></span> <span data-ttu-id="1eaa9-109">Das nächste Bit (Bit 1) entspricht "Hidden" usw.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-109">The next bit (bit 1) corresponds to "Hidden", and so on.</span></span> <span data-ttu-id="1eaa9-110">(Nicht alle Bits müssen von Bedeutung sein.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-110">(Not all bits must be significant.</span></span> <span data-ttu-id="1eaa9-111">In diesem 8-Bit-System haben die zwei hohen Bestell Bits (6 und 7) keine Bedeutung.)</span><span class="sxs-lookup"><span data-stu-id="1eaa9-111">In this eight-bit system, the two high-order bits, 6 and 7, have no significance.)</span></span>

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

<span data-ttu-id="1eaa9-112">Wenn die **filetype** -Eigenschaft den Wert 7 (Bits 0000 0111) meldet, ist die Datei "Read only", "System" und "Hidden".</span><span class="sxs-lookup"><span data-stu-id="1eaa9-112">If the **FileType** property reports the value 7 (bits 0000 0111), the file is "Read Only", "System", and "Hidden".</span></span> <span data-ttu-id="1eaa9-113">Wenn die **filetype** -Eigenschaft den Wert 18 (0x12, Bits 0001 0010) meldet, ist es ein verborgenes Unterverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-113">If the **FileType** property reports the value 18 (0x12, bits 0001 0010), it is a hidden subdirectory.</span></span>

<span data-ttu-id="1eaa9-114">Es gibt zwei verschiedene Typen von Bitmaps, die MOF-Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="1eaa9-114">There are two different types of bitmaps using MOF code:</span></span>

-   <span data-ttu-id="1eaa9-115">Aufeinanderfolgende bedeutende Bits, beginnend mit dem nieder wertigen Bit (Bit 0)</span><span class="sxs-lookup"><span data-stu-id="1eaa9-115">Consecutive significant bits beginning with the low-order bit (bit 0)</span></span>

    <span data-ttu-id="1eaa9-116">Sie können ein Array von Bitwerten definieren, ohne die signifikanten Bits explizit anzugeben, wenn die signifikanten Bits mit dem unteren Bit (Bit 0) beginnen, und der Fortschritt ohne Unterbrechung durch alle Elemente im **BitValue** -Array.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-116">You can define an array of bit values without explicitly specifying the significant bits if the significant bits begin with the low-order bit (bit 0) and progress upward without interruption through all items in the **BitValue** array.</span></span> <span data-ttu-id="1eaa9-117">Im folgenden MOF-Codebeispiel wird die gleiche Funktion wie im vorherigen Beispiel durchführt.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-117">The following MOF code example performs the same function as the previous example.</span></span>

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   <span data-ttu-id="1eaa9-118">Signifikanter Bit, dem ein nicht signifikanter Bit vorangestellt ist</span><span class="sxs-lookup"><span data-stu-id="1eaa9-118">Significant bit preceded by a non-significant bit</span></span>

    <span data-ttu-id="1eaa9-119">Wenn das niedrig wertige Bit unerheblich ist oder die Sequenz signifikanter Bits nicht fortlaufend ist, müssen Sie sowohl die **Bitmap** -als auch die **BitValues** -Qualifizierer angeben.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-119">If the low-order bit is insignificant, or the sequence of significant bits is not continuous, you must specify both the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="1eaa9-120">Das folgende MOF-Codebeispiel zeigt eine Situation, in der das Bit mit niedriger Ordnung nicht signifikant ist und eine Lücke in der Sequenz signifikanter Bits vorliegt.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-120">The following MOF code example shows a situation in which the low-order bit is not significant and there is a gap in the sequence of significant bits.</span></span>

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    <span data-ttu-id="1eaa9-121">In diesem Fall hat das Festlegen des nieder wertigen Bits (Bit 0) keine Bedeutung und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-121">In this case, setting the low-order bit (bit 0) has no significance and is ignored.</span></span> <span data-ttu-id="1eaa9-122">Durch Festlegen von Bit 1 (0x2) wird jedoch angegeben, dass diese e-Mail-Nachricht für die Nachverfolgung gekennzeichnet ist. durch Festlegen von Bit 4 (0x8) wird angegeben, dass eine Übermittlungs Bestätigung an den Absender gesendet werden soll, wenn die e-Mail-Nachricht im Postfach des Empfängers eingetroffen ist. durch Festlegen von Bit 5 (0x10) wird angegeben, dass eine Lesebestätigung an den Absender gesendet werden soll, wenn die e-Mail-Nachricht vom Empfänger geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-122">However, setting bit 1 (0x2) indicates that this email message is flagged for follow up, setting bit 4 (0x8) indicates that a delivery receipt should be sent to the sender when the email message has arrived at the recipient's mailbox, and setting bit 5 (0x10) specifies that a read receipt should be sent to the sender when the email message is opened by the recipient.</span></span> <span data-ttu-id="1eaa9-123">Durch Festlegen aller drei signifikanten Bits (0x1A) werden alle drei Bedingungen für die e-Mail-Nachricht angegeben.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-123">Setting all three significant bits (0x1A) specifies all three conditions for the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eaa9-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eaa9-124">Remarks</span></span>

<span data-ttu-id="1eaa9-125">Wenn Sie entscheiden, ob Sie die **Bitmap**- / **Bitwerte** oder **ValueMap** / **Values** -Qualifizierer verwenden möchten, stellen Sie fest, ob einer der aufgeführten Werte gleichzeitig auftreten könnte.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-125">In deciding whether to use the **BitMap**/**BitValues** or **ValueMap**/**Values** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="1eaa9-126">Wenn mehrere gleichzeitige Werte vorhanden sein können, müssen **Bitmap**- / **Bitwerte** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-126">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="1eaa9-127">Wenn sich alle Werte gegenseitig ausschließen, sollten Sie die **ValueMap** / **Values** -Qualifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-127">If all the values are mutually exclusive, you should use the **ValueMap**/**Values** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1eaa9-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1eaa9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eaa9-129">ValueMap-und Wert Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="1eaa9-129">ValueMap and Value Qualifiers</span></span>](value-map.md)
</dt> </dl>

 

 



