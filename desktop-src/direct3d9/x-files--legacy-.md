---
description: Das x-Dateiformat bezieht sich auf Dateien mit der Dateinamenerweiterung ". X".
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: X-Dateien (Legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0e4ce85a0ff5ecbc2f680f55b8162d13bc1042
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860083"
---
# <a name="x-files-legacy-direct3d-9"></a><span data-ttu-id="3e3e7-103">X-Dateien (Legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e3e7-103">X Files (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="3e3e7-104">Das x-Dateiformat bezieht sich auf Dateien mit der Dateinamenerweiterung ". X".</span><span class="sxs-lookup"><span data-stu-id="3e3e7-104">The X file format refers to files with the .x file name extension.</span></span> <span data-ttu-id="3e3e7-105">X-Dateien wurden mit DirectX 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-105">X files were introduced with DirectX 2.0.</span></span> <span data-ttu-id="3e3e7-106">Anschließend wurde eine binäre Version dieses Formats mit DirectX 3,0 veröffentlicht, das auch in dieser Dokumentation beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-106">A binary version of this format was subsequently released with DirectX 3.0, which is also described in this documentation.</span></span> <span data-ttu-id="3e3e7-107">In DirectX 6,0 wurden Schnittstellen und Methoden eingeführt, die das Lesen aus und Schreiben in x-Dateien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-107">DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files.</span></span>

<span data-ttu-id="3e3e7-108">X-Dateien stellen ein vorlagengesteuerte Format bereit, das die Speicherung von Meshes, Texturen, Animationen und benutzerdefinierbaren Objekten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-108">X files provide a template-driven format that enables the storage of meshes, textures, animations, and user-definable objects.</span></span> <span data-ttu-id="3e3e7-109">Mithilfe der Unterstützung für Animations Sätze können Sie in Echtzeit vordefinierte Pfade für die Wiedergabe speichern.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-109">Support for animation sets enables you to store predefined paths for playback in real time.</span></span> <span data-ttu-id="3e3e7-110">Instanziierung und Hierarchien werden ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-110">Instancing and hierarchies are also supported.</span></span> <span data-ttu-id="3e3e7-111">Die Instanziierung ermöglicht mehrere Verweise auf ein Objekt, z. b. ein Mesh, während die Daten nur einmal pro Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-111">Instancing enables multiple references to an object, such as a mesh, while storing its data only once per file.</span></span> <span data-ttu-id="3e3e7-112">Hierarchien werden verwendet, um Beziehungen zwischen Datensätzen auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-112">Hierarchies are used to express relationships between data records.</span></span>

<span data-ttu-id="3e3e7-113">Das Dateiformat. x stellt Low-Level-Daten Primitive bereit, bei denen Anwendungen auf höherer Ebene über Vorlagen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-113">The .x file format provides low-level data primitives on which applications define higher-level primitives through templates.</span></span>

<span data-ttu-id="3e3e7-114">Dreidimensionale Modelle, die in den dreidimensionalen drei-GB-oder Alias \| Wellen-Anwendungen von Wavefront erstellt werden, können mit den DirectX-Erweiterungen für den Alias Maya in x-Dateien konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-114">Three-dimensional models created in Discreet's 3ds max or Alias\|Wavefront's Maya applications can be converted to .x files with the DirectX Extensions for Alias Maya.</span></span>

<span data-ttu-id="3e3e7-115">In diesem Abschnitt wird die Struktur von x-Dateien beschrieben und erläutert, wie Sie in Ihren Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e3e7-115">This section describes the structure of .x files and how to use them in your applications.</span></span> <span data-ttu-id="3e3e7-116">Die Informationen sind in folgende Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="3e3e7-116">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="3e3e7-117">Laden einer X-Datei (Legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e3e7-117">Loading an X File (Legacy) (Direct3D 9)</span></span>](loading-an-x-file--legacy-.md)
-   [<span data-ttu-id="3e3e7-118">Speichern in einer X-Datei (Legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e3e7-118">Saving to an X File (Legacy) (Direct3D 9)</span></span>](saving-to-an-x-file--legacy-.md)
-   [<span data-ttu-id="3e3e7-119">Definieren eines einfachen Cubes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e3e7-119">Defining a Simple Cube (Direct3D 9)</span></span>](defining-a-simple-cube.md)
-   [<span data-ttu-id="3e3e7-120">Hinzufügen von Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e3e7-120">Adding Textures (Direct3D 9)</span></span>](adding-textures.md)
-   [<span data-ttu-id="3e3e7-121">Hinzufügen von Frames und Animationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e3e7-121">Adding Frames and Animations (Direct3D 9)</span></span>](adding-frames-and-animations.md)

<span data-ttu-id="3e3e7-122">Weitere Informationen zum Format der x-Datei finden Sie unter [Referenz zur x-Datei](dx9-graphics-reference-d3dx-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="3e3e7-122">For more information about the .x file format, see [X File Reference](dx9-graphics-reference-d3dx-x-file.md).</span></span>

<span data-ttu-id="3e3e7-123">Weitere Informationen zur x-Datei-API finden Sie unter [Referenz zu x-Dateien (Legacy)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="3e3e7-123">For more information about the .x file API, see [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e3e7-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e3e7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e3e7-125">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="3e3e7-125">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



