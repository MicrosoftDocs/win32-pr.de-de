---
title: Aktivieren der DirectX-Videobeschleunigung
description: Aktivieren der DirectX-Videobeschleunigung
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows Medienformat-SDK, Aktivieren von DXVA
- Windows Medienformat-SDK, DirectX-Videobeschleunigung (DXVA)
- Windows Medienformat-SDK, Videobeschleunigung
- Advanced Systems Format (ASF), aktivieren von DXVA
- ASF (Advanced Systems Format), aktivieren von DXVA
- Advanced Systems Format (ASF), DirectX Video Acceleration (DXVA)
- ASF (Advanced Systems Format), DirectX Video Acceleration (DXVA)
- Advanced Systems Format (ASF), Videobeschleunigung
- ASF (Advanced Systems Format), Videobeschleunigung
- DirectX Video Acceleration (DXVA), aktivieren
- DXVA (DirectX-Videobeschleunigung),aktivieren
- DirectX Video Acceleration (DXVA), Reihenfolge der Vorgänge
- DXVA (DirectX-Videobeschleunigung), Reihenfolge der Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840549c9a148fdfe8cc67daf46645ffb0925369057fe71f0c17217bfd36823ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930758"
---
# <a name="enabling-directx-video-acceleration"></a>Aktivieren der DirectX-Videobeschleunigung

In diesem Abschnitt wird beschrieben, wie Sie die Microsoft® DirectX® Videobeschleunigung beim Wiedergeben von gestreamten Inhalten in einem benutzerdefinierten Player aktivieren.

## <a name="background"></a>Hintergrund

DirectX Video Acceleration (DirectX VA) ist eine API-Spezifikation für die Hardwarebeschleunigung von 2D-Decodierungsvorgängen. Dadurch können Softwaredecoder bestimmte CPU-intensive Vorgänge zur Verarbeitung auf die Grafikkarte auslagern. Für Endbenutzer ermöglicht dies Video mit hoher Bitrate, z. B. die Vollbild-DVD-Wiedergabe auf älteren Computern, die mit DirectX VA-kompatiblen Grafikkarten ausgestattet sind.

Ab dem Windows Media Format 9 Series SDK unterstützt der filter DMO Wrapper DirectX VA. Dies bedeutet, dass Anwendungen für die lokale Wiedergabe den WM ASF-Readerfilter verwenden können, um Windows medienbasierten Inhalt wiederzugeben, und die DirectX VA-Hardwarebeschleunigung wird automatisch aufgerufen, wenn die Grafikkarte dies unterstützt. Der WM ASF-Readerfilter unterstützt jedoch keine Wiedergabe von gestreamten Inhalten. Wenn Sie directX VA beim Wiedergeben von gestreamten Inhalten in einem benutzerdefinierten Player unterstützen möchten, müssen Sie daher einen alternativen Mechanismus verwenden, der von Windows Media Player ab der Windows Media 9-Serie verwendet wird.

Da Windows Media Player vor der Entwicklung der QASF-Filter entworfen wurde, verfügt Windows Media Player über einen eigenen Quellfilter, der auf dem Windows Medienformat-SDK basiert, um Windows medienbasierten Inhalt wiedergeben zu können. Der WMP-Windows Medienquellenfilter übermittelt dekomprimierte Daten direkt an die Audio- und Videorenderer. Im Gegensatz dazu übermittelt der WM ASF Reader komprimierte Inhalte downstream an die directX-Medienobjekte (DirectX Media Objects, DMOs) des Windows-Mediendecoders, die im DMO Wrapper gehostet werden. Die folgenden Diagramme veranschaulichen die Unterschiede zwischen dem WM ASF-Reader und dem WMP-Windows Medienquellenfilter.

![Benutzerdefinierter Quellfilter gibt unkomprimierte Beispiele aus.](images/wmp-dxva-graph.png)

![Qasf-Quellfilter gibt komprimierte Beispiele aus](images/qasf-dxva-graph.png)

