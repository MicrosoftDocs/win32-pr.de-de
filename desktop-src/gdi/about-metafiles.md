---
description: Intern handelt es sich bei einer Metadatei um ein Array von Strukturen variabler Länge namens Metadatei-Datensätze.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Informationen zu Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753593"
---
# <a name="about-metafiles"></a><span data-ttu-id="6eacd-103">Informationen zu Metadateien</span><span class="sxs-lookup"><span data-stu-id="6eacd-103">About Metafiles</span></span>

<span data-ttu-id="6eacd-104">Intern handelt es sich bei einer Metadatei um ein Array von Strukturen variabler Länge namens *Metadatei-Datensätze*.</span><span class="sxs-lookup"><span data-stu-id="6eacd-104">Internally, a metafile is an array of variable-length structures called *metafile records*.</span></span> <span data-ttu-id="6eacd-105">Die ersten Datensätze in der Metadatei geben allgemeine Informationen an, z. b. die Auflösung des Geräts, auf dem das Bild erstellt wurde, die Abmessungen des Bilds usw.</span><span class="sxs-lookup"><span data-stu-id="6eacd-105">The first records in the metafile specify general information such as the resolution of the device on which the picture was created, the dimensions of the picture, and so on.</span></span> <span data-ttu-id="6eacd-106">Die übrigen Datensätze, die den Großteil der Metadateien bilden, entsprechen den GDI-Funktionen (Graphics Device Interface), die zum Zeichnen des Bilds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6eacd-106">The remaining records, which constitute the bulk of any metafile, correspond to the graphics device interface (GDI) functions required to draw the picture.</span></span> <span data-ttu-id="6eacd-107">Diese Datensätze werden in der Metadatendatei gespeichert, nachdem ein spezieller Metadatei-Gerätekontext erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6eacd-107">These records are stored in the metafile after a special metafile device context is created.</span></span> <span data-ttu-id="6eacd-108">Dieser Metadatei-Gerätekontext wird dann für alle Zeichnungsvorgänge verwendet, die zum Erstellen des Bilds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6eacd-108">This metafile device context is then used for all drawing operations required to create the picture.</span></span> <span data-ttu-id="6eacd-109">Wenn das System eine GDI-Funktion verarbeitet, die einem metadateidc zugeordnet ist, wird die Funktion in die entsprechenden Daten konvertiert, und diese Daten werden in einem Datensatz gespeichert, der an die Metadatendatei angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="6eacd-109">When the system processes a GDI function associated with a metafile DC, it converts the function into the appropriate data and stores this data in a record appended to the metafile.</span></span>

<span data-ttu-id="6eacd-110">Nachdem ein Bild abgeschlossen und der letzte Datensatz in der Metadatei gespeichert wurde, können Sie die Metadatendatei an eine andere Anwendung übergeben, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="6eacd-110">After a picture is complete and the last record is stored in the metafile, you can pass the metafile to another application by:</span></span>

-   <span data-ttu-id="6eacd-111">Verwenden der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="6eacd-111">Using the clipboard</span></span>
-   <span data-ttu-id="6eacd-112">Einbetten in eine andere Datei</span><span class="sxs-lookup"><span data-stu-id="6eacd-112">Embedding it within another file</span></span>
-   <span data-ttu-id="6eacd-113">Speichern auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="6eacd-113">Storing it on disk</span></span>
-   <span data-ttu-id="6eacd-114">Wiederholte Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="6eacd-114">Playing it repeatedly</span></span>

<span data-ttu-id="6eacd-115">Eine Metadatei wird wieder *gegeben* , wenn die zugehörigen Datensätze in Geräte Befehle konvertiert und vom entsprechenden Gerät verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6eacd-115">A metafile is *played* when its records are converted to device commands and processed by the appropriate device.</span></span>

<span data-ttu-id="6eacd-116">Es gibt zwei Arten von Metadateien:</span><span class="sxs-lookup"><span data-stu-id="6eacd-116">There are two types of metafiles:</span></span>

-   [<span data-ttu-id="6eacd-117">Metadateien mit erweitertem Format</span><span class="sxs-lookup"><span data-stu-id="6eacd-117">Enhanced-format metafiles</span></span>](enhanced-format-metafiles.md)
-   [<span data-ttu-id="6eacd-118">Metadateien im Windows-Format</span><span class="sxs-lookup"><span data-stu-id="6eacd-118">Windows-format metafiles</span></span>](windows-format-metafiles.md)

 

 



