---
description: VMR mit mehreren Streams (Gemischter Modus)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR mit mehreren Streams (Gemischter Modus)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f958d8c95372325229dffc1cc37aff579213c48940f93ad090d0fbd9359b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290780"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR mit mehreren Streams (Gemischter Modus)

Die VMR kann mehrere Eingabestreams rendern. In dieser Konfiguration, die als Mischungsmodus bezeichnet wird, lädt die VMR ihren Mixer und Compositor, um das Mischen und Mischen vor dem Rendering durchzuführen. Der Gemischtmodus kann entweder verwendet werden, während sich die VMR im Fenstermodus oder im fensterlosen Modus befindet.

Der Kombinationsmodus erfordert, dass der Grafiktreiber die DDCAPS \_ BLTFOURCC- und DDCAPS \_ BLTSTRETCH-Funktionsflags unterstützt (Farbraumkonvertierung bzw. Stretch-Blitting). Fast alle neuen Grafiktreiber verfügen über diese Funktionen. Darüber hinaus muss der Treiber die Erstellung von Direct3D-Renderzielen für die aktuelle Pixeltiefe der Anzeige unterstützen. Einige Geräte unterstützen keine Direct3D-Vorgänge, wenn die Anzeige auf 24 Bits pro Pixel festgelegt ist. Weitere Informationen finden Sie in der DirectX Graphics SDK-Dokumentation.

> [!Note]  
> Wenn die VMR mehrere Videostreams kombiniert, sucht das Filterdiagramm nicht ordnungsgemäß. Wenn Sie mehrere Videostreams suchen müssen, müssen Sie separate Filterdiagramme erstellen, die das gleiche benutzerdefinierte Allocator-Presenter-Objekt gemeinsam nutzen.

 

**Konfigurieren von VMR-7 für mehrere Streams**

Gehen Sie wie folgt vor, um mehrere Eingabestreams mit VMR-7 zu rendern:

1.  Bevor Sie eine Verbindung mit den Eingabepins der VMR herstellen, rufen Sie die [**IVMRFilterConfig::SetNumberOfStreams-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) mit der Anzahl der Streams auf. Dies bewirkt, dass die VMR den Mixer und den Compositor lädt und die angegebene Anzahl von Eingabepins erstellt.
2.  Rufen Sie [**IVMRFilterConfig::SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) auf, um verschiedene Renderingeinstellungen anzugeben.
3.  Verbinden die Pins an die Upstreamfilter an. Die einfachste Möglichkeit besteht darin, [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) für jeden Eingabestream aufzurufen. Wenn sich der Ausgabepin im Upstreamfilter (in der Regel ein Decoder) und der Eingabepin auf der VMR nicht auf eine Verbindung einigen können, wird eine neue Instanz der VMR mit Standardeinstellungen erstellt. Dies führt zu einem neuen Fenster mit "ActiveMovie" in der Titelleiste. Um dies zu verhindern, sollte die Anwendung immer überprüfen, ob die richtige Instanz der VMR verwendet wird, indem sie eine Methode wie [**IPin::ConnectedTo aufruft.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) Eine weitere Möglichkeit besteht darin, den Quellfilter hinzuzufügen und dann die Pins mithilfe von **IGraphBuilder::Verbinden** zu verbinden.
4.  Verwenden Sie die [**IVMRMixerControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) auf der VMR, um Parameter für jeden Stream zu steuern, z. B. den Alphawert, die Z-Reihenfolge und das Ausgaberechteck.
5.  Führen Sie das Filterdiagramm aus.

**Konfigurieren von VMR-9 für mehrere Streams**

Standardmäßig erstellt VMR-9 vier Eingabepins. Wenn Sie mehr als vier Videostreams mischen möchten, rufen Sie [**IVMRFilterConfig9::SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) auf, bevor Sie eine Verbindung mit Eingabepins herstellen. Verwenden Sie die [**IVMRMixerControl9-Schnittstelle,**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) um die Streamparameter wie Alpha, Z-Reihenfolge und Position festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Gemischtmodus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



