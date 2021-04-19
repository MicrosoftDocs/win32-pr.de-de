---
description: Stellen Sie immer eine Unicode-nur-Text-Datei mit einer Byte Reihenfolge-Markierung vor, die einer Anwendung mitteilt, dass die Datei in Byte sortiert ist.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Verwenden von Byte Reihenfolge Markierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366497"
---
# <a name="using-byte-order-marks"></a><span data-ttu-id="8cb87-103">Verwenden von Byte Reihenfolge Markierungen</span><span class="sxs-lookup"><span data-stu-id="8cb87-103">Using Byte Order Marks</span></span>

<span data-ttu-id="8cb87-104">Stellen Sie immer eine Unicode-nur-Text-Datei mit einer Byte Reihenfolge-Markierung vor, die einer Anwendung mitteilt, dass die Datei in Byte sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cb87-104">Always prefix a Unicode plain text file with a byte order mark, which informs an application receiving the file that the file is byte-ordered.</span></span> <span data-ttu-id="8cb87-105">In der folgenden Tabelle sind die verfügbaren Byte-Reihenfolge Markierungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb87-105">Available byte order marks are listed in the following table.</span></span> <span data-ttu-id="8cb87-106">Da der nur-Text-Unicode-Text eine Sequenz von 16-Bit-Codewerten ist, ist er für die beim Schreiben des Texts verwendete Byte Reihenfolge empfindlich.</span><span class="sxs-lookup"><span data-stu-id="8cb87-106">Because Unicode plain text is a sequence of 16-bit code values, it is sensitive to the byte ordering used when the text is written.</span></span>

> [!Note]  
> <span data-ttu-id="8cb87-107">Eine Byte Reihenfolge Markierung ist kein Steuerzeichen, das die Byte Reihenfolge des Texts auswählt.</span><span class="sxs-lookup"><span data-stu-id="8cb87-107">A byte order mark is not a control character that selects the byte order of the text.</span></span>

 



| <span data-ttu-id="8cb87-108">Bytereihenfolge-Marke</span><span class="sxs-lookup"><span data-stu-id="8cb87-108">Byte order mark</span></span> | <span data-ttu-id="8cb87-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cb87-109">Description</span></span>           |
|-----------------|-----------------------|
| <span data-ttu-id="8cb87-110">EF BB BF</span><span class="sxs-lookup"><span data-stu-id="8cb87-110">EF BB BF</span></span>        | <span data-ttu-id="8cb87-111">UTF-8</span><span class="sxs-lookup"><span data-stu-id="8cb87-111">UTF-8</span></span>                 |
| <span data-ttu-id="8cb87-112">FF FE</span><span class="sxs-lookup"><span data-stu-id="8cb87-112">FF FE</span></span>           | <span data-ttu-id="8cb87-113">UTF-16, Little-d</span><span class="sxs-lookup"><span data-stu-id="8cb87-113">UTF-16, little endian</span></span> |
| <span data-ttu-id="8cb87-114">FE FF</span><span class="sxs-lookup"><span data-stu-id="8cb87-114">FE FF</span></span>           | <span data-ttu-id="8cb87-115">UTF-16, Big-ddian</span><span class="sxs-lookup"><span data-stu-id="8cb87-115">UTF-16, big endian</span></span>    |
| <span data-ttu-id="8cb87-116">FF FE 00 00</span><span class="sxs-lookup"><span data-stu-id="8cb87-116">FF FE 00 00</span></span>     | <span data-ttu-id="8cb87-117">UTF-32, Little-d</span><span class="sxs-lookup"><span data-stu-id="8cb87-117">UTF-32, little endian</span></span> |
| <span data-ttu-id="8cb87-118">00 00 FE FF</span><span class="sxs-lookup"><span data-stu-id="8cb87-118">00 00 FE FF</span></span>     | <span data-ttu-id="8cb87-119">UTF-32, Big-enddian</span><span class="sxs-lookup"><span data-stu-id="8cb87-119">UTF-32, big-endian</span></span>    |



 

