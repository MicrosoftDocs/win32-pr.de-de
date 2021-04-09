---
description: NTFS speichert Dateinamen in Unicode. Im Gegensatz dazu verwenden die älteren Dateisysteme FAT12, FAT16 und FAT32 den OEM-Zeichensatz. Weitere Informationen finden Sie unter Codepages.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: In Dateinamen verwendete Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866104"
---
# <a name="character-sets-used-in-file-names"></a><span data-ttu-id="724f6-105">In Dateinamen verwendete Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="724f6-105">Character Sets Used in File Names</span></span>

<span data-ttu-id="724f6-106">NTFS speichert Dateinamen in Unicode.</span><span class="sxs-lookup"><span data-stu-id="724f6-106">NTFS stores file names in Unicode.</span></span> <span data-ttu-id="724f6-107">Im Gegensatz dazu verwenden die älteren Dateisysteme FAT12, FAT16 und FAT32 den OEM-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="724f6-107">In contrast, the older FAT12, FAT16, and FAT32 file systems use the OEM character set.</span></span> <span data-ttu-id="724f6-108">Weitere Informationen finden Sie unter [Codepages](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="724f6-108">For more information, see [Code Pages](code-pages.md).</span></span>

<span data-ttu-id="724f6-109">Nicht-Unicode-Anwendungen, die FAT-Dateien erstellen, müssen manchmal die standardmäßigen C-Lauf Zeit Bibliotheks-Konvertierungs Funktionen verwenden, um zwischen dem Windows-Codepage-Zeichensatz und dem OEM-Codepage-Zeichensatz</span><span class="sxs-lookup"><span data-stu-id="724f6-109">Non-Unicode applications that create FAT files sometimes have to use the standard C runtime library conversion functions to translate between the Windows code page character set and the OEM code page character set.</span></span> <span data-ttu-id="724f6-110">Bei Unicode-Implementierungen der Dateisystemfunktionen ist es nicht notwendig, solche Übersetzungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="724f6-110">With Unicode implementations of the file system functions, it is not necessary to perform such translations.</span></span>

<span data-ttu-id="724f6-111">Die Anwendung kann generische Zeichen folgen Typen verwenden, wie unter [Windows-Datentypen für](windows-data-types-for-strings.md)Zeichen folgen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="724f6-111">Your application can use generic string types, as described in [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span> <span data-ttu-id="724f6-112">Die Anwendung kann auch generische Funktionsprototypen mithilfe von Verfahren verwenden, die in [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="724f6-112">The application can also use generic function prototypes using techniques described in [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span> <span data-ttu-id="724f6-113">Bei generischen Zeichen folgen Typen oder generischen Funktionsprototypen kann die Anwendung eine einzelne Quelldatei verwenden, um entweder eine Unicode-oder eine nicht-Unicode-Version zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="724f6-113">For either generic string types or generic function prototypes, your application can use a single source file to compile either a Unicode or a non-Unicode version.</span></span> <span data-ttu-id="724f6-114">Um dies zuzulassen, stellt die Anwendung Makros für Funktionen bereit, die beim Kompilieren für Unicode nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="724f6-114">To allow for this, the application provides macros for functions that are not invoked when compiling for Unicode.</span></span>

<span data-ttu-id="724f6-115">In NTFS-und FAT-Dateisystemen lauten die Sonderzeichen " \\ ", "/", ".", "?" und "" \* .</span><span class="sxs-lookup"><span data-stu-id="724f6-115">In both NTFS and FAT file systems, the special file name characters are: '\\', '/', '.', '?', and '\*'.</span></span> <span data-ttu-id="724f6-116">Auf OEM-Codepages befinden sich diese Sonderzeichen im ASCII-Zeichenbereich (0x00 bis 0x7F).</span><span class="sxs-lookup"><span data-stu-id="724f6-116">On OEM code pages, these special characters are in the ASCII range of characters (0x00 through 0x7F).</span></span> <span data-ttu-id="724f6-117">Ihre Unicode-Entsprechungen sind dieselben Werte in einem 2-Byte-Formular, 0x0000 bis 0x007F.</span><span class="sxs-lookup"><span data-stu-id="724f6-117">Their Unicode equivalents are the same values in a 2-byte form, 0x0000 through 0x007F.</span></span>

> [!Caution]  
> <span data-ttu-id="724f6-118">Windows-Codepage-und OEM-Codepage-Zeichensätze, die für Japanisch sprachige Betriebssysteme verwendet werden, enthalten das Yen-Symbol (Yen) anstelle eines umgekehrten Schrägstrichs ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="724f6-118">Windows code page and OEM code page character sets used on Japanese-language operating systems contain the Yen symbol (¥) instead of a backslash (\\).</span></span> <span data-ttu-id="724f6-119">Daher ist das Yen-Symbol ein unzulässiges Zeichen für NTFS-und FAT-Dateisysteme.</span><span class="sxs-lookup"><span data-stu-id="724f6-119">Thus, the Yen symbol is a prohibited character for NTFS and FAT file systems.</span></span> <span data-ttu-id="724f6-120">Bei der Zuordnung von Unicode zu einer japanischen Codepage ordnen [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) und andere Konvertierungs Funktionen den umgekehrten Schrägstrich (u + 005c) und das normale Unicode-Yen-Symbol (u + 00a5) dem gleichen Zeichen zu.</span><span class="sxs-lookup"><span data-stu-id="724f6-120">When mapping Unicode to a Japanese-language code page, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and other conversion functions map both backslash (U+005C) and the normal Unicode Yen symbol (U+00A5) to this same character.</span></span> <span data-ttu-id="724f6-121">Aus Sicherheitsgründen sollten Ihre Anwendungen in der Regel nicht das Zeichen U + 00a5 in einer Unicode-Zeichenfolge zulassen, die zur Verwendung als FAT-Dateinamen konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="724f6-121">For security reasons, your applications should not typically allow the character U+00A5 in a Unicode string that might be converted for use as a FAT file name.</span></span> <span data-ttu-id="724f6-122">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="724f6-122">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="724f6-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="724f6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="724f6-124">Unicode in der Windows-API</span><span class="sxs-lookup"><span data-stu-id="724f6-124">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> <dt>

[<span data-ttu-id="724f6-125">Überlegungen zur Sicherheit: Internationale Features</span><span class="sxs-lookup"><span data-stu-id="724f6-125">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 



