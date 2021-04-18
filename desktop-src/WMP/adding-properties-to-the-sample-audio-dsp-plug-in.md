---
title: Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in
description: Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Audioeigenschaften
- DSP-Plug-ins, Audioeigenschaften
- audiodsp-Plug-ins, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340209"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="ba66e-108">Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in</span><span class="sxs-lookup"><span data-stu-id="ba66e-108">Adding Properties to the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="ba66e-109">Der Beispielcode für audiodsp, den der Assistent für den Windows Media Player-Plug-in generiert, verwendet eine einzelne Eigenschaft, die den Skalierungsfaktor für das audiovolume darstellt.</span><span class="sxs-lookup"><span data-stu-id="ba66e-109">The audio DSP sample code that the Windows Media Player Plug-in Wizard generates uses a single property that represents the scale factor for the audio volume.</span></span> <span data-ttu-id="ba66e-110">Ihr Plug-in erfordert möglicherweise mehr als eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ba66e-110">Your plug-in may require more than one property.</span></span> <span data-ttu-id="ba66e-111">Mithilfe der folgenden Schritte können Sie Ihrem DSP-Plug-in in Visual Studio problemlos Eigenschaften hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ba66e-111">You can easily add properties to your DSP plug-in in Visual Studio using the following steps:</span></span>

-   <span data-ttu-id="ba66e-112">Definieren Sie die Methoden im Schnittstellen Definitions Code in der IDL-Datei, die Teil des ProxyStub-Projekts ist.</span><span class="sxs-lookup"><span data-stu-id="ba66e-112">Define the methods in the interface definition code in the IDL file that is part of the proxy-stub project.</span></span>
    -   <span data-ttu-id="ba66e-113">Fügen Sie die-Methoden Implementierungen der Haupt-CPP-Datei des Projekts hinzu:</span><span class="sxs-lookup"><span data-stu-id="ba66e-113">Add the method implementations to the project's main CPP file:</span></span>

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

<span data-ttu-id="ba66e-114">Um die Eigenschaften für den Benutzer zugänglich zu machen, müssen Sie schließlich Änderungen an der Implementierung der Eigenschaften Seite vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ba66e-114">Finally, to make the properties accessible to the user, you'll want to make changes to the property page implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba66e-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba66e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba66e-116">**Implementieren eines audiodsp-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="ba66e-116">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