> [!Note]  
> <span data-ttu-id="8cb87-120">Microsoft verwendet UTF-16, Little-Endian-Byte Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8cb87-120">Microsoft uses UTF-16, little endian byte order.</span></span>

 

<span data-ttu-id="8cb87-121">Im Idealfall folgt der gesamte Unicode-Text nur einem Satz von Byte Reihenfolge Regeln.</span><span class="sxs-lookup"><span data-stu-id="8cb87-121">Ideally, all Unicode text follows only one set of byte ordering rules.</span></span> <span data-ttu-id="8cb87-122">Dies ist jedoch nicht möglich, da sich die Mikroprozessoren bei der Platzierung des am wenigsten signifikanten Bytes unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="8cb87-122">This is not possible, however, because microprocessors differ in the placement of the least significant byte.</span></span> <span data-ttu-id="8cb87-123">Intel-und MIPS-Prozessoren positionieren das am wenigsten signifikante Byte zuerst, während von den Motorola-Prozessoren (und allen Byte-umgekehrten Unicode-Dateien) die letzte Position angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb87-123">Intel and MIPS processors position the least significant byte first, whereas Motorola processors (and all byte-reversed Unicode files) position it last.</span></span> <span data-ttu-id="8cb87-124">Mit nur einem einzigen Satz von Byte Sortierregeln werden Benutzer von einem Typ von Mikroprozessor gezwungen, die Byte Reihenfolge jedes Mal auszutauschen, wenn eine nur-Text-Datei aus gelesen oder geschrieben wird, auch wenn die Datei nie auf ein anderes Betriebssystem auf der Grundlage eines anderen Mikroprozessors übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="8cb87-124">With only a single set of byte ordering rules, users of one type of microprocessor are forced to swap the byte order every time a plain text file is read from or written to, even if the file is never transferred to another operating system based on a different microprocessor.</span></span>

<span data-ttu-id="8cb87-125">Der bevorzugte Ort zum Angeben der Byte Reihenfolge ist in einem Dateiheader, Textdateien haben jedoch keine Header.</span><span class="sxs-lookup"><span data-stu-id="8cb87-125">The preferred place to specify byte order is in a file header, but text files do not have headers.</span></span> <span data-ttu-id="8cb87-126">Daher hat Unicode ein Zeichen (u + FEFF) und ein nicht-Zeichen (u + FFFE) als Byte Reihenfolge Markierungen definiert.</span><span class="sxs-lookup"><span data-stu-id="8cb87-126">Therefore, Unicode has defined a character (U+FEFF) and a noncharacter (U+FFFE) as byte order marks.</span></span> <span data-ttu-id="8cb87-127">Sie sind Spiegel Byte Bilder zueinander.</span><span class="sxs-lookup"><span data-stu-id="8cb87-127">They are mirror byte images of each other.</span></span>

<span data-ttu-id="8cb87-128">Da die Sequenz U + FEFF am Anfang einer regulären nicht-Unicode-Textdatei sehr selten vorkommt, kann Sie als impliziter Marker oder eine Signatur dienen, um die Datei als Unicode-Datei zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8cb87-128">Since the sequence U+FEFF is exceedingly rare at the beginning of a regular non-Unicode text file, it can serve as an implicit marker or signature to identify the file as a Unicode file.</span></span> <span data-ttu-id="8cb87-129">Anwendungen, die sowohl Unicode-als auch nicht-Unicode-Textdateien lesen, sollten das vorhanden sein dieser Sequenz als Indikator verwenden, dass es sich bei der Datei höchstwahrscheinlich um eine Unicode-Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="8cb87-129">Applications that read both Unicode and non-Unicode text files should use the presence of this sequence as an indicator that the file is most likely a Unicode file.</span></span> <span data-ttu-id="8cb87-130">Vergleichen Sie diese Technik mit der Verwendung des MS-DOS-markermarkers zum Beenden von Textdateien.</span><span class="sxs-lookup"><span data-stu-id="8cb87-130">Compare this technique to using the MS-DOS EOF marker to terminate text files.</span></span>

