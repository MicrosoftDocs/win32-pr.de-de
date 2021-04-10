---
description: Der primäre Sensor Datentyp für Umgebungslichtsensoren ist Beleuchtungs Kraft in Lux (dünn/Quadratmeter). Die in diesem Thema beschriebenen Prinzipien basieren auf der Aufnahme von Lux-Werten als Eingabe und der Reaktion auf diese Daten in einem Programm.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Verstehen und Interpretieren von Lux-Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042598"
---
# <a name="understanding-and-interpreting-lux-values"></a><span data-ttu-id="2e20b-104">Verstehen und Interpretieren von Lux-Werten</span><span class="sxs-lookup"><span data-stu-id="2e20b-104">Understanding and Interpreting Lux Values</span></span>

<span data-ttu-id="2e20b-105">Der primäre Sensor Datentyp für Umgebungslichtsensoren ist Beleuchtungs Kraft in Lux (dünn/Quadratmeter).</span><span class="sxs-lookup"><span data-stu-id="2e20b-105">The primary sensor data type for ambient light sensors is illuminance in lux (lumens per square meter).</span></span> <span data-ttu-id="2e20b-106">Die in diesem Thema beschriebenen Prinzipien basieren auf der Aufnahme von Lux-Werten als Eingabe und der Reaktion auf diese Daten in einem Programm.</span><span class="sxs-lookup"><span data-stu-id="2e20b-106">The principles outlined in this topic are based on taking lux values as input and reacting to that data in a program.</span></span>

<span data-ttu-id="2e20b-107">Lux-Messwerte sind direkt proportional zu der Energie pro Quadratmeter, die pro Sekunde erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="2e20b-107">Lux readings are directly proportional to the energy per square meter that is absorbed per second.</span></span> <span data-ttu-id="2e20b-108">Die menschliche Wahrnehmung von Licht Ebenen ist nicht so einfach.</span><span class="sxs-lookup"><span data-stu-id="2e20b-108">Human perception of light levels is not so straightforward.</span></span> <span data-ttu-id="2e20b-109">Die menschliche Wahrnehmung von Licht ist kompliziert, da unsere Augen ständig angepasst werden und andere biologische Prozesse unsere Wahrnehmung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="2e20b-109">Human perception of light is complicated because our eyes are constantly adjusting and other biological processes are affecting our perception.</span></span> <span data-ttu-id="2e20b-110">Wir können uns diese Wahrnehmung jedoch aus einer vereinfachten Perspektive vorstellen, indem Sie mehrere interessante Bereiche mit bekannten oberen und niedrigeren Schwellenwerten erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e20b-110">However, we can think of this perception from a simplified perspective by creating several ranges of interest with known upper and lower thresholds.</span></span>

<span data-ttu-id="2e20b-111">Das folgende Beispiel DataSet stellt grobe Schwellenwerte für allgemeine Beleuchtungsbedingungen und den entsprechenden Beleuchtungs Schritt dar.</span><span class="sxs-lookup"><span data-stu-id="2e20b-111">The following example data set represents rough thresholds for common lighting conditions, and the corresponding lighting step.</span></span> <span data-ttu-id="2e20b-112">Hier stellt jeder Beleuchtungs Schritt eine Änderung in der Beleuchtungs Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="2e20b-112">Here, each lighting step represents a change in lighting environment.</span></span>

> [!Note]  
> <span data-ttu-id="2e20b-113">Dieses DataSet ist zur Veranschaulichung und für alle Benutzer oder Situationen möglicherweise nicht vollständig genau.</span><span class="sxs-lookup"><span data-stu-id="2e20b-113">This data set is for illustration and may not be completely accurate for all users or situations.</span></span>

 



