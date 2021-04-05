---
title: Strukturen-stoservice
description: Copaper verpackt die Stift Farbe, die Breite und die Koordinaten in inkdata-Strukturen und speichert Sie in einem dynamisch zugeordneten Array, das im Arbeitsspeicher verwaltet wird.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947616"
---
# <a name="structures---stoserve"></a><span data-ttu-id="80685-103">Strukturen-stoservice</span><span class="sxs-lookup"><span data-stu-id="80685-103">Structures - StoServe</span></span>

<span data-ttu-id="80685-104">Copaper verpackt die Stift Farbe, die Breite und die Koordinaten in **inkdata** -Strukturen und speichert Sie in einem dynamisch zugeordneten Array, das im Arbeitsspeicher verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="80685-104">COPaper packages the pen color, width, and coordinates into **INKDATA** structures and stores them in a dynamically allocated array that it manages in memory.</span></span>

## <a name="inkdata-structure"></a><span data-ttu-id="80685-105">Inkdata-Struktur</span><span class="sxs-lookup"><span data-stu-id="80685-105">INKDATA Structure</span></span>

<span data-ttu-id="80685-106">Im folgenden finden Sie die Deklarationen für die **inkdata** -Struktur aus "Paper. H".</span><span class="sxs-lookup"><span data-stu-id="80685-106">The following are the declarations for the **INKDATA** structure from PAPER.H.</span></span>

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