Um DirectX VA für gestreamten Inhalt zu aktivieren, müssen Sie einen benutzerdefinierten Quellfilter wie den im oberen Diagramm erstellen. Im Grunde verwendet dieser Filter das Windows Media Format SDK, um ein WM Reader-Objekt zu instanziieren, die Beispiele zu dekomprimieren und sie downstream an die Ausgabepins zu senden. In dieser Erläuterung wird davon ausgegangen, dass Sie den Quellfilter bereits erstellt haben und nun bereit sind, die DirectX-Va-Unterstützung zu implementieren.

Um DirectX VA zu aktivieren, besteht die grundlegende Aufgabe des Quellfilters darin, den Videorenderer und den WMV-Decoder DMO mit den Schnittstellen bereitzustellen, die sie zum Aushandeln der DirectX VA-Verbindung benötigen. Der Quellfilter nimmt nicht an diesen Handlungen teil. Nachdem das Streaming gestartet wurde, kann der Quellfilter nur die Zeitstempel der Videobeispiele ändern, bevor sie vom WMV-Decoder an den Videorenderer übermittelt werden. Der Hauptgrund hierfür ist die Bereitstellung einer benutzerdefinierten Zeitachsensteuerung, die über die standardmäßigen DirectShow®schnittstellen hinausgeht.

Es werden drei Schnittstellen definiert, um die erforderliche Kommunikation zwischen dem Windows Media Format SDK, dem Quellfilter des Players, dem Windows Media Video-Decoder DMO und dem Overlay Mixer oder Video Mixing Renderer zu ermöglichen. Diese Schnittstellen werden in der folgenden Tabelle beschrieben.



| Schnittstelle                                                        | BESCHREIBUNG                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Wird vom Windows Mediendecoder verfügbar gemacht DMO und vom Quellfilter eines Medienplayers aufgerufen, um die verschiedenen Verbindungen einzurichten, die erforderlich sind, um DirectX VA für die Decodierung von Windows Media Video-Inhalten zu aktivieren. |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Implementiert für den Quellfilter des Players. Sie ermöglicht es dem Filter, die Zeitstempel der Videobeispiele zu ändern, bevor sie nachgeschaltet werden.                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Implementiert für das WM-Reader-Objekt. Er wird von einem Playerquellfilter aufgerufen, um Schnittstellen aus dem Decoder DMO abzurufen.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Reihenfolge der Vorgänge in directX VA-fähiger Wiedergabe

In diesem Abschnitt wird die allgemeine Reihenfolge der Vorgänge zur Laufzeit für einen DirectX VA-fähigen Player und dessen Quellfilter beschrieben. Die komponenten, auf die in diesem Abschnitt verwiesen wird, sind:

-   Ein Media Player eines Drittanbieters, der als Player bezeichnet wird.
-   Ein benutzerdefinierter Quellfilter, der vom Player instanziiert wird und das Windows Media Format SDK verwendet, um Windows medienbasierten Inhalt zu dekomprimieren.
-   Der Videoausgabepin des Quellfilters des Players, der als Ausgabepin bezeichnet wird.
-   Das DirectShow-Videowiedergabefilterdiagramm, das als Graph bezeichnet wird.
-   Der Videomischungsrenderer, der als VMR bezeichnet wird.
-   Das Windows Media Format SDK-Objekt für den asynchronen Reader, das als Reader bezeichnet wird.
-   Das Windows Media Video Decoder DirectX Media Object, das als Decoder DMO bezeichnet wird.

Die Reihenfolge der Vorgänge lautet wie folgt:

1.  Der Player instanziiert seinen Quellfilter und ein Readerobjekt. Der Reader erstellt einen Videodecoder DMO und legt den (komprimierten) Eingabetyp darauf fest. Dies muss geschehen, bevor der Player versucht, seinen Videowiedergabegraphen zu konfigurieren, da das SDK und der Decoder DMO am Aushandlungsprozess mit dem Diagramm beteiligt sein müssen und die DMO das Eingabeformat in Schritt 9 kennen müssen.
2.  Der Player ruft **IGraphBuilder::Render** auf und stellt den Ausgabepin des Videoquellfilters bereit. An diesem Punkt versucht der DirectShow-Filtergraph-Manager, die VMR mit dem Videoquellfilter des Players zu verbinden.
3.  Der Filtergraph-Manager ruft **IPin::Verbinden** auf dem Ausgabepin des Videoquellfilters des Players auf.

