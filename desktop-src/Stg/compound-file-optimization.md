---
title: Optimierung der Verbund Datei
description: Der asynchrone Speicher ermöglicht Anwendungen das genaue Layout von Verbund Dateien, sodass Daten in der Reihenfolge verfügbar sind, in der Sie von Anwendungen benötigt werden.
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- Optimierung der Verbund Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708201"
---
# <a name="compound-file-optimization"></a><span data-ttu-id="9bc3b-104">Optimierung der Verbund Datei</span><span class="sxs-lookup"><span data-stu-id="9bc3b-104">Compound File Optimization</span></span>

<span data-ttu-id="9bc3b-105">Der asynchrone Speicher ermöglicht Anwendungen das genaue Layout von Verbund Dateien, sodass Daten in der Reihenfolge verfügbar sind, in der Sie von Anwendungen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-105">Asynchronous storage enables applications to precisely layout compound files so that data is available in the order in which applications will require it.</span></span> <span data-ttu-id="9bc3b-106">Wenn eine Anwendung nur einen Teil der Daten benötigt, um eine erste Seite mit Informationen anzuzeigen, können diese Daten am Anfang der Datei platziert werden, auch wenn Sie logisch am Ende eines Streams angeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-106">If an application requires only part of its data to display a first page of information, this data can be placed at the beginning of the file, even if it logically resides at the end of a stream.</span></span> <span data-ttu-id="9bc3b-107">Daten aus unterschiedlichen Streams können verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-107">Data from different streams can be interleaved.</span></span> <span data-ttu-id="9bc3b-108">Audiodaten und Videodaten können z. b. verschachtelt werden, damit nachfolgende Lesevorgänge beide gleichzeitig abgerufen werden. Dies ist eine Anforderung für Multimedia-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-108">Audio and video data, for example, can be interleaved so that subsequent read operations retrieve both simultaneously, a requirement for multimedia applications.</span></span>

<span data-ttu-id="9bc3b-109">[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) kann verwendet werden, um eine DOCFILE-Datei zu erstellen und so die Leistung in den meisten Szenarien zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-109">[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) can be used to layout a docfile, thus improving performance in most scenarios.</span></span>

 

 




