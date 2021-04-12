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
# <a name="variables-to-store-properties"></a>Variablen zum Speichern von Eigenschaften

Zunächst benötigen Sie eine Variable, um die Verzögerungszeit zu speichern. Das vom Assistenten für Windows-Media Player-Plug-in erstellte Standardbeispiel stellt eine Variable mit dem Namen m \_ fscalefactor zum Speichern des Skalierungs Multiplikators bereit, der für die Verarbeitung verwendet wird. In diesem Beispiel wird diese Variable nicht mehr benötigt, sodass Sie den Namen und den Typ ändern können, um den Wert für die Verzögerungszeit zu speichern.

1.  Ersetzen Sie jede Instanz von m \_ -f-Datei in Echo. h und Echo. cpp durch m \_ dwdelta-time.
2.  Ändern Sie den Datentyp für m \_ fscalefactor (jetzt m \_ dwdelta-Time) von Double in DWORD in Echo. h.
3.  Ändern Sie im Konstruktor für Cecho den Standardwert für Verzögerungszeit in 1000.
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

Deklarieren Sie anschließend zwei neue Element Variablen, um den Prozentsatz der Auswirkung zu speichern, und den Prozentsatz des Quell Signals, der im endgültigen Ausgabepuffer gemischt werden soll. Der Begriff "nass" bezieht sich auf den Effekt, und der Begriff "trocken" bezieht sich auf das Quell Signal. Fügen Sie Echo. h die folgenden Deklarationen hinzu:


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



Diese Werte werden als Dezimal Darstellungen von Prozentsätzen gespeichert, sodass Sie problemlos als Skalierungsfaktoren verwendet werden können. Beispielsweise würde eine Mischung aus 50-Prozent Effekten und einem Quell Signal von 50% als Wert 0,50 für jede Variable dargestellt werden. Die Summe der Werte für m "m", "m" und "m" von " \_ \_ f" darf nicht größer als 1,0 (100 Prozent) sein. Schließlich können diese Werte als Eigenschaften aufgerufen werden.

Fügen Sie dem Cecho-Konstruktor den folgenden Code hinzu, um die Standardwerte auf 50 Prozent festzulegen:


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo-Beispiel Eigenschaften**](echo-sample-properties.md)
</dt> </dl>

 

 




