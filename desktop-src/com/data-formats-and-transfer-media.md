---
title: Datenformate und Übertragungsmedien
description: Datenformate und Übertragungsmedien
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104039829"
---
# <a name="data-formats-and-transfer-media"></a><span data-ttu-id="00c3f-103">Datenformate und Übertragungsmedien</span><span class="sxs-lookup"><span data-stu-id="00c3f-103">Data Formats and Transfer Media</span></span>

<span data-ttu-id="00c3f-104">Die meisten Plattformen, einschließlich Windows, definieren ein Standardprotokoll für die Übertragung von Daten zwischen Anwendungen, basierend auf einem Satz von Funktionen, die als Zwischenablage bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="00c3f-104">Most platforms, including Windows, define a standard protocol for transferring data between applications, based on a set of functions called the clipboard.</span></span> <span data-ttu-id="00c3f-105">Anwendungen, die diese Funktionen verwenden, können Daten freigeben, auch wenn Ihre nativen Datenformate stark voneinander abweichen.</span><span class="sxs-lookup"><span data-stu-id="00c3f-105">Applications using these functions can share data even if their native data formats are wildly different.</span></span> <span data-ttu-id="00c3f-106">Im Allgemeinen haben diese zwischen Ablagen zwei bedeutende Mängel, die com überwunden hat.</span><span class="sxs-lookup"><span data-stu-id="00c3f-106">Generally, these clipboards have two significant shortcomings that COM has overcome.</span></span>

<span data-ttu-id="00c3f-107">Zuerst verwenden Daten Beschreibungen nur einen Format Bezeichner, z. b. den einzelnen 16-Bit-Format Bezeichner für die Zwischenablage unter Windows. Dies bedeutet, dass die Zwischenablage nur die Struktur Ihrer Daten beschreiben kann, d. h. die Reihenfolge der Bits.</span><span class="sxs-lookup"><span data-stu-id="00c3f-107">First, data descriptions use only a format identifier, such as the single 16-bit clipboard format identifier on Windows, which means the clipboard can only describe the structure of its data, that is, the ordering of the bits.</span></span> <span data-ttu-id="00c3f-108">Es kann berichtet werden: "Ich verfüge über eine Bitmap", oder ich habe Text, aber es kann nicht die Zielgeräte angeben, für die die Daten erstellt werden, welche Sichten oder Aspekte selbst die Daten bereitstellen können oder welche Speichermedien am besten für die Übertragung geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="00c3f-108">It can report, "I have a bitmap" "or I have some text," but it cannot specify the target devices for which the data is composed, which views or aspects of itself the data can provide, or which storage media are best suited for its transfer.</span></span> <span data-ttu-id="00c3f-109">Beispielsweise kann nicht berichtet werden: "Ich habe eine Text Zeichenfolge, die im globalen Speicher gespeichert ist und für die Präsentation entweder auf dem Bildschirm oder auf einem Drucker formatiert ist." oder "Ich habe eine Miniaturansicht der Miniaturansicht für einen 100 dpi-Punkt-Matrix-Drucker gerendert und als Datenträger Datei gespeichert."</span><span class="sxs-lookup"><span data-stu-id="00c3f-109">For example, it cannot report, "I have a string of text that is stored in global memory and formatted for presentation either on screen or on a printer" or "I have a thumbnail sketch bitmap rendered for a 100 dpi dot-matrix printer and stored as a disk file."</span></span>

<span data-ttu-id="00c3f-110">Zweitens erfolgen alle Datenübertragungen, die die Zwischenablage verwenden, im Allgemeinen durch globalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="00c3f-110">Second, all data transfers using the clipboard generally occur through global memory.</span></span> <span data-ttu-id="00c3f-111">Die Verwendung des globalen Speichers ist für kleine Datenmengen, aber erschreckend ineffizient für große Mengen, z. b. ein Multimediaobjekt von 20 MB, ausreichend effizient.</span><span class="sxs-lookup"><span data-stu-id="00c3f-111">Using global memory is reasonably efficient for small amounts of data but horribly inefficient for large amounts, such as a 20 MB multimedia object.</span></span> <span data-ttu-id="00c3f-112">Der globale Arbeitsspeicher ist bei einem großen Datenobjekt langsam, dessen Größe einen beträchtlichen Austausch in den virtuellen Arbeitsspeicher auf dem Datenträger erfordert.</span><span class="sxs-lookup"><span data-stu-id="00c3f-112">Global memory is slow for a large data object, whose size requires considerable swapping to virtual memory on disk.</span></span> <span data-ttu-id="00c3f-113">In Fällen, in denen sich die ausgetauschten Daten größtenteils auf dem Datenträger befinden, ist das Erzwingen dieses virtuellen Arbeitsspeichers äußerst ineffizient.</span><span class="sxs-lookup"><span data-stu-id="00c3f-113">In cases where the data being exchanged is going to reside mostly on disk anyway, forcing it through this virtual-memory bottleneck is highly inefficient.</span></span> <span data-ttu-id="00c3f-114">Eine bessere Möglichkeit würde den globalen Speicher vollständig überspringen und die Daten einfach direkt auf den Datenträger übertragen.</span><span class="sxs-lookup"><span data-stu-id="00c3f-114">A better way would skip global memory entirely and simply transfer the data directly to disk.</span></span>

<span data-ttu-id="00c3f-115">Um diese Probleme zu beheben, stellt com zwei Datenstrukturen bereit: [**formatusw**](/windows/win32/api/objidl/ns-objidl-formatetc) . und [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span><span class="sxs-lookup"><span data-stu-id="00c3f-115">To alleviate these problems, COM provides two data structures: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) and [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span></span> <span data-ttu-id="00c3f-116">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="00c3f-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="00c3f-117">Die FORMATETC-Struktur</span><span class="sxs-lookup"><span data-stu-id="00c3f-117">The FORMATETC Structure</span></span>](the-formatetc-structure.md)
-   [<span data-ttu-id="00c3f-118">Die STGMEDIUM-Struktur</span><span class="sxs-lookup"><span data-stu-id="00c3f-118">The STGMEDIUM Structure</span></span>](the-stgmedium-structure.md)

## <a name="related-topics"></a><span data-ttu-id="00c3f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00c3f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00c3f-120">Datenübertragung</span><span class="sxs-lookup"><span data-stu-id="00c3f-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




