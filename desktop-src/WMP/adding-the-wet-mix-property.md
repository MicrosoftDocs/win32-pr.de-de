---
title: Hinzufügen der Eigenschaft "nass Mischung"
description: Hinzufügen der Eigenschaft "nass Mischung"
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Windows Media Player-Plug-ins, Echo-Beispiel Eigenschaften
- Plug-ins, Echo-Beispiel Eigenschaften
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel Eigenschaften
- DSP-Plug-ins, Echo-Beispiel Eigenschaften
- Echo DSP-Plug-in-Beispiel, Eigenschaften
- Echo DSP-Plug-in-Beispiel, Eigenschaft "nass Mischung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310088"
---
# <a name="adding-the-wet-mix-property"></a>Hinzufügen der Eigenschaft "nass Mischung"

Sie müssen den Code hinzufügen, um die zusätzliche Eigenschaft für die Wirkungs Ebene bereitzustellen.

Im Abschnitt [Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) finden Sie ausführliche Informationen zum Hinzufügen einer neuen Eigenschaft mit Visual C++. In diesem Abschnitt wird gezeigt, wie Sie den Code manuell hinzufügen. Dies umfasst das Hinzufügen von Code an denselben drei Stellen, an denen Sie den Code für die Eigenschaft Verzögerungszeit geändert haben.

Fügen Sie die Prototypen für die get \_ -Methode Get wetmix und Put \_ wetmix direkt nach den anderen Eigenschaften Methoden Prototypen in Echo. h ein. Verwenden Sie die folgende Syntax:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Fügen Sie jetzt die Implementierung für jede Methode direkt nach den anderen Eigenschafts Implementierungen in Echo. cpp hinzu. Das folgende Beispiel zeigt den Code für beide Methoden:


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



Beachten Sie, dass die Implementierung von put \_ wetmix den Code enthält, um den korrekten Wert für m \_ fdrymix zu berechnen. Jedes Mal, wenn ein neuer Wert für m-" \_ fiwetmix" angegeben wird, ist diese Berechnung erforderlich.

Fügen Sie den folgenden Code in der Schnittstellen Definition direkt nach dem Code für die Delay-Methoden in Echo. idl hinzu:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo-Beispiel Eigenschaften**](echo-sample-properties.md)
</dt> </dl>

 

 




