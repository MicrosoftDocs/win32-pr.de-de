---
description: Mehrere Consumer, z. b. der aktive Skript Ereignisconsumer oder der Befehlszeilen-Ereignisconsumer, verfügen über Zeichen folgen Eigenschaften mit dem Vorlagen Qualifizierer.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Verwenden von Standard mäßigen Zeichen folgen Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866867"
---
# <a name="using-standard-string-templates"></a><span data-ttu-id="b8b2e-103">Verwenden von Standard mäßigen Zeichen folgen Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b8b2e-103">Using Standard String Templates</span></span>

<span data-ttu-id="b8b2e-104">Mehrere Consumer, z. b. der aktive Skript Ereignisconsumer oder der Befehlszeilen-Ereignisconsumer, verfügen über Zeichen folgen Eigenschaften mit dem **Vorlagen** Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-104">Several consumers, such as the Active Script Event Consumer or the Command Line Event Consumer, have string properties with the **Template** qualifier.</span></span> <span data-ttu-id="b8b2e-105">Diese Eigenschaften verwenden standardmäßige Zeichen folgen Vorlagen, um eine Zeichenfolge zu erstellen, die teilweise von der consumerinstanz und teilweise von einem Ereignis konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-105">These properties use standard string templates to construct a string that is configured in part by the consumer instance and in part by an event.</span></span> <span data-ttu-id="b8b2e-106">Die Struktur einer Standard Zeichen folgen Vorlage ähnelt der Spezifikation der Microsoft Windows-Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-106">The structure of a standard string template is similar to the Microsoft Windows environment variable specification.</span></span>

<span data-ttu-id="b8b2e-107">In der folgenden Liste sind einige Beispiele für die Vorlagen Sprache aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b8b2e-107">The following list shows some examples of the template language:</span></span>

-   <span data-ttu-id="b8b2e-108">Die Zeichenfolge "Text hier" erzeugt immer die Zeichenfolge "Text hier".</span><span class="sxs-lookup"><span data-stu-id="b8b2e-108">The string "Some text here" always produces the string "Some text here".</span></span>
-   <span data-ttu-id="b8b2e-109">"% Cpuausnutzung%" erzeugt immer den Wert der **cpunutzungseigenschaft** des übermittelten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-109">"%CPUUtilization%" always produces the value of the **CPUUtilization** property of the event being delivered.</span></span> <span data-ttu-id="b8b2e-110">Wenn die Eigenschaft keine Zeichenfolge ist, wird Sie in eine Zeichenfolge konvertiert. Beispiel: "90" oder "true".</span><span class="sxs-lookup"><span data-stu-id="b8b2e-110">If the property is not a string, it is converted to a string; for example, "90" or "TRUE".</span></span>
-   <span data-ttu-id="b8b2e-111">"Die CPU-Auslastung dieses Prozessors ist zu diesem Zeitpunkt% cpuausnutzung%." bettet den Wert der **cpunutzungseigenschaft** des Ereignisses in die Zeichenfolge ein und erzeugt so etwa Folgendes: "die CPU-Auslastung dieses Prozessors ist 90.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-111">"The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization** property of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".</span></span>
-   <span data-ttu-id="b8b2e-112">"% TargetInstance. cpuauslastungs%" Ruft den Wert der **cpunutzungseigenschaft** in der eingebetteten Instanz der **TargetInstance** -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-112">"%TargetInstance.CPUUtilization%" retrieves the value of the **CPUUtilization** property in the embedded instance of the **TargetInstance** property.</span></span>
-   <span data-ttu-id="b8b2e-113">"%%" erzeugt ein einzelnes%-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-113">"%%" produces a single % sign.</span></span>
-   <span data-ttu-id="b8b2e-114">Wenn es sich bei der abgerufenen Eigenschaft um ein Array handelt, wird das gesamte Array im folgenden Format erstellt: "(1, 5, 10, 1024)".</span><span class="sxs-lookup"><span data-stu-id="b8b2e-114">If the property being retrieved is an array, the entire array is produced in the following format: "(1,5,10,1024)".</span></span> <span data-ttu-id="b8b2e-115">Wenn nur ein-Element im-Array vorhanden ist, werden die Klammern ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-115">If there is only one element in the array, the parentheses are omitted.</span></span> <span data-ttu-id="b8b2e-116">Wenn keine Elemente im Array vorhanden sind, wird "()" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-116">If there are no elements in the array, "()" is produced.</span></span>
-   <span data-ttu-id="b8b2e-117">Wenn eine Eigenschaft ein eingebettetes Objekt ist, wird die MOF-Darstellung des Objekts erstellt (ähnlich der Methode [**IWbemClassObject:: getobjecttext**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).</span><span class="sxs-lookup"><span data-stu-id="b8b2e-117">If a property is an embedded object, the MOF representation of the object is produced (similar to the [**IWbemClassObject::GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) method).</span></span>
-   <span data-ttu-id="b8b2e-118">Wenn eine Eigenschaft eines eingebetteten Arrays von-Objekten angefordert wird, wird diese als Eigenschaft mit einem Array Wert behandelt.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-118">If a property of an embedded array of objects is requested, it is treated as a property with an array value.</span></span> <span data-ttu-id="b8b2e-119">Beispiel:% MyEvents. TargetInstance. driverletter% kann "(" C: "," D: ")" ("C:", "D:") "(" C: "," D: ")" ergeben</span><span class="sxs-lookup"><span data-stu-id="b8b2e-119">For example: %MyEvents.TargetInstance.DriverLetter% could produce '("C:","D:")' if MyEvents is an array of embedded instance modification events.</span></span>

## <a name="string-literals"></a><span data-ttu-id="b8b2e-120">Zeichenfolgenliterale</span><span class="sxs-lookup"><span data-stu-id="b8b2e-120">String Literals</span></span>

<span data-ttu-id="b8b2e-121">Alles in einem Paar von Anführungszeichen wird als Zeichenfolgenliteralzeichen betrachtet und nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-121">Anything inside a pair of quotes is considered a string literal and will not be replaced.</span></span>

<span data-ttu-id="b8b2e-122">Das folgende Beispiel zeigt die Zeichenfolge, die der Compiler für "CPU-Auslastung ist% cpuausnutzung%" anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-122">The following example shows the string that the compiler sees for "CPU utilization is %CPUUtilization%".</span></span>

``` syntax
CPU utilization is %CPUUtilization%
```

<span data-ttu-id="b8b2e-123">Diese Zeichenfolge erzeugt die folgende Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-123">This string produces the following output.</span></span>

``` syntax
CPU utilization is 90
```

<span data-ttu-id="b8b2e-124">Andererseits wird die Zeichenfolge "CPU-Auslastung ( \\ % cpuausnutzung%") \\ wie folgt vom Compiler erkannt.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-124">On the other hand, the string "CPU utilization is \\"%CPUUtilization%\\"" is seen by the compiler as follows.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

<span data-ttu-id="b8b2e-125">Diese Zeichenfolge erzeugt die folgende Ausgabe ohne Variablen Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="b8b2e-125">This string produces the following output, with no variable substitution.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a><span data-ttu-id="b8b2e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8b2e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8b2e-127">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="b8b2e-127">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



