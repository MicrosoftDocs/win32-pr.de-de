---
description: VMR mit mehreren Streams (Mischungs Modus)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR mit mehreren Streams (Mischungs Modus)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21a954b0ad78afbceabf0fde493f920961b90dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358572"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR mit mehreren Streams (Mischungs Modus)

VMR kann mehrere Eingabestreams Rendering. In dieser Konfiguration, dem sogenannten Mischungs Modus, lädt der VMR seinen Mixer und den Compositor, um vor dem Rendering die Mischung und die Mischung auszuführen. Der Mischungs Modus kann verwendet werden, während sich der VMR im Fenstermodus oder im fensterlosen Modus befindet.

Der Mischungs Modus erfordert, dass der Grafiktreiber die ddcaps \_ bltfourcc-und ddcaps \_ bltstretch-funktionsflags (Farb Raum Konvertierung bzw. Stretch-blierung) unterstützt. Fast alle neuen Grafiktreiber verfügen über diese Funktionen. Außerdem muss der Treiber die Erstellung von Direct3D-Renderingzielen für die aktuelle Anzeige Pixel Tiefe unterstützen. Einige Geräte unterstützen keine Direct3D-Vorgänge, wenn die Anzeige auf 24 Bits pro Pixel festgelegt ist. Weitere Informationen finden Sie in der Dokumentation zum DirectX-Grafik-SDK.

> [!Note]  
> Wenn VMR mehrere Videostreams vermischt, sucht das Filter Diagramm nicht ordnungsgemäß. Wenn Sie mehrere Videostreams suchen müssen, müssen Sie separate Filter Diagramme erstellen, die dasselbe benutzerdefinierte "zuordcator-Presenter"-Objekt verwenden.

 

**Konfigurieren von VMR-7 für mehrere Streams**

Gehen Sie folgendermaßen vor, um mehrere Eingabedaten Ströme mit VMR-7 zu erzeugen:

1.  Bevor Sie eine Verbindung mit den Eingabe Pins von VMR herstellen, können Sie die [**ivmrfilterconfig:: setnumofstreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) -Methode mit der Anzahl der Streams aufrufen. Dies bewirkt, dass der VMR den Mixer und den Compositor lädt und die angegebene Anzahl von Eingabe Pins erstellt.
2.  Rufen Sie [**ivmrfilterconfig:: strenderingprefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) auf, um verschiedene renderingeinstellungen anzugeben.
3.  Verbinden Sie die Pins mit den upstreamfiltern. Dies lässt sich am einfachsten durchführen, indem Sie für jeden Eingabestream [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) aufruft. Wenn die Ausgabepin auf dem upstreamfilter (in der Regel ein Decoder) und die Eingabe-PIN in der VMR für eine Verbindung nicht übereinstimmen, wird eine neue Instanz von VMR mit Standardeinstellungen erstellt. Dies führt zu einem neuen Fenster mit "ActiveMovie" in der Titelleiste. Um dies zu verhindern, sollte die Anwendung immer überprüfen, ob die richtige Instanz von VMR durch Aufrufen einer Methode wie [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)verwendet wird. Eine weitere Möglichkeit besteht darin, den Quell Filter hinzuzufügen und dann die Pins mithilfe von **igraphbuilder:: Connect** zu verbinden.
4.  Verwenden Sie die [**ivmrmixercontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) -Schnittstelle für den VMR, um Parameter für jeden Stream zu steuern, z. b. den Alpha-Wert, die Z-Reihenfolge und das Ausgabe Rechteck.
5.  Führen Sie das Filter Diagramm aus.

**Konfigurieren von VMR-9 für mehrere Streams**

Standardmäßig erstellt VMR-9 vier Eingabe Pins. Wenn Sie mehr als vier Videostreams kombinieren möchten, müssen Sie vor dem Verbinden von Eingabe Pins [**IVMRFilterConfig9:: setnumofstreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) aufrufen. Verwenden Sie die [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) -Schnittstelle zum Festlegen der StreamParameter, wie Z. b. Alpha, Z-Reihenfolge und Position.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



