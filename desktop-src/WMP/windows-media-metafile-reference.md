---
title: Referenz zu Windows Media-Metadateien
description: Referenz zu Windows Media-Metadateien
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Media-Metadateien, Referenz
- Metadatendateien, Referenz
- Referenz für Windows Media-Metadatendateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036926"
---
# <a name="windows-media-metafile-reference"></a><span data-ttu-id="a727b-106">Referenz zu Windows Media-Metadateien</span><span class="sxs-lookup"><span data-stu-id="a727b-106">Windows Media Metafile Reference</span></span>

<span data-ttu-id="a727b-107">Dieser Verweis dokumentiert Elemente und Dateinamen Erweiterungen für Windows Media-Metadatendateien.</span><span class="sxs-lookup"><span data-stu-id="a727b-107">This reference documents elements and file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="a727b-108">Der Verweis ist in die folgenden Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="a727b-108">The reference is divided into the following sections.</span></span>



| <span data-ttu-id="a727b-109">`Section`</span><span class="sxs-lookup"><span data-stu-id="a727b-109">Section</span></span>                                                                                    | <span data-ttu-id="a727b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a727b-110">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a727b-111">Verweis auf Windows Media-Metadateielemente</span><span class="sxs-lookup"><span data-stu-id="a727b-111">Windows Media Metafile Elements Reference</span></span>](windows-media-metafile-elements-reference.md) | <span data-ttu-id="a727b-112">Dokumentiert Metadatei-Elemente, einschließlich Definitionen, Attribute und deren Werte, sowie spezielle Bedingungen, die sich auf die einzelnen Elemente beziehen.</span><span class="sxs-lookup"><span data-stu-id="a727b-112">Documents metafile elements, including definitions, attributes and their values, and special conditions related to each element.</span></span> |
| [<span data-ttu-id="a727b-113">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="a727b-113">File Name Extensions</span></span>](file-name-extensions.md)                                           | <span data-ttu-id="a727b-114">Dokumentiert Dateinamen Erweiterungen für Metadateien mit Regeln und Richtlinien zur Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a727b-114">Documents metafile file name extensions with rules and guidelines on their use.</span></span>                                                  |



 

<span data-ttu-id="a727b-115">Windows Media-Metadateien sind Textdateien, die Informationen über einen Dateistream und seine Präsentation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a727b-115">Windows Media metafiles are text files that provide information about a file stream and its presentation.</span></span> <span data-ttu-id="a727b-116">Die Metadatendateien basieren auf der Syntax von Extensible Markup Language (XML) und bestehen aus verschiedenen XML-ähnlichen Elementen mit ihren Tags und Attributen.</span><span class="sxs-lookup"><span data-stu-id="a727b-116">The metafiles are based on the Extensible Markup Language (XML) syntax, and are made up of various XML-like elements with their tags and attributes.</span></span> <span data-ttu-id="a727b-117">Jedes Element definiert eine Einstellung oder Aktion für Streaming-Medien.</span><span class="sxs-lookup"><span data-stu-id="a727b-117">Each element defines a setting or action for streaming media.</span></span>

<span data-ttu-id="a727b-118">Es sind zwei Sätze von Element Tags für Metadateien verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a727b-118">There are two sets of element tags available for metafiles.</span></span> <span data-ttu-id="a727b-119">Client seitige Metadateien haben einen Satz von Elementen, und serverseitige Metadateien verfügen über einen anderen Satz von Elementen.</span><span class="sxs-lookup"><span data-stu-id="a727b-119">Client-side metafiles have one set of elements, and server-side metafiles have another set of elements.</span></span>

<span data-ttu-id="a727b-120">Wenn ein Elementtag keine untergeordneten Elemente hat (die Elemente, die sich in einem anderen Element ändern oder befinden), kann ein einzelner Schrägstrich (/) am Ende des öffnenden Tags anstelle eines Endtags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a727b-120">If an element tag does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag in place of a closing tag.</span></span> <span data-ttu-id="a727b-121">Wenn untergeordnete Elemente nicht zwischen dem öffnenden und dem schließenden Tag für ein Element angezeigt werden, sind Sie keine untergeordneten Elemente für dieses Element und werden ignoriert, oder es wird ein Fehler in der Syntax der Metadatei verursacht.</span><span class="sxs-lookup"><span data-stu-id="a727b-121">If child elements do not appear between the opening and closing tag for an element, they are not child elements for that element, and are ignored or cause an error in the syntax of the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a727b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a727b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a727b-123">**Informationen zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="a727b-123">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="a727b-124">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="a727b-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="a727b-125">**Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="a727b-125">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




