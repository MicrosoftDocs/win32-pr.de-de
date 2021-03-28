---
description: Zum Bearbeiten eines Bilds, das in einer erweiterten Metadatei gespeichert ist, muss eine Anwendung die im folgenden Verfahren beschriebenen Aufgaben ausführen.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Bearbeiten einer erweiterten Metadatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130784"
---
# <a name="editing-an-enhanced-metafile"></a><span data-ttu-id="0234d-103">Bearbeiten einer erweiterten Metadatei</span><span class="sxs-lookup"><span data-stu-id="0234d-103">Editing an Enhanced Metafile</span></span>

<span data-ttu-id="0234d-104">Zum Bearbeiten eines Bilds, das in einer erweiterten Metadatei gespeichert ist, muss eine Anwendung die im folgenden Verfahren beschriebenen Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="0234d-104">To edit a picture stored in an enhanced metafile, an application must perform the tasks described in the following procedure.</span></span>

<span data-ttu-id="0234d-105">**So bearbeiten Sie ein Bild, das in einer erweiterten Metadatei gespeichert ist**</span><span class="sxs-lookup"><span data-stu-id="0234d-105">**To edit a picture stored in an enhanced metafile**</span></span>

1.  <span data-ttu-id="0234d-106">Verwenden Sie Treffer Tests, um die Cursor Koordinaten zu erfassen und die Position des Objekts (Linie, Bogen, Rechteck, Ellipse, Polygon oder unregelmäßige Form) abzurufen, die der Benutzer ändern möchte.</span><span class="sxs-lookup"><span data-stu-id="0234d-106">Use hit-testing to capture the cursor coordinates and retrieve the position of the object (line, arc, rectangle, ellipse, polygon, or irregular shape) that the user wants to alter.</span></span>
2.  <span data-ttu-id="0234d-107">Konvertieren Sie diese Koordinaten in logische (oder weltweite) Einheiten.</span><span class="sxs-lookup"><span data-stu-id="0234d-107">Convert these coordinates to logical (or world) units.</span></span>
3.  <span data-ttu-id="0234d-108">Nennen Sie die [**enumenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) -Funktion, und untersuchen Sie jeden Metadateidatensatz.</span><span class="sxs-lookup"><span data-stu-id="0234d-108">Call the [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) function and examine each metafile record.</span></span>
4.  <span data-ttu-id="0234d-109">Bestimmen Sie, ob ein bestimmter Datensatz einer GDI-Zeichnungs Funktion entspricht.</span><span class="sxs-lookup"><span data-stu-id="0234d-109">Determine whether a given record corresponds to a GDI drawing function.</span></span>
5.  <span data-ttu-id="0234d-110">Wenn dies der Fall ist, stellen Sie fest, ob die im Datensatz gespeicherten Koordinaten der Zeile, dem Bogen, der Ellipse oder einem anderen Grafik Element entsprechen, das die vom Benutzer angegebenen Koordinaten überschneidet.</span><span class="sxs-lookup"><span data-stu-id="0234d-110">If it does, determine whether the coordinates stored in the record correspond to the line, arc, ellipse, or other graphics element that intersects the coordinates specified by the user.</span></span>
6.  <span data-ttu-id="0234d-111">Wenn Sie den Datensatz ermitteln, der der Ausgabe entspricht, die der Benutzer ändern möchte, löschen Sie das Objekt auf dem Bildschirm, das dem ursprünglichen Datensatz entspricht.</span><span class="sxs-lookup"><span data-stu-id="0234d-111">Upon finding the record that corresponds to the output that the user wants to alter, erase the object on the screen that corresponds to the original record.</span></span>
7.  <span data-ttu-id="0234d-112">Löschen Sie den entsprechenden Datensatz aus der Metadatendatei, und speichern Sie einen Zeiger auf den Speicherort.</span><span class="sxs-lookup"><span data-stu-id="0234d-112">Delete the corresponding record from the metafile, saving a pointer to its location.</span></span>
8.  <span data-ttu-id="0234d-113">Ermöglicht dem Benutzer das erneute zeichnen oder Ersetzen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0234d-113">Permit the user to redraw or replace the object.</span></span>
9.  <span data-ttu-id="0234d-114">Konvertieren Sie die GDI-Funktionen, die zum Zeichnen des neuen Objekts verwendet werden, in einen oder mehrere Enhanced-Metafile-Datensätze.</span><span class="sxs-lookup"><span data-stu-id="0234d-114">Convert the GDI functions used to draw the new object into one or more enhanced-metafile records.</span></span>
10. <span data-ttu-id="0234d-115">Speichern Sie diese Datensätze in der erweiterten Metadatei.</span><span class="sxs-lookup"><span data-stu-id="0234d-115">Store these records in the enhanced metafile.</span></span>

 

 



