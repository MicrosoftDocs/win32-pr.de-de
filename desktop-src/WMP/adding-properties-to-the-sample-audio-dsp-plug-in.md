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
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in

Der Beispielcode für audiodsp, den der Assistent für den Windows Media Player-Plug-in generiert, verwendet eine einzelne Eigenschaft, die den Skalierungsfaktor für das audiovolume darstellt. Ihr Plug-in erfordert möglicherweise mehr als eine Eigenschaft. Mithilfe der folgenden Schritte können Sie Ihrem DSP-Plug-in in Visual Studio problemlos Eigenschaften hinzufügen:

-   Definieren Sie die Methoden im Schnittstellen Definitions Code in der IDL-Datei, die Teil des ProxyStub-Projekts ist.
    -   Fügen Sie die-Methoden Implementierungen der Haupt-CPP-Datei des Projekts hinzu:

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

    

Um die Eigenschaften für den Benutzer zugänglich zu machen, müssen Sie schließlich Änderungen an der Implementierung der Eigenschaften Seite vornehmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines audiodsp-Plug-ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