<span data-ttu-id="80685-107">Auf das dynamische Array dieser **inkdata** -Pakete wird durch m \_ painkdata, ein Member der [**iPaper**](ipaper-methods.md) -Implementierungs Klasse, verwiesen.</span><span class="sxs-lookup"><span data-stu-id="80685-107">The dynamic array of these **INKDATA** packets is pointed to by m\_paInkData, a member of the [**IPaper**](ipaper-methods.md) implementation class.</span></span> <span data-ttu-id="80685-108">Das Array wird in der **iPaper:: initpaper** -Methode mit einer anfänglichen Zuordnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="80685-108">The array is created within the **IPaper::InitPaper** method with an initial allocation.</span></span> <span data-ttu-id="80685-109">Weitere Informationen finden Sie in der **initpaper** -Methode und in der privaten nextlot-hilfsprogrammmethode der cimpipaper-Implementierung in Paper. H.</span><span class="sxs-lookup"><span data-stu-id="80685-109">For details, see the **InitPaper** method and the private NextSlot utility method of the CImpIPaper implementation in PAPER.H.</span></span> <span data-ttu-id="80685-110">Die [**inkstart**](inkstart-method.md)-, [**inkdraw**](inkdraw-method.md)-und [**inkstoppt**](cguipaper-methods.md) -Methoden verwenden nextslot, um neue Slots im Array abzurufen.</span><span class="sxs-lookup"><span data-stu-id="80685-110">The [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods use NextSlot to obtain new slots in the array.</span></span> <span data-ttu-id="80685-111">Das Array wird nach Bedarf dynamisch erweitert.</span><span class="sxs-lookup"><span data-stu-id="80685-111">The array is expanded dynamically by NextSlot as the need arises.</span></span>

<span data-ttu-id="80685-112">Der Client ruft die [**iPaper:: Erase**](ipaper-methods.md) -Methode auf, um die aktuelle Zeichnung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="80685-112">The client calls the [**IPaper::Erase**](ipaper-methods.md) method to erase the current drawing.</span></span> <span data-ttu-id="80685-113">Diese Methode weist das Array nicht neu zu. Es werden einfach alle aktuellen frei Hand Daten als inktype \_ None gekennzeichnet und der Dateiende-Index des Arrays auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="80685-113">This method does not reallocate the array; it simply marks all current ink data as INKTYPE\_NONE and resets the array's end-of-data index to zero.</span></span>

<span data-ttu-id="80685-114">Der Client ruft die [**iPaper:: Lock**](ipaper-methods.md) -Methode und die **Unlock** -Methode auf, um den Besitz des copaper zum Zeichnen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="80685-114">The client calls the [**IPaper::Lock**](ipaper-methods.md) and **Unlock** methods to manage ownership of COPaper for drawing.</span></span> <span data-ttu-id="80685-115">Diese Methoden werden bereitgestellt, um den Zugriff auf mehrere Clients auf die Zeichnung zu organisieren, die in einem freigegebenen copaper aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="80685-115">These methods are provided to organize access among multiple clients to the drawing held in a shared COPaper.</span></span>

## <a name="paper_properties-structure"></a><span data-ttu-id="80685-116">Struktur der Papier \_ Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80685-116">PAPER\_PROPERTIES Structure</span></span>

<span data-ttu-id="80685-117">Der Client ruft die [**iPaper:: Resize**](ipaper-methods.md) -Methode auf, um copaper mitzuteilen, dass der Benutzer die Größe des aktuellen Zeichnungs Papier Rechtecks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="80685-117">The client calls the [**IPaper::Resize**](ipaper-methods.md) method to tell COPaper that the user resized the current drawing paper rectangle.</span></span> <span data-ttu-id="80685-118">Diese Koordinatendaten werden in einer **Papier \_ Eigenschafts** Struktur aufbewahrt, die mit den frei Hand Daten gespeichert wird, wenn alle Papier Daten in einer Verbund Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="80685-118">This coordinate data is kept in a **PAPER\_PROPERTIES** structure, which is stored with the ink data when all the paper data is stored in a compound file.</span></span>

<span data-ttu-id="80685-119">Im folgenden finden Sie die Deklaration der **Papier \_ Eigenschaften** aus Paper. H.</span><span class="sxs-lookup"><span data-stu-id="80685-119">The following is the **PAPER\_PROPERTIES** declaration from PAPER.H.</span></span>

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

<span data-ttu-id="80685-120">Die Struktur der **Papier \_ Eigenschaften** ist so konzipiert, dass jederzeit neue frei Hand Datenformate hinzugefügt werden können, wenn die Komponente dllpaper weiterentwickelt wird.</span><span class="sxs-lookup"><span data-stu-id="80685-120">The **PAPER\_PROPERTIES** structure is designed so that new ink data formats can be added at any time as the DllPaper component evolves.</span></span> <span data-ttu-id="80685-121">Die [**iPaper**](ipaper-methods.md) -Schnittstelle ist allgemein genug, dass eine nachfolgende Version der dllpaper-Komponente ein anderes frei Hand Datenformat speichern kann, während dieselbe **iPaper** -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="80685-121">The [**IPaper**](ipaper-methods.md) interface is general enough that a subsequent version of the DllPaper component may store a different ink data format while implementing the same **IPaper** interface.</span></span> <span data-ttu-id="80685-122">Da die Methoden von **iPaper** nicht von einem bestimmten Freihand-Datenformat abhängen, kann eine neue Version der dllpaper-Komponente, die ein anderes frei Hand Datenformat unterstützt, dieselbe Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="80685-122">Because the methods of **IPaper** do not depend on a specific ink data format, a new version of the DllPaper component that does support a different ink data format can use this same interface.</span></span>

<span data-ttu-id="80685-123">Die in einer Verbund Datei gespeicherten Papiereigenschaften zeichnen die aktuelle Größe des frei Hand Daten Arrays auf.</span><span class="sxs-lookup"><span data-stu-id="80685-123">The paper properties stored in a compound file record the current size of the ink data array.</span></span> <span data-ttu-id="80685-124">Die richtige Array Größe kann dann zugewiesen werden, um die aus der Datei gelesenen frei Hand Daten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="80685-124">The proper array size can then be allocated to accommodate the ink data read from the file.</span></span>

<span data-ttu-id="80685-125">In der Struktur der **Papier \_ Eigenschaften** werden auch die Zeichnungs Rechtecke-Größe und Hintergrund Fenster Farbe der Papieroberfläche gespeichert.</span><span class="sxs-lookup"><span data-stu-id="80685-125">The **PAPER\_PROPERTIES** structure also stores the paper surface's drawing rectangle size and background window color.</span></span>

<span data-ttu-id="80685-126">Obwohl Sie nicht in den **stoservice** / -Beispielen von **stoservice** verwendet werden, können auch ein Zeichnungs Titel und ein Autorenname gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="80685-126">Though not used in the **StoServe**/**StoClien** samples, a drawing title and an author name can also be stored.</span></span>

<span data-ttu-id="80685-127">Erstellungsdatum und Datum der letzten Änderung sind nicht in diesen Papiereigenschaften enthalten, da die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle, die für den Zugriff auf Verbund Dateien verwendet wird, diese Informationen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="80685-127">Creation date and last modified dates are not included in these paper properties, because the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface used to access compound files manages this information.</span></span>

 

 