Die Schritte 4 bis 10 finden in **IPin::Verbinden** statt.

1.  Der Quellfilter ruft die **IWMCodecAMVideoAccelerator-Schnittstelle** von der **IWMReaderAccelerator::GetCodecInterface-Methode** des Readers ab. Wenn der Codec DirectX VA nicht unterstützt, schlägt der Aufruf von **GetCodecInterface** möglicherweise fehl. In diesem Fall wird die Aushandlung wie gewohnt ohne DirectX VA-Unterstützung fortgesetzt.
2.  Der Quellfilter übergibt den **IAMVideoAccelerator-Zeiger** vom Pin, der an **Verbinden** übergeben wird, an den Decoder DMO über **IWMCodecAMVideoAccelerator::SetAcceleratorInterface**.
3.  Der Quellfilter delegiert dann den Rest des **IPin::Verbinden-Vorgangs** an die **CBaseOutputPin::Verbinden-Methode.** Die Formatenumeration mit dem SDK wird wie heute fortgesetzt. Wenn der Codec DirectX VA für den Inhalt unterstützt, der verbunden wird, stellt der Codec DMO diese DirectX VA-Untertypen zuerst vor den unterstützten YUV- und RGB-Typen dar. Wenn DirectX VA-Unterstützung verfügbar ist, werden die Schritte 7 bis 11 im Kontext eines DirectX VA-Untertyps versucht. Der folgende Codeausschnitt zeigt, wie Sie einen DirectX VA-Medienuntertyp identifizieren.
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

    

4.  Die **CBaseOutputPin::Verbinden-Implementierung** ruft **IPin::CompleteConnect** während Schritt 3 auf. Wenn ein DirectX VA-Untertyp berücksichtigt wird, wird versucht, die DirectX-VA-Aushandlung zu versuchen. Der Ausgabepin ruft **IWMCodecAMVideoAccelerator::NegotiateConnection** auf und übergibt ihm den aktuellen Ausgabemedientyp.
5.  Der Decoder DMO führt die erforderliche Aushandlung mit der VMR über die **IAMVideoAccelerator-Schnittstelle** durch und gibt die Videountertyp-GUID zurück, auf die sich die beiden einigen. Der Ausgabepin delegiert alle **IAMVideoAcceleratorNotify-Aufrufe,** die während dieses Prozesses empfangen wurden, an die **IAMVideoAcceleratorNotify-Schnittstelle** des Decoders DMO, die auch über die **IWMReaderAccelerator::GetCodecInterface-Methode** abgerufen werden kann.
6.  Wenn **NegotiateConnection** erfolgreich ist, ruft der Ausgabepin **IWMCodecAMVideoAccelerator::SetPlayerNotify** mit einer **IWMPlayerTimestampHook-Schnittstelle** auf. Mit diesem Hook kann der Quellfilter die Zeitstempel der Stichproben aktualisieren, bevor sie an den Renderer übergeben werden.
7.  Der Quellfilter ruft **IWMReaderAccelerator::Notify** mit dem ausgehandelten Medientyp auf. Dadurch kann der Reader seine internen Variablen aktualisieren und einen Commit für DirectX VA durchführen. Dies ist die letzte Stelle, an der der Codec oder Reader fehlschlagen kann. Wenn einer der oben genannten Schritte fehlschlägt, sollte der Quellfilter zu Schritt 3 zurückkehren und den nächsten Typ ausprobieren, der vom Reader aufzählt wird.
8.  Die Wiedergabe beginnt. Der Reader ignoriert Ausgabepuffer aus dem Decoder DMO, wenn der Verbindungsausgabetyp DirectX VA ist.
9.  Wenn **IPin::D isconnect** auftritt, ruft der Quellfilter **IWMCodecAMVideoAccelerator::SetAcceleratorInterface** mit einem **NULL-Wert** auf. Dadurch wird die DirectX VA-Verbindung zwischen dem Codec und dem Renderer unterbrochen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




