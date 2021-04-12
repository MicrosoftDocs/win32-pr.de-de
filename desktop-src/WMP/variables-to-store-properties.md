---
title: Variablen zum Speichern von Eigenschaften
description: Variablen zum Speichern von Eigenschaften
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Windows Media Player-Plug-ins, Echo-Beispiel Eigenschaften
- Plug-ins, Echo-Beispiel Eigenschaften
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel Eigenschaften
- DSP-Plug-ins, Echo-Beispiel Eigenschaften
- Echo DSP-Plug-in-Beispiel, Eigenschaften
- Echo DSP-Plug-in-Beispiel, Variablen zum Speichern von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206924"
---
# <a name="variables-to-store-properties"></a><span data-ttu-id="92225-109">Variablen zum Speichern von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92225-109">Variables to Store Properties</span></span>

<span data-ttu-id="92225-110">Zunächst benötigen Sie eine Variable, um die Verzögerungszeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="92225-110">First, you will need a variable to store the delay time.</span></span> <span data-ttu-id="92225-111">Das vom Assistenten für Windows-Media Player-Plug-in erstellte Standardbeispiel stellt eine Variable mit dem Namen m \_ fscalefactor zum Speichern des Skalierungs Multiplikators bereit, der für die Verarbeitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92225-111">The default sample created by the Windows Media Player Plug-in Wizard provides a variable named m\_fScaleFactor to store the scaling multiplier it uses for processing.</span></span> <span data-ttu-id="92225-112">In diesem Beispiel wird diese Variable nicht mehr benötigt, sodass Sie den Namen und den Typ ändern können, um den Wert für die Verzögerungszeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="92225-112">This sample no longer needs this variable, so you can change its name and type to store the delay time value.</span></span>

1.  <span data-ttu-id="92225-113">Ersetzen Sie jede Instanz von m \_ -f-Datei in Echo. h und Echo. cpp durch m \_ dwdelta-time.</span><span class="sxs-lookup"><span data-stu-id="92225-113">Replace each instance of m\_fScaleFactor in Echo.h and Echo.cpp with m\_dwDelayTime.</span></span>
2.  <span data-ttu-id="92225-114">Ändern Sie den Datentyp für m \_ fscalefactor (jetzt m \_ dwdelta-Time) von Double in DWORD in Echo. h.</span><span class="sxs-lookup"><span data-stu-id="92225-114">Change the data type for m\_fScaleFactor (now m\_dwDelayTime) from double to DWORD in Echo.h.</span></span>
3.  <span data-ttu-id="92225-115">Ändern Sie im Konstruktor für Cecho den Standardwert für Verzögerungszeit in 1000.</span><span class="sxs-lookup"><span data-stu-id="92225-115">In the constructor for CEcho, change the default delay time value to 1000.</span></span>
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

<span data-ttu-id="92225-116">Deklarieren Sie anschließend zwei neue Element Variablen, um den Prozentsatz der Auswirkung zu speichern, und den Prozentsatz des Quell Signals, der im endgültigen Ausgabepuffer gemischt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92225-116">Next, declare two new member variables to store the percentage of effect signal and the percentage of source signal to be mixed in the final output buffer.</span></span> <span data-ttu-id="92225-117">Der Begriff "nass" bezieht sich auf den Effekt, und der Begriff "trocken" bezieht sich auf das Quell Signal.</span><span class="sxs-lookup"><span data-stu-id="92225-117">The term "wet" refers to the effect, and the term "dry" refers to the source signal.</span></span> <span data-ttu-id="92225-118">Fügen Sie Echo. h die folgenden Deklarationen hinzu:</span><span class="sxs-lookup"><span data-stu-id="92225-118">Add the following declarations to Echo.h:</span></span>


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



<span data-ttu-id="92225-119">Diese Werte werden als Dezimal Darstellungen von Prozentsätzen gespeichert, sodass Sie problemlos als Skalierungsfaktoren verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="92225-119">These values are stored as decimal representations of percentages so they can easily be used as scale factors.</span></span> <span data-ttu-id="92225-120">Beispielsweise würde eine Mischung aus 50-Prozent Effekten und einem Quell Signal von 50% als Wert 0,50 für jede Variable dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="92225-120">For instance, a mixture of 50 percent effect and 50 percent source signal would be represented as a value of 0.50 for each variable.</span></span> <span data-ttu-id="92225-121">Die Summe der Werte für m "m", "m" und "m" von " \_ \_ f" darf nicht größer als 1,0 (100 Prozent) sein.</span><span class="sxs-lookup"><span data-stu-id="92225-121">The sum of the values for m\_fWetMix and m\_fDryMix must not be more than 1.0 (100 percent).</span></span> <span data-ttu-id="92225-122">Schließlich können diese Werte als Eigenschaften aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92225-122">Eventually, these values will be accessible as properties.</span></span>

<span data-ttu-id="92225-123">Fügen Sie dem Cecho-Konstruktor den folgenden Code hinzu, um die Standardwerte auf 50 Prozent festzulegen:</span><span class="sxs-lookup"><span data-stu-id="92225-123">Add the following code to the CEcho constructor to set the default values to 50 percent each:</span></span>


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a><span data-ttu-id="92225-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92225-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92225-125">**Echo-Beispiel Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="92225-125">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