<span data-ttu-id="8cb87-131">Wenn eine Anwendung am Anfang einer Textdatei U + FEFF findet, wird die Datei in der Regel als Unicode-Datei verarbeitet, obwohl Sie weitere heuristische Prüfungen zur Überprüfung durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="8cb87-131">When an application finds U+FEFF at the beginning of a text file, it typically processes the file as a Unicode file, although it can perform further heuristic checks for verification.</span></span> <span data-ttu-id="8cb87-132">Eine solche Überprüfung kann so einfach wie das Testen sein, um herauszufinden, ob die Variation in den nieder wertigen Bytes deutlich höher ist als die Variation in den höherwertigen Bytes.</span><span class="sxs-lookup"><span data-stu-id="8cb87-132">Such a check can be as simple as testing to find out if the variation in the low-order bytes is much higher than the variation in the high-order bytes.</span></span> <span data-ttu-id="8cb87-133">Wenn z. b. ASCII-Text in Unicode-Text konvertiert wird, ist jedes zweite Byte 0.</span><span class="sxs-lookup"><span data-stu-id="8cb87-133">For example, if ASCII text is converted to Unicode text, every second byte is 0.</span></span> <span data-ttu-id="8cb87-134">Außerdem kann die Überprüfung sowohl für den Zeilenvorschub als auch das Wagen Rücklauf Zeichen (u + 000A und U + 000D) sowie für die gerade oder ungerade Dateigröße einen starken Indikator für die Art der Datei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8cb87-134">Also, checking both for the linefeed and carriage return characters (U+000A and U+000D) and for even or odd file size can provide a strong indicator of the nature of the file.</span></span>

<span data-ttu-id="8cb87-135">Wenn eine Anwendung am Anfang einer Textdatei U + FFFE findet, wird Sie so interpretiert, dass die Datei eine Byte-umgekehrte Unicode-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="8cb87-135">When an application finds U+FFFE at the beginning of a text file, it interprets it to mean that the file is a byte-reversed Unicode file.</span></span> <span data-ttu-id="8cb87-136">Die Anwendung kann entweder die Reihenfolge der Bytes austauschen oder den Benutzer darüber benachrichtigen, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8cb87-136">The application can either swap the order of the bytes or alert the user that an error has occurred.</span></span>

<span data-ttu-id="8cb87-137">Da das Unicode-Byte Reihenfolge-Zeichen nicht in einer Codepage gefunden wird, wird es nicht mehr angezeigt, wenn Daten in ANSI konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="8cb87-137">Since the Unicode byte order mark character is not found in any code page, it disappears if data is converted to ANSI.</span></span> <span data-ttu-id="8cb87-138">Im Gegensatz zu anderen Unicode-Zeichen wird es beim Konvertieren nicht durch ein Standard Zeichen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8cb87-138">Unlike other Unicode characters, it is not replaced by a default character when it is converted.</span></span> <span data-ttu-id="8cb87-139">Wenn eine Byte Reihenfolge-Markierung in der Mitte einer Datei gefunden wird, wird Sie nicht als Unicode-Zeichen interpretiert und hat keine Auswirkung auf die Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="8cb87-139">If a byte order mark is found in the middle of a file, it is not interpreted as a Unicode character and has no effect on text output.</span></span>

> [!Note]  
> <span data-ttu-id="8cb87-140">Der Unicode-Wert U + FFFF ist in nur-Text-Dateien unzulässig und kann nicht zwischen Anwendungen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8cb87-140">The Unicode value U+FFFF is illegal in plain text files and cannot be passed between applications.</span></span> <span data-ttu-id="8cb87-141">Es ist für die private Verwendung einer Anwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8cb87-141">It is reserved for the private use of an application.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8cb87-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cb87-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cb87-143">Verwenden von Sonderzeichen in Unicode</span><span class="sxs-lookup"><span data-stu-id="8cb87-143">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



