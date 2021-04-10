---
title: Kopieren von Daten aus einer Datei in eine andere
description: Kopieren von Daten aus einer Datei in eine andere
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- Windows Media-Format-SDK, Kopieren von Daten
- Advanced Systems Format (ASF), Kopieren von Daten
- ASF (Advanced Systems Format), Kopieren von Daten
- Streams, Kopieren von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b38a1675ac79630371fe4d3fda66d44b4b2990
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948009"
---
# <a name="copying-data-from-one-file-to-another"></a><span data-ttu-id="4a355-107">Kopieren von Daten aus einer Datei in eine andere</span><span class="sxs-lookup"><span data-stu-id="4a355-107">Copying Data from One File to Another</span></span>

<span data-ttu-id="4a355-108">Auf der grundlegendsten Ebene ist das Kopieren eines Streams aus einer ASF-Datei zu einem anderen recht unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="4a355-108">At the most basic level, copying a stream from one ASF file to another is fairly straightforward.</span></span> <span data-ttu-id="4a355-109">Beim Arbeiten mit Datenströmen aus mehreren Eingabedateien oder beim Kopieren von Streams, die Sie erstmalig Dekomprimieren und erneut codieren, müssen jedoch Probleme berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a355-109">However, there are issues to consider when working with streams from multiple input files or when copying streams that you first decompress and re-encode.</span></span>

<span data-ttu-id="4a355-110">In den folgenden Abschnitten wird das Kopieren von Datenströmen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a355-110">The following sections describe copying streams.</span></span>



| <span data-ttu-id="4a355-111">`Section`</span><span class="sxs-lookup"><span data-stu-id="4a355-111">Section</span></span>                                                                                              | <span data-ttu-id="4a355-112">Descripiton</span><span class="sxs-lookup"><span data-stu-id="4a355-112">Descripiton</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a355-113">Kopieren von Streams, ohne die Daten zu entkomprimieren</span><span class="sxs-lookup"><span data-stu-id="4a355-113">Copying Streams Without Decompressing the Data</span></span>](copying-streams-without-decompressing-the-data.md) | <span data-ttu-id="4a355-114">Beschreibt, wie Datenströme mithilfe von komprimierten Beispielen kopiert werden, um die Qualität des Inhalts beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4a355-114">Describes how to copy streams using compressed samples to preserve the quality of the content.</span></span> |
| [<span data-ttu-id="4a355-115">Kopieren von Streams mithilfe von nicht komprimierten Beispielen</span><span class="sxs-lookup"><span data-stu-id="4a355-115">Copying Streams Using Decompressed Samples</span></span>](copying-streams-using-decompressed-samples.md)         | <span data-ttu-id="4a355-116">Beschreibt die Schwierigkeiten beim Kopieren von Datenströmen mithilfe von entkomprimierten Beispielen.</span><span class="sxs-lookup"><span data-stu-id="4a355-116">Describes the difficulties in copying streams using decompressed samples.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="4a355-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a355-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a355-118">**Profil-Manager-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4a355-118">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="4a355-119">**Stream-Konfigurationsobjekt**</span><span class="sxs-lookup"><span data-stu-id="4a355-119">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="4a355-120">**Synchrones Reader-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4a355-120">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="4a355-121">**Writer-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4a355-121">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




