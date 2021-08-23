---
title: Hinzufügen der Vernetzungsmischungseigenschaft
description: Hinzufügen der Vernetzungsmischungseigenschaft
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Windows Media Player Plug-Ins, Echo-Beispieleigenschaften
- Plug-Ins, Echo-Beispieleigenschaften
- Digitale Signalverarbeitungs-Plug-Ins, Echo-Beispieleigenschaften
- DSP-Plug-Ins, Echo-Beispieleigenschaften
- Echo-DSP-Plug-In-Beispiel, Eigenschaften
- Echo-DSP-Plug-In-Beispiel, Vermischungseigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f743cc25ce25aed1e7ff5695c022d65e30c1680eee4121eb3952698d6f0da94f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055418"
---
# <a name="adding-the-wet-mix-property"></a>Hinzufügen der Vernetzungsmischungseigenschaft

Sie müssen den Code hinzufügen, um die zusätzliche Eigenschaft für die Effektebene bereitzustellen.

Der Abschnitt [Hinzufügen von Eigenschaften zum Beispielaudio-DSP-Plug-In](adding-properties-to-the-sample-audio-dsp-plug-in.md) enthält Details zum Hinzufügen einer neuen Eigenschaft mithilfe von Visual C++. In diesem Abschnitt erfahren Sie, wie Sie den Code manuell hinzufügen. Dies umfasst das Hinzufügen von Code an den gleichen drei Stellen, an denen Sie den Code für die Delay Time-Eigenschaft geändert haben.

Fügen Sie die Prototypen für die \_ Get-Mix-Methode hinzu, und fügen Sie \_ die Methoden von "mixmix" direkt nach den anderen Prototypen der Eigenschaftsmethode in Echo.h ein. Verwenden Sie die folgende Syntax:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Fügen Sie nun die Implementierung für jede Methode unmittelbar nach den anderen Eigenschaftsimplementierungen in Echo.cpp hinzu. Das folgende Beispiel zeigt den Code für beide Methoden:


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



Beachten Sie, dass die Implementierung von put \_ mix den Code zum Berechnen des richtigen Werts für m \_ fDryMix enthält. Jedes Mal, wenn ein neuer Wert für m \_ fWetMix angegeben wird, ist diese Berechnung erforderlich.

Fügen Sie den folgenden Code direkt nach dem Code für die Verzögerungsmethoden in Echo.idl in die Schnittstellendefinition ein:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo Sample Properties**](echo-sample-properties.md)
</dt> </dl>

 

 




