---
title: Hinzufügen von Eigenschaften zum Beispiel-Audio-DSP-Plug-In
description: Hinzufügen von Eigenschaften zum Beispiel-Audio-DSP-Plug-In
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Windows Media Player-Plug-Ins,Audio-DSP
- Plug-Ins, Audio-DSP
- Plug-Ins für die digitale Signalverarbeitung, Audioeigenschaften
- DSP-Plug-Ins, Audioeigenschaften
- Audio-DSP-Plug-Ins,Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b87c650ed66bbb3da0886eb02157804ca10005a47053def841996019917ceed8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031500"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Hinzufügen von Eigenschaften zum Beispiel-Audio-DSP-Plug-In

Der Audio-DSP-Beispielcode, den der Windows Media Player Plug-In-Assistent generiert, verwendet eine einzelne Eigenschaft, die den Skalierungsfaktor für das Audiovolumen darstellt. Ihr Plug-In erfordert möglicherweise mehrere Eigenschaften. Mithilfe der folgenden Schritte können Sie ihrem DSP-Plug-In ganz Visual Studio Eigenschaften hinzufügen:

-   Definieren Sie die Methoden im Schnittstellendefinitionscode in der IDL-Datei, die Teil des Proxystubprojekts ist.
    -   Fügen Sie die Methodenimplementierung der CPP-Hauptdatei des Projekts hinzu:

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

    

Abschließend sollten Sie Änderungen an der Implementierung der Eigenschaftenseite vornehmen, um dem Benutzer zugriff auf die Eigenschaften zu ermöglichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Audio-DSP-Plug-Ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




