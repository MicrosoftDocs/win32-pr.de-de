---
title: Implementieren von Rendering Sample
description: Implementieren von Rendering Sample
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- Visualisierungen, Glüh Beispiel
- benutzerdefinierte Visualisierungen, Glüh Beispiel
- Programmier Handbuch, Visualisierungen
- Beispiele, Glanz Visualisierung
- Beispiel für Glanz Visualisierung
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Funktion "Rendering", Glanz Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517330"
---
# <a name="implementing-render-sample"></a><span data-ttu-id="52977-111">Implementieren von Rendering Sample</span><span class="sxs-lookup"><span data-stu-id="52977-111">Implementing Render Sample</span></span>

<span data-ttu-id="52977-112">Der folgende Code wird verwendet, um die Funktion " **Rendering** " zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="52977-112">The following code is used to implement the **Render** function:</span></span>


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



<span data-ttu-id="52977-113">Im folgenden finden Sie eine Erläuterung des Codes:</span><span class="sxs-lookup"><span data-stu-id="52977-113">Here is an explanation of the code:</span></span>

<span data-ttu-id="52977-114">Eine Variable mit dem Namen " *myColor* " wird für die Farbe des Leucht Stoffs verwendet und mit **COLORREF** deklariert.</span><span class="sxs-lookup"><span data-stu-id="52977-114">A variable named *mycolor* is used for the color of the glow and is declared with **COLORREF**.</span></span> <span data-ttu-id="52977-115">Für alle Farben sollte der **COLORREF** -Datentyp verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52977-115">All colors should use the **COLORREF** data type.</span></span>

<span data-ttu-id="52977-116">Eine Variable mit dem Namen " *mylevel* " wird für die Momentaufnahme der Audiowaveform-Ebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="52977-116">A variable named *mylevel* is used for the audio waveform level snapshot.</span></span> <span data-ttu-id="52977-117">Dieser Wert hängt von der tatsächlichen Stromversorgung zum Zeitpunkt der Momentaufnahme ab.</span><span class="sxs-lookup"><span data-stu-id="52977-117">This value will depend on the actual power level at the moment of the snapshot.</span></span>

<span data-ttu-id="52977-118">Die **Switch** -Anweisung wird von der Voreinstellung festgelegt, die der Benutzer unter Windows Media Player ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="52977-118">The **switch** statement is set by the preset that the user has chosen on Windows Media Player.</span></span> <span data-ttu-id="52977-119">Mit der Auswahl wird " *myColor* " auf die gewünschte Farbe (rot, grün oder blau) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52977-119">The choice will set *mycolor* to the desired color (red, green, or blue).</span></span> <span data-ttu-id="52977-120">Die genaue Farbe wird jedoch durch die audiostromebene bestimmt.</span><span class="sxs-lookup"><span data-stu-id="52977-120">However, the exact color will be determined by the audio power level.</span></span> <span data-ttu-id="52977-121">Wenn z. b. die rote Voreinstellung ausgewählt wird, ist die Farbe ein ausgefülltes, aber je nach Audiowaveform zum Zeitpunkt der Momentaufnahme heller oder dunkler.</span><span class="sxs-lookup"><span data-stu-id="52977-121">For example, if the red preset is chosen, the color will be a solid red, but it will be lighter or darker depending on the audio waveform at the moment of the snapshot.</span></span> <span data-ttu-id="52977-122">Stellen Sie sicher, dass Sie das **RBG** -Makro verwenden, um die Farbe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="52977-122">Be sure to use the **RBG** macro to create your color.</span></span>

<span data-ttu-id="52977-123">Es wird ein Pinsel namens *hnewbrush* erstellt, der verwendet wird, um das von Windows Media Player bereitgestellte *PRC* -Rechteck auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="52977-123">A brush is created called *hNewBrush*, and it is used to fill the *prc* rectangle provided by Windows Media Player.</span></span> <span data-ttu-id="52977-124">Die Zeichen Oberfläche ist der *hdc* -Gerätekontext, der von Windows Media Player bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="52977-124">The drawing surface is the *hdc* device context provided by Windows Media Player.</span></span>

<span data-ttu-id="52977-125">Der Pinsel wird von **DeleteObject** gelöscht.</span><span class="sxs-lookup"><span data-stu-id="52977-125">The brush is deleted by **DeleteObject**.</span></span> <span data-ttu-id="52977-126">Stellen Sie immer sicher, dass Sie alle von Ihnen erstellten Stifte oder Pinsel löschen.</span><span class="sxs-lookup"><span data-stu-id="52977-126">Always be sure to delete any pens or brushes you create.</span></span>

<span data-ttu-id="52977-127">Nachdem der **rendercode** abgeschlossen ist, zeigt Windows Media Player die *hdc* -Grafiken in einem Fenster an, das von der verwendeten Skin bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="52977-127">Once the **Render** code is finished, Windows Media Player will display the *hdc* graphics in a window determined by the skin being used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52977-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52977-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52977-129">**Das Glüh Beispiel**</span><span class="sxs-lookup"><span data-stu-id="52977-129">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




