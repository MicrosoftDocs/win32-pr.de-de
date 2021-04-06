---
title: Implementieren von Cecho FinalConstruct
description: Implementieren von Cecho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Cecho FinalConstruct-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100690"
---
# <a name="implementing-cechofinalconstruct"></a><span data-ttu-id="3a2bf-109">Implementieren von Cecho:: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="3a2bf-109">Implementing CEcho::FinalConstruct</span></span>

<span data-ttu-id="3a2bf-110">Die Cecho:: FinalConstruct-Methode ist in Echo. cpp implementiert.</span><span class="sxs-lookup"><span data-stu-id="3a2bf-110">The CEcho::FinalConstruct method is implemented in Echo.cpp.</span></span> <span data-ttu-id="3a2bf-111">Es enthält Code zum Lesen der Eigenschaftswerte aus der Registrierung, wenn Windows Media Player das DSP-Plug-in-Objekt instanziiert.</span><span class="sxs-lookup"><span data-stu-id="3a2bf-111">It contains code to read the property values from the registry when Windows Media Player instantiates the DSP plug-in object.</span></span> <span data-ttu-id="3a2bf-112">Dies ist wichtig, da die Benutzereinstellungen zwischen Instanzen des Objekts und zwischen Sitzungen beibehalten werden können.</span><span class="sxs-lookup"><span data-stu-id="3a2bf-112">This is important because it allows the user settings to persist between instances of the object, as well as between sessions.</span></span> <span data-ttu-id="3a2bf-113">Der Beispielcode des Plug-in-Assistenten bietet eine Implementierung zum Lesen einer einzelnen Eigenschaft aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="3a2bf-113">The plug-in wizard sample code provides implementation to read a single property from the registry.</span></span> <span data-ttu-id="3a2bf-114">Sie können diesen Code ändern, um die Eigenschaft Verzögerungszeit zu verarbeiten, und dann Code hinzufügen, um den Eigenschafts Wert für die nasse Mischung zu lesen.</span><span class="sxs-lookup"><span data-stu-id="3a2bf-114">You can modify this code to handle the delay time property, and then add code to read the wet mix property value.</span></span>

<span data-ttu-id="3a2bf-115">Im folgenden Beispielcode wird jeder Eigenschafts Wert aus der Registrierung gelesen und in der richtigen Element Variablen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="3a2bf-115">The following example code reads each property value from the registry and stores each in the correct member variable:</span></span>


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



<span data-ttu-id="3a2bf-116">Beachten Sie, dass der DWORD-Wert für die nasse Mischung in einen Gleit Komma Wert konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="3a2bf-116">Notice that the DWORD value for the wet mix is converted to a floating-point value.</span></span> <span data-ttu-id="3a2bf-117">Beachten Sie auch, dass der Code den korrekten Wert für m-"sssmix" berechnet \_ .</span><span class="sxs-lookup"><span data-stu-id="3a2bf-117">Also note that the code calculates the correct value for m\_fDryMix.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a2bf-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a2bf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a2bf-119">**Ändern der Eigenschaften Seite Echo Sample**</span><span class="sxs-lookup"><span data-stu-id="3a2bf-119">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




