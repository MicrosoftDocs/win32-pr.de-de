---
description: 'Berücksichtigen Sie Folgendes, wenn Sie entscheiden, wann und wie das Divider-Objekt in einer Anwendung verwendet werden soll:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Weitere Überlegungen zu Trenn Punkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216974"
---
# <a name="other-divider-considerations"></a><span data-ttu-id="70995-103">Weitere Überlegungen zu Trenn Punkten</span><span class="sxs-lookup"><span data-stu-id="70995-103">Other Divider Considerations</span></span>

<span data-ttu-id="70995-104">Berücksichtigen Sie Folgendes, wenn Sie entscheiden, wann und wie das [**Divider**](inkdivider-class.md) -Objekt in einer Anwendung verwendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="70995-104">Consider the following when deciding when and how to use the [**Divider**](inkdivider-class.md) object in an application:</span></span>

-   <span data-ttu-id="70995-105">Das [**Divider**](inkdivider-class.md) -Objekt ist so konzipiert, dass Zeichnungen und Handschrift Blöcke getrennt werden, aber keine höheren Ebenen der Struktur erkannt werden, z. b. Tabellen oder Spalten.</span><span class="sxs-lookup"><span data-stu-id="70995-105">The [**Divider**](inkdivider-class.md) object is designed to separate drawings and blocks of handwriting, but not to recognize higher levels of structure, such as tables or columns.</span></span>
-   <span data-ttu-id="70995-106">Das [**Divider**](inkdivider-class.md) -Objekt stellt keine Schnittstellen speziell für die Korrektur der Ergebnisse der Layoutanalyse bereit.</span><span class="sxs-lookup"><span data-stu-id="70995-106">The [**Divider**](inkdivider-class.md) object does not provide interfaces specifically for correction of results of layout analysis.</span></span>
-   <span data-ttu-id="70995-107">Die Verwendung des Timeouts und der Anzahl der hubheuristiken zum Hinzufügen oder Entfernen mehrerer Striche gleichzeitig aus den Strichen im [**Divider**](inkdivider-class.md) -Objekt kann die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="70995-107">The use of timeout and number of stroke heuristics to add or remove multiple strokes at a time from the strokes in the [**Divider**](inkdivider-class.md) object may improve performance.</span></span>

## <a name="reanalysis-considerations"></a><span data-ttu-id="70995-108">Überlegungen zur erneuten Analyse</span><span class="sxs-lookup"><span data-stu-id="70995-108">Reanalysis Considerations</span></span>

<span data-ttu-id="70995-109">Wenn Sie in Erwägung ziehen, das [**Divider**](inkdivider-class.md) -Objekt in einer Anwendung zu verwenden, **in der möglich** erweise große Mengen von frei Hand Eingaben erneut analysiert werden müssen, beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="70995-109">If you are considering using the [**Divider**](inkdivider-class.md) object in an application where the **Divider** object may have to reanalyze large amounts of ink, keep the following in mind.</span></span>

### <a name="retaining-copies-of-ink-and-strokes"></a><span data-ttu-id="70995-110">Beibehalten von Kopien von frei Hand Eingaben und Strichen</span><span class="sxs-lookup"><span data-stu-id="70995-110">Retaining Copies of Ink and Strokes</span></span>

<span data-ttu-id="70995-111">Eine Anwendung kann Kopien von " [**Ink**](inkdisp-class.md) "-und " [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) "-Objekten für Anwendungs Elemente aufbewahren, die später in der Anwendungs Sitzung wieder besucht werden können.</span><span class="sxs-lookup"><span data-stu-id="70995-111">An application can keep copies of [**Ink**](inkdisp-class.md) and [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) objects for application elements that may be revisited later in the application session.</span></span> <span data-ttu-id="70995-112">Dadurch entfällt die Notwendigkeit, das **Ink** -Objekt erneut zu analysieren, wenn der Benutzer zum-Element zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="70995-112">This eliminates the need to reanalyze the **Ink** object if the user returns to the element.</span></span> <span data-ttu-id="70995-113">Bei diesem Ansatz wird der Arbeitsspeicher für eine bessere Leistung betrieben.</span><span class="sxs-lookup"><span data-stu-id="70995-113">This approach trades off memory for better performance.</span></span>

### <a name="data-reduction-heuristics"></a><span data-ttu-id="70995-114">Heuristik zur Daten Reduzierung</span><span class="sxs-lookup"><span data-stu-id="70995-114">Data Reduction Heuristics</span></span>

<span data-ttu-id="70995-115">Möglicherweise sind Sie in der Lage, die Analyseergebnisse als Anwendungsdaten aufzuzeichnen und Heuristik zu implementieren, um zu bestimmen, wann ein Satz von Strichen erneut analysiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="70995-115">You may be able to record the analysis results as application data, and implement heuristics to determine when to reanalyze a set of strokes.</span></span> <span data-ttu-id="70995-116">Diese Vorgehensweise würde die Notwendigkeit verringern, alle frei Hand Eingaben in der Anwendung zwischen Anwendungs Sitzungen erneut zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="70995-116">This practice would reduce the need to reanalyze all the ink in the application between application sessions.</span></span> <span data-ttu-id="70995-117">Sie müssen jedoch sorgfältig vorgehen, um strukturelle Elementgrenzen beizubehalten oder alle Striche für betroffene Elemente erneut zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="70995-117">However, care must be taken to preserve structural element boundaries or to reanalyze all the strokes for affected elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70995-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70995-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70995-119">**InkDivider-Klasse**</span><span class="sxs-lookup"><span data-stu-id="70995-119">**InkDivider Class**</span></span>](inkdivider-class.md)
</dt> <dt>

<span data-ttu-id="70995-120">[Microsoft. Ink. Divider-Klasse](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="70995-120">[Microsoft.Ink.Divider Class](/previous-versions/ms583616(v=vs.100))</span></span>
</dt> </dl>

 

 
