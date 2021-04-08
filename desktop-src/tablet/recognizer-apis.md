---
description: 'Die Erkennungs Punkte:'
ms.assetid: d7c694a2-0da6-4172-b434-2b0f94e1b649
title: Erkennungs Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e193b6098f6d82751951d1a39630ad30023c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050530"
---
# <a name="recognizer-reference"></a><span data-ttu-id="3ddc1-103">Erkennungs Referenz</span><span class="sxs-lookup"><span data-stu-id="3ddc1-103">Recognizer Reference</span></span>

<span data-ttu-id="3ddc1-104">Die Erkennungs Punkte:</span><span class="sxs-lookup"><span data-stu-id="3ddc1-104">The recognizer handles:</span></span>

-   <span data-ttu-id="3ddc1-105">Bestimmen Sie, welche erkenners auf dem Computer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-105">Determine which recognizers are available on the computer.</span></span>
-   <span data-ttu-id="3ddc1-106">Identifizieren Sie die zu verwendende Erkennung.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-106">Identify which recognizer to use.</span></span>
-   <span data-ttu-id="3ddc1-107">Erstellen Sie einen Erkennungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-107">Create a recognizer context.</span></span>
-   <span data-ttu-id="3ddc1-108">Abrufen der Erkennungsergebnisse und der Alternativen.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-108">Retrieve recognizer results and alternates.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ddc1-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3ddc1-109">In This Section</span></span>



| <span data-ttu-id="3ddc1-110">Thema</span><span class="sxs-lookup"><span data-stu-id="3ddc1-110">Topic</span></span>                                                      | <span data-ttu-id="3ddc1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ddc1-111">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ddc1-112">Hrecoalt-handle</span><span class="sxs-lookup"><span data-stu-id="3ddc1-112">HRECOALT Handle</span></span>](hrecoalt-handle.md)                     | <span data-ttu-id="3ddc1-113">Ruft die alternativen Zeichen folgen-und Eigenschaftswerte ab, z. b. Vertrauensgrad und Metriken.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-113">Retrieves the alternate string and property values, such as confidence level and metrics.</span></span><br/>                                                                  |
| [<span data-ttu-id="3ddc1-114">Hrecocontext-handle</span><span class="sxs-lookup"><span data-stu-id="3ddc1-114">HRECOCONTEXT Handle</span></span>](hrecocontext-handle.md)             | <span data-ttu-id="3ddc1-115">Fügt dem kontextfrei Hand Eingaben, führt die frei Handerkennung durch und ruft das Erkennungs Ergebnis ab und wechselt.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-115">Adds ink to the context, performs ink recognition, and retrieves the recognition result and alternates.</span></span><br/>                                                    |
| [<span data-ttu-id="3ddc1-116">Herkenzer-handle</span><span class="sxs-lookup"><span data-stu-id="3ddc1-116">HRECOGNIZER Handle</span></span>](hrecognizer-handle.md)               | <span data-ttu-id="3ddc1-117">Erstellt einen Erkennungs Kontext, ruft seine Attribute und Eigenschaften ab und bestimmt, welche Paket Eigenschaften die Erkennung zum Durchführen der Erkennung benötigt.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-117">Creates a recognizer context, retrieves its attributes and properties, and determines which packet properties the recognizer needs to perform recognition.</span></span><br/> |
| [<span data-ttu-id="3ddc1-118">Hrecowordlist-handle</span><span class="sxs-lookup"><span data-stu-id="3ddc1-118">HRECOWORDLIST Handle</span></span>](hrecowordlist-handle.md)           | <span data-ttu-id="3ddc1-119">Verwaltet eine Wortliste, die Sie an einen Erkennungs Kontext anfügen.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-119">Manages a word list that you attach to a recognizer context.</span></span> <span data-ttu-id="3ddc1-120">Diese Liste verbessert die Erkennungsergebnisse.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-120">This list improves the recognition results.</span></span><br/>                                                   |
| [<span data-ttu-id="3ddc1-121">Erkennungsenumerationen</span><span class="sxs-lookup"><span data-stu-id="3ddc1-121">Recognizer Enumerations</span></span>](recognizer-api-enumerations.md) | <span data-ttu-id="3ddc1-122">Beschreibt die Enumerationstypen der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-122">Describes the recognizer enumeration types.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="3ddc1-123">Erkennungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="3ddc1-123">Recognizer Structures</span></span>](recognizer-api-structures.md)     | <span data-ttu-id="3ddc1-124">Beschreibt die Erkennungs Strukturen.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-124">Describes the recognizer structures.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3ddc1-125">Erkennungs-GUIDs</span><span class="sxs-lookup"><span data-stu-id="3ddc1-125">Recognizer GUIDs</span></span>](recognizer-guids.md)                   | <span data-ttu-id="3ddc1-126">Gibt den Typ der Eigenschaft für Paket Eigenschaften und Erkennungs Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="3ddc1-126">Specifies the type of property for packet properties and recognizer properties.</span></span><br/>                                                                            |



 

 

 




