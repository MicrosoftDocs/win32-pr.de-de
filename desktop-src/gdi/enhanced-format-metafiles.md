---
description: Metadatendateien Enhanced-Format
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Metadatendateien Enhanced-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978625"
---
# <a name="enhanced-format-metafiles"></a><span data-ttu-id="6f83d-103">Metadatendateien Enhanced-Format</span><span class="sxs-lookup"><span data-stu-id="6f83d-103">Enhanced-Format Metafiles</span></span>

<span data-ttu-id="6f83d-104">Die *Metadatei mit erweitertem Format* besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="6f83d-104">The *enhanced-format metafile* consists of the following elements:</span></span>

-   <span data-ttu-id="6f83d-105">Ein-Header</span><span class="sxs-lookup"><span data-stu-id="6f83d-105">A header</span></span>
-   <span data-ttu-id="6f83d-106">Eine Tabelle mit Handles für GDI-Objekte</span><span class="sxs-lookup"><span data-stu-id="6f83d-106">A table of handles to GDI objects</span></span>
-   <span data-ttu-id="6f83d-107">Eine private Palette</span><span class="sxs-lookup"><span data-stu-id="6f83d-107">A private palette</span></span>
-   <span data-ttu-id="6f83d-108">Ein Array von Metadatei-Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="6f83d-108">An array of metafile records</span></span>

<span data-ttu-id="6f83d-109">Erweiterte Metadatendateien bieten echte Geräteunabhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="6f83d-109">Enhanced metafiles provide true device independence.</span></span> <span data-ttu-id="6f83d-110">Sie können sich das Bild, das in einer erweiterten Metadatei gespeichert ist, als "Momentaufnahme" der Videoanzeige vorstellen, die zu einem bestimmten Zeitpunkt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f83d-110">You can think of the picture stored in an enhanced metafile as a "snapshot" of the video display taken at a particular moment.</span></span> <span data-ttu-id="6f83d-111">Diese "Momentaufnahme" behält die Dimensionen unabhängig davon bei, wo Sie auf einem Drucker, einem Plotter, dem Desktop oder im Client Bereich einer beliebigen Anwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f83d-111">This "snapshot" maintains its dimensions no matter where it appears on a printer, a plotter, the desktop, or in the client area of any application.</span></span>

<span data-ttu-id="6f83d-112">Sie können Erweiterte Metadateien zum Speichern eines Bilds verwenden, das mit den GDI-Funktionen (einschließlich neuer Pfad-und Transformations Funktionen) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f83d-112">You can use enhanced metafiles to store a picture created by using the GDI functions (including new path and transformation functions).</span></span> <span data-ttu-id="6f83d-113">Da das erweiterte Metadatei-Format standardisiert ist, können Bilder, die in diesem Format gespeichert sind, aus einer Anwendung in eine andere kopiert werden. und da die Bilder wirklich Geräte unabhängig sind, gewährleisten Sie, dass Sie Ihre Form und den Anteil an allen Ausgabegeräten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="6f83d-113">Because the enhanced metafile format is standardized, pictures that are stored in this format can be copied from one application to another; and, because the pictures are truly device independent, they are guaranteed to maintain their shape and proportion on any output device.</span></span>

-   [<span data-ttu-id="6f83d-114">Erweiterte Metafile-Datensätze</span><span class="sxs-lookup"><span data-stu-id="6f83d-114">Enhanced Metafile Records</span></span>](enhanced-metafile-records.md)
-   [<span data-ttu-id="6f83d-115">Erweiterte metadateierstellung</span><span class="sxs-lookup"><span data-stu-id="6f83d-115">Enhanced Metafile Creation</span></span>](enhanced-metafile-creation.md)
-   [<span data-ttu-id="6f83d-116">Erweiterte metadateivorgänge</span><span class="sxs-lookup"><span data-stu-id="6f83d-116">Enhanced Metafile Operations</span></span>](enhanced-metafile-operations.md)

 

 



