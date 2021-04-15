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
# <a name="implementing-render-sample"></a>Implementieren von Rendering Sample

Der folgende Code wird verwendet, um die Funktion " **Rendering** " zu implementieren:


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



Im folgenden finden Sie eine Erläuterung des Codes:

Eine Variable mit dem Namen " *myColor* " wird für die Farbe des Leucht Stoffs verwendet und mit **COLORREF** deklariert. Für alle Farben sollte der **COLORREF** -Datentyp verwendet werden.

Eine Variable mit dem Namen " *mylevel* " wird für die Momentaufnahme der Audiowaveform-Ebene verwendet. Dieser Wert hängt von der tatsächlichen Stromversorgung zum Zeitpunkt der Momentaufnahme ab.

Die **Switch** -Anweisung wird von der Voreinstellung festgelegt, die der Benutzer unter Windows Media Player ausgewählt hat. Mit der Auswahl wird " *myColor* " auf die gewünschte Farbe (rot, grün oder blau) festgelegt. Die genaue Farbe wird jedoch durch die audiostromebene bestimmt. Wenn z. b. die rote Voreinstellung ausgewählt wird, ist die Farbe ein ausgefülltes, aber je nach Audiowaveform zum Zeitpunkt der Momentaufnahme heller oder dunkler. Stellen Sie sicher, dass Sie das **RBG** -Makro verwenden, um die Farbe zu erstellen.

Es wird ein Pinsel namens *hnewbrush* erstellt, der verwendet wird, um das von Windows Media Player bereitgestellte *PRC* -Rechteck auszufüllen. Die Zeichen Oberfläche ist der *hdc* -Gerätekontext, der von Windows Media Player bereitgestellt wird.

Der Pinsel wird von **DeleteObject** gelöscht. Stellen Sie immer sicher, dass Sie alle von Ihnen erstellten Stifte oder Pinsel löschen.

Nachdem der **rendercode** abgeschlossen ist, zeigt Windows Media Player die *hdc* -Grafiken in einem Fenster an, das von der verwendeten Skin bestimmt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Das Glüh Beispiel**](the-glow-sample.md)
</dt> </dl>

 

 




