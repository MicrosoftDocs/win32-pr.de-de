---
title: Storages und Streams
description: Ein Speicher Objekt ist analog zu einem Dateisystem Verzeichnis.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708352"
---
# <a name="storages-and-streams"></a><span data-ttu-id="c3d2b-103">Storages und Streams</span><span class="sxs-lookup"><span data-stu-id="c3d2b-103">Storages and Streams</span></span>

<span data-ttu-id="c3d2b-104">Ein Speicher Objekt ist analog zu einem Dateisystem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-104">A storage object is analogous to a file system directory.</span></span> <span data-ttu-id="c3d2b-105">Ebenso wie ein Verzeichnis andere Verzeichnisse und Dateien enthalten kann, kann ein Speicher Objekt andere Speicher Objekte und Streamobjekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-105">Just as a directory can contain other directories and files, a storage object can contain other storage objects and stream objects.</span></span> <span data-ttu-id="c3d2b-106">Ebenso wie ein Verzeichnis verfolgt ein Speicher Objekt die Speicherorte und Größen der untergeordneten Speicher Objekte und Streamobjekte.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-106">Also like a directory, a storage object tracks the locations and sizes of the storage objects and stream objects nested beneath it.</span></span>

<span data-ttu-id="c3d2b-107">Ein Stream-Objekt entspricht dem herkömmlichen Konzept einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-107">A stream object is analogous to the traditional notion of a file.</span></span> <span data-ttu-id="c3d2b-108">Wie eine-Datei enthält ein Stream Daten, die als aufeinander folgende Byte Sequenz gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-108">Like a file, a stream contains data stored as a consecutive sequence of bytes.</span></span>

<span data-ttu-id="c3d2b-109">Eine com-Verbund Datei besteht aus einem Stamm Speicher Objekt, das mindestens ein Stream-Objekt enthält, das die systemeigenen Daten zusammen mit einem oder mehreren Speicher Objekten darstellt, die den verknüpften und eingebetteten Objekten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-109">A COM compound file consists of a root storage object containing at least one stream object representing its native data along with one or more storage objects corresponding to its linked and embedded objects.</span></span> <span data-ttu-id="c3d2b-110">Das Stamm Speicher Objekt ist einem Dateinamen in dem Dateisystem zugeordnet, in dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-110">The root storage object maps to a file name in whatever file system it happens to reside.</span></span> <span data-ttu-id="c3d2b-111">Jedes der Objekte innerhalb des Dokuments wird auch durch ein Speicher Objekt dargestellt, das mindestens ein Streamobjekt enthält, das möglicherweise auch ein oder mehrere Speicher Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-111">Each of the objects inside the document also is represented by a storage object containing one or more stream objects, and perhaps also containing one or more storage objects.</span></span> <span data-ttu-id="c3d2b-112">Auf diese Weise kann ein Dokument aus einer unbegrenzten Anzahl von in der Liste unter fallenen Objekten bestehen.</span><span class="sxs-lookup"><span data-stu-id="c3d2b-112">In this way, a document can consist of an unlimited number of nested objects.</span></span> <span data-ttu-id="c3d2b-113">Weitere Informationen finden Sie unter [Verbund Dateien](compound-files.md).</span><span class="sxs-lookup"><span data-stu-id="c3d2b-113">For more information, see [Compound Files](compound-files.md).</span></span>

 

 




