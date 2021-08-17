---
title: Implementieren eines Renderbeispiels
description: Implementieren eines Renderbeispiels
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- Visualisierungen,Leuchtbeispiel
- Benutzerdefinierte Visualisierungen, Beispiel "Leucht"
- Programmierhandbuch,Visualisierungen
- Beispiele,Leuchtvisualisierung
- Beispiel für die Visualisierung von Leuchtern
- Visualisierungen,Render-Funktion
- Benutzerdefinierte Visualisierungen, Renderfunktion
- Renderfunktion,Leuchtbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c00b57f15655468e5bd0000ccc3b5120e19c2af58d5a1ad6b5493b535c7253f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135573"
---
# <a name="implementing-render-sample"></a>Implementieren eines Renderbeispiels

Der folgende Code wird verwendet, um die **Render-Funktion zu** implementieren:


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



Im Folgenden finden Sie eine Erläuterung des Codes:

Eine Variable namens *mycolor* wird für die Farbe des Lichts verwendet und mit **COLORREF deklariert.** Alle Farben sollten den **COLORREF-Datentyp** verwenden.

Eine Variable mit dem *Namen mylevel* wird für die Audiomomentaufnahme auf Waveformebene verwendet. Dieser Wert hängt vom tatsächlichen Energiestand zum Zeitpunkt der Momentaufnahme ab.

Die **switch-Anweisung** wird durch die Voreinstellung festgelegt, die der Benutzer für die Windows Media Player. Die Auswahl setzt *mycolor auf* die gewünschte Farbe (Rot, Grün oder Blau). Die genaue Farbe wird jedoch durch den Audioleistungsgrad bestimmt. Wenn z. B. die rote Voreinstellung ausgewählt wird, ist die Farbe vollrot, aber je nach Audio waveform zum Zeitpunkt der Momentaufnahme heller oder dunkler. Stellen Sie sicher, dass Sie das **RBG-Makro** verwenden, um Ihre Farbe zu erstellen.

Ein Pinsel mit dem Namen *hNewBrush* wird erstellt und zum Ausfüllen des *prc-Rechtecks* verwendet, das von Windows Media Player. Die Zeichenoberfläche ist der *hdc-Gerätekontext,* der von Windows Media Player.

Der Pinsel wird von **DeleteObject gelöscht.** Achten Sie immer darauf, alle von Ihnen erstellten Stifte oder Pinsel zu löschen.

Sobald der **Rendercode** abgeschlossen ist, Windows Media Player *hdc-Grafiken* in einem Fenster angezeigt, das von der verwendeten Skin bestimmt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**The Glow Sample**](the-glow-sample.md)
</dt> </dl>

 

 




