---
description: Zusätzlich zum Erkennen von Text können Erkennungs Tools eine Klasse verwandter Objekte erkennen.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Objekterkenzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960287"
---
# <a name="object-recognizers"></a><span data-ttu-id="46abc-103">Objekterkenzer</span><span class="sxs-lookup"><span data-stu-id="46abc-103">Object Recognizers</span></span>

<span data-ttu-id="46abc-104">Zusätzlich zum Erkennen von Text können Erkennungs Tools eine Klasse verwandter Objekte erkennen.</span><span class="sxs-lookup"><span data-stu-id="46abc-104">In addition to recognizing text, recognizers can recognize a class of related objects.</span></span> <span data-ttu-id="46abc-105">Objekt erkenmentatoren erkennen allgemeine Formen entsprechend ihrem Zweck.</span><span class="sxs-lookup"><span data-stu-id="46abc-105">Object recognizers recognize general shapes, according to their purpose.</span></span> <span data-ttu-id="46abc-106">Objekterkenatoren werden verwendet, um Folgendes zu erkennen:</span><span class="sxs-lookup"><span data-stu-id="46abc-106">Object recognizers are used to recognize:</span></span>

-   <span data-ttu-id="46abc-107">Musik Notizen</span><span class="sxs-lookup"><span data-stu-id="46abc-107">Musical notes</span></span>
-   <span data-ttu-id="46abc-108">Geometrische Formen</span><span class="sxs-lookup"><span data-stu-id="46abc-108">Geometric shapes</span></span>
-   <span data-ttu-id="46abc-109">Mathematische Gleichungen</span><span class="sxs-lookup"><span data-stu-id="46abc-109">Math equations</span></span>
-   <span data-ttu-id="46abc-110">Flussdiagramm Elemente</span><span class="sxs-lookup"><span data-stu-id="46abc-110">Flow chart elements</span></span>

<span data-ttu-id="46abc-111">In der Regel befinden sich die Objekte, die von einer solchen Erkennung erkannt werden, in einer zweidimensionalen räumlichen oder funktionalen Beziehung zueinander.</span><span class="sxs-lookup"><span data-stu-id="46abc-111">Usually, the objects that are recognized by such a recognizer are in a two-dimensional spatial or functional relationship with each other.</span></span> <span data-ttu-id="46abc-112">Innerhalb der komplexen Beziehungen in einer mathematischen Gleichung kann eine Erkennung z. b. unterschiedliche Ergebnisse für eine Obergrenze für eine definitive Ganzzahl zurückgeben, im Gegensatz zu einem Zähler in einem Bruchteil.</span><span class="sxs-lookup"><span data-stu-id="46abc-112">For example, within the complex relationships in a math equation, a recognizer can return different results for an upper limit on a definite integral as opposed to a numerator in a fraction.</span></span>

<span data-ttu-id="46abc-113">Aufgrund der allgemeinen Natur dieser Beziehungen ist es äußerst schwierig, den Satz von Schnittstellen zu definieren, der für jede Objekterkennung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="46abc-113">Because of the very general nature of these relationships, it is extremely difficult to define the set of interfaces that will work for every object recognizer.</span></span>

<span data-ttu-id="46abc-114">Die Tablet PC-Technologie stellt ein grundlegendes Framework für Objekt erkenzer in der verwalteten Bibliothek und in den Automatisierungs Schnittstellen bereit.</span><span class="sxs-lookup"><span data-stu-id="46abc-114">The Tablet PC Technology provides a basic framework for object recognizers in the Managed Library and Automation interfaces.</span></span> <span data-ttu-id="46abc-115">Sie müssen jedoch benutzerdefinierte Schnittstellen entwickeln, die komplexe räumliche Beziehungen zwischen erkannten Objekten für jede Objekterkennung beschreiben.</span><span class="sxs-lookup"><span data-stu-id="46abc-115">However, you must develop custom interfaces that describe complex spatial relationships between recognized objects for each object recognizer.</span></span> <span data-ttu-id="46abc-116">Speziell für Objekt erkennenungen stellt die Plattform das grundlegende [**Erkennungs**](inkrecognizercontext-class.md) Element-Objekt bereit, [**um das frei Hand Objekt dem**](inkdisp-class.md) Erkennungs Kontext zuzuordnen und den Erkennungs Modul zum Durchführen der Erkennung aufzurufenden.</span><span class="sxs-lookup"><span data-stu-id="46abc-116">Specifically, for object recognizers, the platform provides the basic [**RecognizerContext**](inkrecognizercontext-class.md) object for associating the [**Ink**](inkdisp-class.md) object with the recognizer context and for calling the recognizer to perform the recognition.</span></span>

 

 



