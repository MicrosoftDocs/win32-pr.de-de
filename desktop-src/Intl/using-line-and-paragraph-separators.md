---
description: Ihre Anwendungen sollten das Zeilen Trennzeichen (0x2028) und das Absatz Trennzeichen (0x2029) verwenden, um nur-Text aufzuteilen. Nach jeder Zeilentrennung wird eine neue Zeile begonnen. Nach jedem Absatztrennzeichen wird ein neuer Absatz begonnen.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Verwenden von Zeilen-und Absatz Trennzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218690"
---
# <a name="using-line-and-paragraph-separators"></a><span data-ttu-id="5a99f-105">Verwenden von Zeilen-und Absatz Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="5a99f-105">Using Line and Paragraph Separators</span></span>

<span data-ttu-id="5a99f-106">Ihre Anwendungen sollten das Zeilen Trennzeichen (0x2028) und das Absatz Trennzeichen (0x2029) verwenden, um nur-Text aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="5a99f-106">Your applications should use the line separator character (0x2028) and the paragraph separator character (0x2029) to divide plain text.</span></span> <span data-ttu-id="5a99f-107">Nach jeder Zeilentrennung wird eine neue Zeile begonnen.</span><span class="sxs-lookup"><span data-stu-id="5a99f-107">A new line is begun after each line separator.</span></span> <span data-ttu-id="5a99f-108">Nach jedem Absatztrennzeichen wird ein neuer Absatz begonnen.</span><span class="sxs-lookup"><span data-stu-id="5a99f-108">A new paragraph is begun after each paragraph separator.</span></span>

<span data-ttu-id="5a99f-109">Es ist nicht erforderlich, die erste Zeile oder den Absatz in einer Datei mit diesen Zeichen zu starten oder die letzte Zeile bzw. den letzten Absatz mit Ihnen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="5a99f-109">It is not necessary to start the first line or paragraph in a file with these characters, or to end the last line or paragraph with them.</span></span> <span data-ttu-id="5a99f-110">Dies deutet darauf hin, dass es eine leere Zeile oder einen leeren Absatz an diesem Speicherort gibt.</span><span class="sxs-lookup"><span data-stu-id="5a99f-110">Doing so indicates that there is an empty line or paragraph in that location.</span></span>

<span data-ttu-id="5a99f-111">Die Anwendung kann das Zeilen Trennzeichen verwenden, um ein unbedingtes Zeilenende anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5a99f-111">The application can use the line separator to indicate an unconditional end of line.</span></span> <span data-ttu-id="5a99f-112">Zeilentrennzeichen entsprechen jedoch nicht den gesonderten Wagenrücklauf- oder Zeilenvorschubzeichen oder einer Kombination dieser Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5a99f-112">However, line separators do not correspond to the separate carriage return and linefeed characters, or to a combination of these characters.</span></span> <span data-ttu-id="5a99f-113">Zeilentrennzeichen müssen getrennt von Wagenrücklauf- und Zeilenvorschubzeichen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5a99f-113">Line separators must be processed separately from carriage return and linefeed characters.</span></span>

<span data-ttu-id="5a99f-114">Die Anwendung kann ein Absatz Trennzeichen zwischen Text Absätzen einfügen.</span><span class="sxs-lookup"><span data-stu-id="5a99f-114">The application can insert a paragraph separator between paragraphs of text.</span></span> <span data-ttu-id="5a99f-115">Die Verwendung dieses Trennzeichens ermöglicht das Erstellen von Nur-Text-Dateien, die mit unterschiedlichen Zeilenhöhen auf verschiedenen Betriebssystemen formatiert werden können.</span><span class="sxs-lookup"><span data-stu-id="5a99f-115">Use of this separator allows creation of plain text files that can be formatted with different line widths on different operating systems.</span></span> <span data-ttu-id="5a99f-116">Das Zielsystem kann Zeilentrennzeichen ignorieren und Absätze nur bei den Absatztrennzeichen umbrechen.</span><span class="sxs-lookup"><span data-stu-id="5a99f-116">The target system can ignore any line separators and break paragraphs only at the paragraph separators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a99f-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a99f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a99f-118">Verwenden von Sonderzeichen in Unicode</span><span class="sxs-lookup"><span data-stu-id="5a99f-118">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



