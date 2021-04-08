---
description: GraphEdit-Datei Format
ms.assetid: 84c2de05-6c8f-45f1-b789-04a24cfa3ea1
title: GraphEdit-Datei Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a75421ff75c9bb26901eddf423448bbd9e4f478
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747632"
---
# <a name="graphedit-file-format"></a><span data-ttu-id="8333b-103">GraphEdit-Datei Format</span><span class="sxs-lookup"><span data-stu-id="8333b-103">GraphEdit File Format</span></span>

<span data-ttu-id="8333b-104">Wenn das Hilfsprogramm GraphEdit ein DirectShow-Filter Diagramm speichert, werden Speicherdateien mit der Erweiterung. GRF erstellt.</span><span class="sxs-lookup"><span data-stu-id="8333b-104">When the GraphEdit utility saves a DirectShow filter graph, it creates a storage files with a .grf extension.</span></span> <span data-ttu-id="8333b-105">Die Speicherdatei enthält einen einzelnen Datenstrom mit dem Namen activemuviegraph.</span><span class="sxs-lookup"><span data-stu-id="8333b-105">The storage file contains a single stream called ActiveMovieGraph.</span></span> <span data-ttu-id="8333b-106">Dieser Stream enthält Informationen zu allen Filtern, Filternamen, Dateinamen, Verbindungen usw.</span><span class="sxs-lookup"><span data-stu-id="8333b-106">This stream contains information about all of the filters, filter names, file names, connections, and so forth.</span></span>

<span data-ttu-id="8333b-107">Die folgende Grammatik beschreibt die Syntax des Diagramms innerhalb des Streams mithilfe einer geänderten BNF-Syntax (Backus-Naur Form):</span><span class="sxs-lookup"><span data-stu-id="8333b-107">The following grammar describes the syntax of the graph within the stream, using a modified BNF (Backus-Naur Form) syntax:</span></span>


```C++
<graph> ::= 
0003\r\n<filters><connections><clock>
END | 
0002\r\n<filters><connections>
END
<filters> ::= 
FILTERS<b> 
[<filter list><b>
]
<filter list> ::= <filter><b> 
[<filter list>
]
<filter> ::= <filter id><b><name><b><class id><b>
[<file>
]<length><b1><filter data>
<class id> ::= <guid>
<file> ::= 
SOURCE <name><b> | 
SINK <name><b>
<connections> ::= 
CONNECTIONS<b> 
{<connection><b>
}
<connection> ::= <filter id><b><pin id><b><filter id><b><pin id><b><media type>
<filter id> ::= <id>
<pin id> ::= <name>
<media type> ::= <sample size><major type><b><subtype><b><flags><format>
<major type> ::= <guid>
<subtype> ::= <guid>
<flags> ::= <fixed sample size><b><temporal compression><b>
<fixed sample size> ::= 1 
| 0
<temporal compression> ::= 1 
| 0
<format> ::= <length><b1><format type><b><length><b1><format data>
<format type> ::= <guid>
<format data> ::= 
{ binary_data 
}
<clock> ::= 
CLOCK <b><required><b><clockid>
\r\n
<required> ::= 1 
| 0
<clockid> ::= <filter id> 
| <class id>
<name> ::= quote_symbol 
{ any_non_quote_character 
} quote_symbol
<length> ::= unsigned decimal number (as a string), indicating the number 
             of bytes of data in the following token.
<guid> ::= GUID in string format. for example: {CF49D4E0-1115-11CE-B03A-0020AF0BA770}
<b> ::= 
{ space_character 
} 
{ \t 
} 
{ \r 
} 
{ \n 
} { <b> 
}
<b1> ::= space_character
<id> ::= integer (as a string), such as 0001
```



<span data-ttu-id="8333b-108">Bei der Ausgabe gibt es eine neue Zeile (" \\ r \\ n") pro Filter, eine pro Verbindung und eine für jedes der Schlüsselwort Filter und-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="8333b-108">On output there will be a new line ("\\r\\n") per filter, one per connection, and one for each of the keywords FILTERS and CONNECTIONS.</span></span> <span data-ttu-id="8333b-109">Bei jedem anderen Fall von handelt es sich um <b> ein einzelnes Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="8333b-109">Each other case of <b> will be a single space.</span></span> <span data-ttu-id="8333b-110">Die Schlüsselwörter Filter, Connections und End sind nicht lokalisierbar.</span><span class="sxs-lookup"><span data-stu-id="8333b-110">The keywords FILTERS, CONNECTIONS, and END are not localizable.</span></span> <span data-ttu-id="8333b-111">Beachten Sie auch, dass die Filterdaten und die Formatierungsdaten binär sind, sodass Sie falsche Zeilenumbrüche, NULL-Werte usw. enthalten können.</span><span class="sxs-lookup"><span data-stu-id="8333b-111">Note also that the filter data and the format data are binary, so they might contain incorrect line breaks, null values, and so on.</span></span> <span data-ttu-id="8333b-112">Der Stream verwendet breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8333b-112">The stream uses wide characters.</span></span>

<span data-ttu-id="8333b-113">Im folgenden wird ein typisches Diagramm gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8333b-113">The following shows a typical graph.</span></span> <span data-ttu-id="8333b-114">(Die Verbindungs Zeilen wurden aus Gründen der Übersichtlichkeit getrennt, und die Binärdaten wurden ausgelassen.)</span><span class="sxs-lookup"><span data-stu-id="8333b-114">(The connection lines have been broken for clarity, and the binary data omitted.)</span></span>


```C++
003
FILTERS
0001 "C:\SomeFile.avi" {E436EBB5-524F-11CE-9F53-0020AF0BA770} SOURCE "C:\SomeFile.avi" 0000000000 
0002 "AVI Splitter" {1B544C20-FD0B-11CE-8C63-00AA0044B51E} 0000000000 
0003 "AVI Decompressor" {CF49D4E0-1115-11CE-B03A-0020AF0BA770} 0000000000
0004 "Video Renderer" {70E102B0-5556-11CE-97C0-00AA0055595A} 0000000000
CONNECTIONS
0001 "Output" 0002 "input pin" 0000000288 
   {E436EB83-524F-11CE-9F53-0020AF0BA770} 
   {E436EB88-524F-11CE-9F53-0020AF0BA770} 1 0 0000000001 
   {00000000-0000-0000-0000-000000000000} 0000000000  
0002 "Stream 00" 0003 "In" 0000000376 
   {73646976-0000-0010-8000-00AA00389B71} 
   {64697663-0000-0010-8000-00AA00389B71} 0 0 0000000001 
   {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data>
0003 "Out" 0004 "In" 0000000376 
    {73646976-0000-0010-8000-00AA00389B71} 
    {E436EB7D-524F-11CE-9F53-0020AF0BA770} 1 0 0000129600 
    {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data> 
CLOCK 1 0000
END
```



## <a name="related-topics"></a><span data-ttu-id="8333b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8333b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8333b-116">Simulieren der Diagramm Erstellung mit GraphEdit</span><span class="sxs-lookup"><span data-stu-id="8333b-116">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



