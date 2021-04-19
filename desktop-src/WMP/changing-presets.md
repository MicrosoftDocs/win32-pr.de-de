---
title: Ändern von Voreinstellungen
description: Ändern von Voreinstellungen
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- Visualisierungen, Glüh Beispiel
- benutzerdefinierte Visualisierungen, Glüh Beispiel
- Programmier Handbuch, Visualisierungen
- Beispiele, Glanz Visualisierung
- Beispiel für Glanz Visualisierung
- Visualisierungen, Voreinstellungen
- benutzerdefinierte Visualisierungen, Voreinstellungen
- Voreinstellungen in Visualisierungen, Glüh Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342053"
---
# <a name="changing-presets"></a><span data-ttu-id="faa1a-111">Ändern von Voreinstellungen</span><span class="sxs-lookup"><span data-stu-id="faa1a-111">Changing Presets</span></span>

<span data-ttu-id="faa1a-112">Die folgenden vordefinierten Code Abschnitte wurden so geändert, dass Sie drei Voreinstellungen zulassen:</span><span class="sxs-lookup"><span data-stu-id="faa1a-112">The following preset code sections were changed to allow three presets:</span></span>

## <a name="getpresettitle"></a><span data-ttu-id="faa1a-113">Getpresettitle</span><span class="sxs-lookup"><span data-stu-id="faa1a-113">GetPresetTitle</span></span>

<span data-ttu-id="faa1a-114">Dieser Code wurde anstelle des generierten voreingestellten Codes eingefügt:</span><span class="sxs-lookup"><span data-stu-id="faa1a-114">This code was inserted in place of the generated preset code:</span></span>


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a><span data-ttu-id="faa1a-115">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="faa1a-115">Enumerations</span></span>

<span data-ttu-id="faa1a-116">Die folgende Enumeration in "Glow. h" wurde so geändert, dass drei Voreinstellungen zulässig sind:</span><span class="sxs-lookup"><span data-stu-id="faa1a-116">The following enumeration in Glow.h was changed to allow three presets:</span></span>


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a><span data-ttu-id="faa1a-117">Ressourcen Header</span><span class="sxs-lookup"><span data-stu-id="faa1a-117">Resource Header</span></span>

<span data-ttu-id="faa1a-118">Die folgenden Ressourcen wurden in "Resource. h" definiert, um drei Voreinstellungen zuzulassen:</span><span class="sxs-lookup"><span data-stu-id="faa1a-118">The following resources were defined in Resource.h to allow three presets:</span></span>


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



<span data-ttu-id="faa1a-119">Beachten Sie, dass Sie auch die Ressourcen Anzahl von **\_ APS \_ Next \_ symed \_ value** in 106 ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="faa1a-119">Note that you must also change the resource number of **\_APS\_NEXT\_SYMED\_VALUE** to 106.</span></span>

## <a name="resource-file"></a><span data-ttu-id="faa1a-120">Ressourcendatei</span><span class="sxs-lookup"><span data-stu-id="faa1a-120">Resource File</span></span>

<span data-ttu-id="faa1a-121">Die folgenden Zeichen folgen müssen in der Datei "glowdll. RC" geändert werden, um drei Voreinstellungen zuzulassen und Ihnen Namen zu geben:</span><span class="sxs-lookup"><span data-stu-id="faa1a-121">The following strings must be changed in the Glowdll.rc file to allow three presets and give them names:</span></span>


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a><span data-ttu-id="faa1a-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="faa1a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faa1a-123">**Das Glüh Beispiel**</span><span class="sxs-lookup"><span data-stu-id="faa1a-123">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




