---
title: Aktivieren der DirectX-Video Beschleunigung
description: Aktivieren der DirectX-Video Beschleunigung
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows Media-Format-SDK, Aktivieren von DXVA
- Windows Media-Format-SDK, DirectX-Video Beschleunigung (DXVA)
- Windows Media-Format-SDK, Videobeschleunigung
- Advanced Systems Format (ASF), Aktivieren von DXVA
- ASF (Advanced Systems Format), Aktivieren von DXVA
- Advanced Systems Format (ASF), DirectX-Video Beschleunigung (DXVA)
- ASF (Advanced Systems-Format), DirectX-Video Beschleunigung (DXVA)
- Advanced Systems Format (ASF), Videobeschleunigung
- ASF (Advanced Systems Format), Videobeschleunigung
- DirectX-Video Beschleunigung (DXVA), aktivieren
- DXVA (DirectX-Video Beschleunigung), aktivieren
- DirectX-Video Beschleunigung (DXVA), Reihenfolge der Vorgänge
- DXVA (DirectX-Video Beschleunigung), Reihenfolge der Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896147fe11b4b7f5fb91d8dc288e616b643bd5ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389846"
---
# <a name="enabling-directx-video-acceleration"></a>Aktivieren der DirectX-Video Beschleunigung

In diesem Abschnitt wird beschrieben, wie Sie Microsoft® DirectX® Video Beschleunigung bei der Wiedergabe von gestreuten Inhalten in einem benutzerdefinierten Player aktivieren.

## <a name="background"></a>Hintergrund

DirectX-Video Beschleunigung (DirectX VA) ist eine API-Spezifikation für die Hardwarebeschleunigung von 2D-Decodierungs Vorgängen. Dadurch können Software Decoder bestimmte CPU-intensive Vorgänge zur Verarbeitung auf die Grafikkarte auslagern. Für Endbenutzer ist dies ein Video mit hoher Bitrate, z. b. voll Bild-DVD-Wiedergabe auf älteren Computern, die mit DirectX VA-kompatiblen Grafikkarten ausgestattet sind.

Der DMO-Wrapper Filter unterstützt ab dem Windows Media Format 9-Reihe-SDK DirectX VA. Dies bedeutet, dass Anwendungen für die lokale Wiedergabe den WM-ASF-Reader-Filter verwenden können, um Windows Media-basierte Inhalte wiederzugeben, und die DirectX VA-Hardwarebeschleunigung wird automatisch aufgerufen, wenn Sie von der Grafikkarte unterstützt wird. Der WM-ASF-Reader-Filter unterstützt die Wiedergabe von gestreuten Inhalten jedoch nicht. Wenn Sie DirectX VA bei der Wiedergabe von gestreuten Inhalten in einem benutzerdefinierten Player unterstützen möchten, müssen Sie daher einen alternativen Mechanismus verwenden. dieser Mechanismus wird von Windows Media Player der mit der Windows Media 9-Reihe verwendet wird.

Da Windows Media Player vor der Entwicklung der qasf-Filter entworfen wurde, verfügt Windows Media Player über einen eigenen Quell Filter, der auf dem Windows Media-Format-SDK für die Wiedergabe von Windows Media-basierten Inhalten basiert. Der WMP-Windows Media-Quell Filter liefert dekomprimierte Daten direkt an die Audio-und Videorenderer. Im Gegensatz dazu stellt der WM-ASF-Reader komprimierte Inhalte Downstream an den Windows Media Decoder DirectX Media Objects (DMOs) bereit, die im DMO-Wrapper gehostet werden. In den folgenden Diagrammen werden die Unterschiede zwischen dem WM-ASF-Reader und dem WMP-Windows Media-Quell Filter veranschaulicht.

![benutzerdefinierter Quell Filter gibt unkomprimierte Beispiele aus](images/wmp-dxva-graph.png)

![qasf-Quell Filter gibt komprimierte Beispiele aus.](images/qasf-dxva-graph.png)

Um DirectX VA für das Streamen von Inhalten zu aktivieren, müssen Sie einen benutzerdefinierten Quell Filter wie den im oberen Diagramm erstellen. Im Grunde wird mit diesem Filter das Windows Media-Format-SDK verwendet, um ein WM-Reader-Objekt zu instanziieren, die Beispiele zu dekomprimieren und an die Ausgabe Pins zu senden. In dieser Erläuterung wird davon ausgegangen, dass Sie den Quell Filter bereits erstellt haben und jetzt bereit sind, die DirectX-VA-Unterstützung zu implementieren.