| <span data-ttu-id="2e20b-114">Beleuchtungs Bedingung</span><span class="sxs-lookup"><span data-stu-id="2e20b-114">Lighting condition</span></span> | <span data-ttu-id="2e20b-115">Von (Lux)</span><span class="sxs-lookup"><span data-stu-id="2e20b-115">From (lux)</span></span> | <span data-ttu-id="2e20b-116">An (Lux)</span><span class="sxs-lookup"><span data-stu-id="2e20b-116">To (lux)</span></span> | <span data-ttu-id="2e20b-117">Mittelwert (Lux)</span><span class="sxs-lookup"><span data-stu-id="2e20b-117">Mean value (lux)</span></span> | <span data-ttu-id="2e20b-118">Beleuchtungs Schritt</span><span class="sxs-lookup"><span data-stu-id="2e20b-118">Lighting step</span></span> |
|--------------------|------------|----------|------------------|---------------|
| <span data-ttu-id="2e20b-119">Schwarze Tonhöhe</span><span class="sxs-lookup"><span data-stu-id="2e20b-119">Pitch Black</span></span>        | <span data-ttu-id="2e20b-120">0</span><span class="sxs-lookup"><span data-stu-id="2e20b-120">0</span></span>          | <span data-ttu-id="2e20b-121">10</span><span class="sxs-lookup"><span data-stu-id="2e20b-121">10</span></span>       | <span data-ttu-id="2e20b-122">5</span><span class="sxs-lookup"><span data-stu-id="2e20b-122">5</span></span>                | <span data-ttu-id="2e20b-123">1</span><span class="sxs-lookup"><span data-stu-id="2e20b-123">1</span></span>             |
| <span data-ttu-id="2e20b-124">Sehr dunkel</span><span class="sxs-lookup"><span data-stu-id="2e20b-124">Very Dark</span></span>          | <span data-ttu-id="2e20b-125">11</span><span class="sxs-lookup"><span data-stu-id="2e20b-125">11</span></span>         | <span data-ttu-id="2e20b-126">50</span><span class="sxs-lookup"><span data-stu-id="2e20b-126">50</span></span>       | <span data-ttu-id="2e20b-127">30</span><span class="sxs-lookup"><span data-stu-id="2e20b-127">30</span></span>               | <span data-ttu-id="2e20b-128">2</span><span class="sxs-lookup"><span data-stu-id="2e20b-128">2</span></span>             |
| <span data-ttu-id="2e20b-129">Dunkel innen</span><span class="sxs-lookup"><span data-stu-id="2e20b-129">Dark Indoors</span></span>       | <span data-ttu-id="2e20b-130">51</span><span class="sxs-lookup"><span data-stu-id="2e20b-130">51</span></span>         | <span data-ttu-id="2e20b-131">200</span><span class="sxs-lookup"><span data-stu-id="2e20b-131">200</span></span>      | <span data-ttu-id="2e20b-132">125</span><span class="sxs-lookup"><span data-stu-id="2e20b-132">125</span></span>              | <span data-ttu-id="2e20b-133">3</span><span class="sxs-lookup"><span data-stu-id="2e20b-133">3</span></span>             |
| <span data-ttu-id="2e20b-134">Im Inneren</span><span class="sxs-lookup"><span data-stu-id="2e20b-134">Dim Indoors</span></span>        | <span data-ttu-id="2e20b-135">201</span><span class="sxs-lookup"><span data-stu-id="2e20b-135">201</span></span>        | <span data-ttu-id="2e20b-136">400</span><span class="sxs-lookup"><span data-stu-id="2e20b-136">400</span></span>      | <span data-ttu-id="2e20b-137">300</span><span class="sxs-lookup"><span data-stu-id="2e20b-137">300</span></span>              | <span data-ttu-id="2e20b-138">4</span><span class="sxs-lookup"><span data-stu-id="2e20b-138">4</span></span>             |
| <span data-ttu-id="2e20b-139">Normal im Inneren</span><span class="sxs-lookup"><span data-stu-id="2e20b-139">Normal Indoors</span></span>     | <span data-ttu-id="2e20b-140">401</span><span class="sxs-lookup"><span data-stu-id="2e20b-140">401</span></span>        | <span data-ttu-id="2e20b-141">1000</span><span class="sxs-lookup"><span data-stu-id="2e20b-141">1000</span></span>     | <span data-ttu-id="2e20b-142">700</span><span class="sxs-lookup"><span data-stu-id="2e20b-142">700</span></span>              | <span data-ttu-id="2e20b-143">5</span><span class="sxs-lookup"><span data-stu-id="2e20b-143">5</span></span>             |
| <span data-ttu-id="2e20b-144">Hell im Inneren</span><span class="sxs-lookup"><span data-stu-id="2e20b-144">Bright Indoors</span></span>     | <span data-ttu-id="2e20b-145">1001</span><span class="sxs-lookup"><span data-stu-id="2e20b-145">1001</span></span>       | <span data-ttu-id="2e20b-146">5.000</span><span class="sxs-lookup"><span data-stu-id="2e20b-146">5000</span></span>     | <span data-ttu-id="2e20b-147">3000</span><span class="sxs-lookup"><span data-stu-id="2e20b-147">3000</span></span>             | <span data-ttu-id="2e20b-148">6</span><span class="sxs-lookup"><span data-stu-id="2e20b-148">6</span></span>             |
| <span data-ttu-id="2e20b-149">Dim im Außenbereich</span><span class="sxs-lookup"><span data-stu-id="2e20b-149">Dim Outdoors</span></span>       | <span data-ttu-id="2e20b-150">5001</span><span class="sxs-lookup"><span data-stu-id="2e20b-150">5001</span></span>       | <span data-ttu-id="2e20b-151">10.000</span><span class="sxs-lookup"><span data-stu-id="2e20b-151">10,000</span></span>   | <span data-ttu-id="2e20b-152">7.500</span><span class="sxs-lookup"><span data-stu-id="2e20b-152">7500</span></span>             | <span data-ttu-id="2e20b-153">7</span><span class="sxs-lookup"><span data-stu-id="2e20b-153">7</span></span>             |
| <span data-ttu-id="2e20b-154">Bewölkt im Außenbereich</span><span class="sxs-lookup"><span data-stu-id="2e20b-154">Cloudy Outdoors</span></span>    | <span data-ttu-id="2e20b-155">10.001</span><span class="sxs-lookup"><span data-stu-id="2e20b-155">10,001</span></span>     | <span data-ttu-id="2e20b-156">30.000</span><span class="sxs-lookup"><span data-stu-id="2e20b-156">30,000</span></span>   | <span data-ttu-id="2e20b-157">20.000</span><span class="sxs-lookup"><span data-stu-id="2e20b-157">20,000</span></span>           | <span data-ttu-id="2e20b-158">8</span><span class="sxs-lookup"><span data-stu-id="2e20b-158">8</span></span>             |
| <span data-ttu-id="2e20b-159">Direktes Sonnenlicht</span><span class="sxs-lookup"><span data-stu-id="2e20b-159">Direct Sunlight</span></span>    | <span data-ttu-id="2e20b-160">30.001</span><span class="sxs-lookup"><span data-stu-id="2e20b-160">30,001</span></span>     | <span data-ttu-id="2e20b-161">100.000</span><span class="sxs-lookup"><span data-stu-id="2e20b-161">100,000</span></span>  | <span data-ttu-id="2e20b-162">65.000</span><span class="sxs-lookup"><span data-stu-id="2e20b-162">65,000</span></span>           | <span data-ttu-id="2e20b-163">9</span><span class="sxs-lookup"><span data-stu-id="2e20b-163">9</span></span>             |



 

