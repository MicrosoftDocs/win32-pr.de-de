---
description: Die FOURCCMap-Klasse ermöglicht die Konvertierung zwischen GUID-Medienuntertypen und 32-Bit-Medientags im alten Format.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908858"
---
# <a name="fourccmap-class"></a><span data-ttu-id="0a2d2-103">FOURCCMap-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a2d2-103">FOURCCMap class</span></span>

![fourccmap-Klassenhierarchie](images/fourcc01.png)

<span data-ttu-id="0a2d2-105">Die **FOURCCMap-Klasse** ermöglicht die Konvertierung zwischen **GUID-Medienuntertypen** und 32-Bit-Medientags im alten Format. </span><span class="sxs-lookup"><span data-stu-id="0a2d2-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="0a2d2-106">In den ursprünglichen Windows-Multimedia-APIs wurden Medientypen mit 32-Bit-Werten markiert, die aus vier 8-Bit-Zeichen erstellt wurden und als **FOURCC** s bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="0a2d2-107">DirectShow-Medientypen verfügen über **GUID-S** für den Untertyp, auch weil diese einfacher zu erstellen sind (die Erstellung einer neuen **FOURCC** erfordert die Registrierung bei Microsoft).</span><span class="sxs-lookup"><span data-stu-id="0a2d2-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="0a2d2-108">Da **FOURCC-s** eindeutig sind, wurde eine 1:1-Zuordnung ermöglicht, indem ein Bereich von 4.000 Millionen **GUID-S** zugeordnet wurde, die **FOURCC** s darstellen.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="0a2d2-109">Bei diesem Bereich handelt es sich um alle **GUIDs** des Formulars:</span><span class="sxs-lookup"><span data-stu-id="0a2d2-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="0a2d2-110">Diese Klasse vereinfacht die Konvertierung zwischen **GUID** s und **FOURCC** s.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="0a2d2-111">Dies dient nur zur Kompatibilität.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-111">This is for compatibility only.</span></span> <span data-ttu-id="0a2d2-112">Es wird empfohlen, alle neuen Medienuntertypen durch **GUID-S** darzustellen, die von Guidgen.exe oder einem ähnlichen Tool erstellt wurden, und nicht durch Zuordnung von **FOURCC** s.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="0a2d2-113">Das -Objekt wird von einer **GUID** abgeleitet, ohne zusätzliche Datenmember, und kann in eine **GUID** umgerechnet werden.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="0a2d2-114">Dem Objekt kann zur Erstellungszeit eine **FOURCC** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="0a2d2-115">Der Standardkonstruktor initialisiert **FOURCC** auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0a2d2-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="0a2d2-116">Die [**Methoden GetFOURCC**](fourccmap-getfourcc.md) und [**SetFOURCC**](fourccmap-setfourcc.md) überprüfen nicht, ob die festen Teile der **GUID** dem **FOURCC-Bereich** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="0a2d2-117">Wenn Sie also einen Zeiger auf eine **GUID** in einen Zeiger auf eine **FOURCC-Datei** umgewandelt und dann das **FELD FOURCC** festlegen oder abrufen, müssen Sie auch separat überprüfen, ob sich die **GUID** innerhalb des **FOURCC-Bereichs** befindet.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="0a2d2-118">Elementfunktionen</span><span class="sxs-lookup"><span data-stu-id="0a2d2-118">Member Functions</span></span>



| <span data-ttu-id="0a2d2-119">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="0a2d2-119">Label</span></span> | <span data-ttu-id="0a2d2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0a2d2-120">Value</span></span> |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="0a2d2-121">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="0a2d2-121">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="0a2d2-122">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="0a2d2-123">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="0a2d2-123">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="0a2d2-124">Ruft **fourcc aus einem** **FOURCCMap-Objekt** ab.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-124">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="0a2d2-125">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="0a2d2-125">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="0a2d2-126">Legt den **FOURCC-Teil** des **FOURCCMap-Objekts** fest.</span><span class="sxs-lookup"><span data-stu-id="0a2d2-126">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