Zum Aktivieren von DirectX VA besteht die grundlegende Aufgabe des Quell Filters darin, den Videorenderer und den WMV-Decoder DMO mit den Schnittstellen bereitzustellen, die für die Aushandlung der DirectX-VA-Verbindung erforderlich sind. Der Quell Filter ist nicht an diesen Verhandlungen beteiligt. Nachdem das Streaming gestartet wurde, besteht die einzige DirectX-VA-bezogene Aufgabe, die der Quell Filter ausführen kann, darin, die Zeitstempel in den Videobeispielen zu ändern, bevor der WMV-Decoder Sie an den Videorenderer übergibt. Der Hauptgrund hierfür ist die Bereitstellung eines benutzerdefinierten Zeitachsen-Steuer Elements, das über die Aktivierung der standardmäßigen DirectShow-® Schnittstellen hinausgeht

Es werden drei Schnittstellen definiert, um die erforderliche Kommunikation zwischen dem Windows Media-Format-SDK, dem Quell Filter des Players, dem Windows Media Video Decoder DMO und dem Überlagerungs-oder videomischungs-Renderer zu ermöglichen. Diese Schnittstellen werden in der folgenden Tabelle beschrieben.



| Schnittstelle                                                        | BESCHREIBUNG                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmcodecamvideoaccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Wird vom Windows Media Decoder DMO verfügbar gemacht und durch den Quell Filter eines Media Player aufgerufen, um die verschiedenen Verbindungen einzurichten, die zum Aktivieren von DirectX VA für das Decodieren von Windows Media Video Inhalt erforderlich sind. |
| [**Iwmplayertimestamphook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Wird für den Quell Filter des Players implementiert. Sie ermöglicht es dem Filter, die Zeitstempel in den Videobeispielen vor der Übertragung zu ändern.                                                 |
| [**Iwmreaderaccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Wird für das WM Reader-Objekt implementiert. Sie wird von einem Player-Quell Filter aufgerufen, um Schnittstellen vom Decoder-DMO abzurufen.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Reihenfolge der Vorgänge in DirectX VA – aktivierter Wiedergabe

In diesem Abschnitt wird die allgemeine Reihenfolge der Vorgänge zur Laufzeit für einen DirectX-aktivierten Player und dessen Quell Filter beschrieben. Die Komponenten, auf die in diesem Abschnitt verwiesen wird, lauten:

-   Ein Drittanbieter-Media Player, der als Player bezeichnet wird.
-   Ein benutzerdefinierter Quell Filter, der vom Player instanziiert wird, der das Windows Media-Format-SDK zum Dekomprimieren von Windows Media-basiertem Inhalt verwendet.
-   Die Videoausgabe-PIN des Quell Filters des Players, der als Ausgabe-PIN bezeichnet wird.
-   Das Diagramm für den DirectShow-Videowiedergabe Filter, das als Graph bezeichnet wird.
-   Der Video Mischungs-Renderer, der als VMR bezeichnet wird.
-   Das Windows Media Format SDK-asynchrone Reader-Objekt, das als Reader bezeichnet wird.
-   Das DirectX-Medienobjekt Windows Media Video Decoder, das als Decoder DMO bezeichnet wird.

Die Reihenfolge der Vorgänge lautet wie folgt:

1.  Der Player instanziiert seinen Quell Filter und ein Reader-Objekt. Der Reader erstellt einen Video Decoder DMO und legt den (komprimierten) Eingabetyp darauf fest. Dies muss eintreten, bevor der Player versucht, das Videowiedergabe Diagramm zu konfigurieren, da das SDK und der Decoder-DMO an dem Aushandlungs Prozess mit dem Diagramm beteiligt sein müssen, und der DMO muss das Eingabeformat in Schritt 9 kennen.
2.  Der Player ruft **igraphbuilder:: Rendering** auf und stellt ihm die Ausgabe-PIN des Video Quell Filters bereit. An diesem Punkt versucht der DirectShow Filter Graph-Manager, die VMR mit dem Video Quell Filter des Players zu verbinden.
3.  Der Filter Graph-Manager ruft **IPin:: Connect** in der Ausgabe-PIN des Video Quell Filters des Players auf.

Die Schritte 4 bis 10 erfolgen innerhalb von **IPin:: Connect**.

1.  Der Quell Filter Ruft die **iwmcodecamvideoaccelerator** -Schnittstelle aus der **iwmreaderaccelerator:: getcodecinterface** -Methode des Readers ab. Wenn der Codec DirectX VA nicht unterstützt, tritt beim Aufrufen von **getcodecinterface** möglicherweise ein Fehler auf. In diesem Fall verläuft die Aushandlung wie gewohnt, ohne DirectX-VA-Unterstützung.
2.  Der Quell Filter übergibt den **iamvideoaccelerator** -Zeiger von **der an übergebenen Pin über** **iwmcodecamvideoaccelerator:: setacceleratorinterface**.
3.  Der Quell Filter delegiert dann den Rest des **IPin:: Connect** -Vorgangs an die **cbaseoutputpin:: Connect** -Methode. Die formatenumeration mit dem SDK verläuft wie heute. Wenn der Codec DirectX VA für den Inhalt unterstützt, der verbunden wird, stellt der Codec-DMO diese DirectX VA-Untertypen zuerst vor, bevor die unterstützten YUV-und RGB-Typen unterstützt werden. Wenn die DirectX-VA-Unterstützung verfügbar ist, werden die Schritte 7 bis 11 im Kontext eines DirectX VA-unter Typs ausprobiert. Der folgende Code Ausschnitt zeigt, wie ein DirectX-VA-Medien Untertyp identifiziert wird.
    ```C++
    bool IsDXVASubtype( AM_MEDIA_TYPE * pmt )
    {
        // All DXVA types have the same last 3 DWORDs.
        // guidDXVA is the base GUID for all DXVA subtypes.

        GUID guidDXVA = { 0x00000000, 0xa0c7, 0x11d3, { 0xb9,0x84,0x00,0xc0,0x4f,0x2e,0x73,0xc5 } };

        unsigned long const * plguid;
        unsigned long const * plguidDXVA;
        plguid = (unsigned long const *)&pmt->subtype;
        plguidDXVA = (unsigned long *)&guidDXVA;

        if( ( plguid[1] == plguidDXVA[1] ) &&
            ( plguid[2] == plguidDXVA[2] ) &&
            ( plguid[3] == plguidDXVA[3] ) )
        {
            return true;
        }

        return false;
    }
    
    ```

    

4.  Die **cbaseoutputpin:: Connect** -Implementierung ruft **IPin:: completeconnect** während Schritt 3 auf. Wenn ein DirectX-VA-Untertyp berücksichtigt wird, wird versucht, die DirectX-VA-Aushandlung auszuführen. Die Ausgabepin ruft **iwmcodecamvideoaccelerator:: aushandateconnetction** auf und übergibt dabei den aktuellen Ausgabe Medientyp.
5.  Der Decoder DMO führt die erforderliche Aushandlung mit der VMR über die **iamvideoaccelerator** -Schnittstelle aus und gibt den Video Untertyp GUID zurück, den die beiden zugestimmt haben. Die Ausgabe-PIN delegiert alle **iamvideoacceleratornotify** -Aufrufe, die während dieses Prozesses empfangen werden, an die **iamvideoacceleratornotify** -Schnittstelle des Decoders DMO, die auch über die **iwmreaderaccelerator:: getcodecinterface** -Methode abgerufen werden kann.
6.  Wenn **aushandateconnetction** erfolgreich ist, ruft die Ausgabepin **iwmcodecamvideoaccelerator:: setplayernotify** mit einer **iwmplayertimestamphook** -Schnittstelle auf. Mit diesem Hook kann der Quell Filter die Zeitstempel der Beispiele aktualisieren, bevor Sie an den Renderer übergeben werden.
7.  Der Quell Filter ruft **iwmreaderaccelerator:: notify** mit dem ausgehandelten Medientyp auf. Dies ermöglicht es dem Reader, seine internen Variablen zu aktualisieren und an DirectX VA zu übergeben. Dies ist die letzte Stelle, an der der Codec oder der Reader fehlschlagen kann. Wenn einer der obigen Schritte fehlschlägt, sollte der Quell Filter zu Schritt 3 zurückkehren und den nächsten Typ, der vom Reader aufgelistet wird, testen.
8.  Wiedergabe wird gestartet. Der Reader ignoriert Ausgabepuffer aus dem DMO-Decoder, wenn der Verbindungs Ausgabetyp DirectX VA ist.
9.  Wenn **IPin::D isconnect** auftritt, ruft der Quell Filter **iwmcodecamvideoaccelerator:: setacceleratorinterface** mit einem **null**-Wert auf. Dadurch wird die DirectX-VA-Verbindung zwischen dem Codec und dem Renderer unterbrochen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