<span data-ttu-id="2e20b-164">Wenn wir diese Daten mithilfe der Mittelwerte aus dieser Tabelle visualisieren, sehen wir, dass die Beziehung zwischen Lux und Beleuchtungs Schritt nicht linear ist, wie im folgenden Diagramm gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e20b-164">If we visualize this data by using the mean values from this table, we see that the lux-to-lighting-step relationship is not linear, as show in the following graph.</span></span>

![lineare Beleuchtungs Diagramm](images/luxtostep.png)

<span data-ttu-id="2e20b-166">Wenn wir diese Daten jedoch mithilfe einer logarithmischen Skalierung auf der x-Achse anzeigen, können wir sehen, dass eine ungefähr lineare Beziehung entsteht.</span><span class="sxs-lookup"><span data-stu-id="2e20b-166">However, if we view this data by using a logarithmic scale on the x-axis, we can see that a roughly linear relationship emerges.</span></span>

![logarithmische Beleuchtungs Diagramm](images/luxlogtostep.png)

### <a name="an-example-transform"></a><span data-ttu-id="2e20b-168">Eine Beispiel Transformation</span><span class="sxs-lookup"><span data-stu-id="2e20b-168">An Example Transform</span></span>

<span data-ttu-id="2e20b-169">Basierend auf dem Beispiel Dataset für Ambient-Light-Sensoren, die zuvor bereitgestellt wurden, können Sie die folgende Gleichung erreichen, um der menschlichen Wahrnehmung von Lux-Werten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2e20b-169">Based on the sample data set for ambient light sensors previously provided, you could arrive at the following equation to map lux values to human perception.</span></span> <span data-ttu-id="2e20b-170">In diesem Beispiel liegen die erwarteten Werte zwischen 0 und 1 Million Lux.</span><span class="sxs-lookup"><span data-stu-id="2e20b-170">In this example, the expected values range from 0 lux to 1,000,000 lux.</span></span>

![Lux-Wert Gleichung](images/sensor-lux-equation.jpg)

<span data-ttu-id="2e20b-172">Diese Gleichung führt zu Werten, die sich zwischen 0,0 und 1,0 in einer ungefähr linearen Weise unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2e20b-172">This equation results in values that vary in a roughly linear fashion between 0.0 and 1.0.</span></span> <span data-ttu-id="2e20b-173">Dieses Ergebnis gibt an, wie sich die von Menschen wahrgenommene Beleuchtung basierend auf dem zuvor gezeigten Beispiel Dataset geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2e20b-173">This result indicates how human-perceived lighting changed based on the example data set that was shown previously.</span></span>

 

 



