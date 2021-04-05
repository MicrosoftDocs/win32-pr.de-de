---
description: Verwenden der Video-Mixer-Steuerelemente
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Verwenden der Video-Mixer-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a062c6f984e0eac0128bd67c72bf691c95af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042039"
---
# <a name="using-the-video-mixer-controls"></a>Verwenden der Video-Mixer-Steuerelemente

Der EVR-Mixer bietet mehrere Schnittstellen, die eine Anwendung verwenden kann, um zu steuern, wie der Mixer Video verarbeitet. Diese Schnittstellen können entweder in DirectShow oder Media Foundation verwendet werden.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMF videomixerbitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) -Schnittstelle   | Alpha: kombiniert ein statisches Bitmap-Bild mit dem Video.                                                                                                                                                                                          |
| [**IMF videomixercontrol**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) -Schnittstelle | Steuert, wie das EVR Video-unter Ströme mischt.                                                                                                                                                                                                |
| [**IMF videoprocessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) -Schnittstelle       | Steuert Farbanpassung, Bild Filter und andere Video Verarbeitungsfunktionen. Diese Schnittstelle bietet Zugriff auf die Funktionalität, die vom Grafiktreiber implementiert wird, sodass die genauen Funktionen vom Grafiktreiber des Benutzers abhängen. |



 

Die richtige Methode, um Zeiger auf diese Schnittstellen zu erhalten, hängt davon ab, ob Sie die DirectShow-Version von EVR oder die Media Foundation Version verwenden. Für den Media Foundation EVR hängt es auch davon ab, ob Sie den EVR direkt verwenden oder über die [Medien Sitzung](media-session.md)verwenden. (In der Regel verwendet eine Anwendung den EVR über die Medien Sitzung, nicht direkt).

Um einen Zeiger auf eine dieser Schnittstellen zu erhalten, führen Sie folgende Schritte aus:

1.  Einen Zeiger auf die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle für den EVR erhalten.

    -   Wenn Sie den DirectShow-EVR-Filter verwenden, können Sie **QueryInterface** für den Filter aufzurufen.

    -   Wenn Sie die EVR-Medien Senke direkt verwenden, können Sie **QueryInterface** in der Medien Senke aufzurufen.

    -   Wenn Sie die Medien Sitzung verwenden, können Sie **QueryInterface** in der Medien Sitzung aufzurufen.

2.  Wenn Sie die Medien Sitzung verwenden, warten Sie, bis die Medien Sitzung das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) mit dem Statuswert MF \_ topostatus Ready sendet \_ . (Überspringen Sie diesen Schritt, wenn Sie die Medien Sitzung nicht verwenden.)

3.  Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) zum Abrufen der Mixer-Schnittstelle. Verwenden Sie den Dienst Bezeichner Mr- \_ Video- \_ Mixer- \_ Dienst.

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Alpha mischen einer Bitmap in das Video

Sie können die [**imfvideomixerbitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) -Schnittstelle verwenden, um während der Wiedergabe eine statische Bitmap auf das Video zu mischen. Sie können die Bitmap in einer Direct3D-Oberfläche speichern, die als **IDirect3DSurface9** -Zeiger angegeben ist, oder Sie verwenden eine GDI-Bitmap.

Wenn Sie eine Direct3D-Oberfläche für die Bitmap verwenden, kann die-Oberfläche pro Pixel-Alpha-Daten enthalten, die verwendet werden, wenn das Bild von der Mischung gemischt wird. Alternativ können Sie einen Farbschlüssel definieren, d. –. eine einzelne Farbe, die überall transparent ist, wo Sie in der Bitmap angezeigt wird. Außerdem können Sie einen Alphawert angeben, der auf das gesamte Bild angewendet wird. Sie können auch ein Quell Rechteck zum Zuschneiden der Bitmap und ein Ziel Rechteck festlegen, um die Bitmap innerhalb des Video Rahmens zu positionieren.

Um die Bitmap festzulegen, müssen Sie [**imfvideomixerbitmap:: setalphabitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap)aufrufen. Diese Methode nimmt einen Zeiger auf eine [**mfvideoalphabitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) -Struktur an, die die Bitmap und die Alpha Mischungs Parameter angibt. Beispielcode finden Sie im Referenz Thema für die **setalphabitmap** -Methode.

Nachdem Sie die Bitmap festgelegt haben, können Sie die Mischungs Parameter, einschließlich der Quell-und Ziel-recangles, durch Aufrufen von [**imfvideomixerbitmap:: updatealphabitmapparameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters)aktualisieren. Das Update wird im nächsten Video Frame wirksam. Das Video muss abgespielt werden, damit das Update stattfindet. Sie können diese Methode verwenden, um einfache Animationen auf der Bitmap auszuführen. (Wenn Sie anspruchsvollere Effekte benötigen, sollten Sie einen benutzerdefinierten EVR-Mixer schreiben.)

Um die Bitmap zu löschen, müssen Sie [**imfvideomixerbitmap:: clearalphabitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap)aufrufen.

## <a name="controlling-substreams"></a>Steuern von Substreams

Der EVR kann einen oder mehrere videosubstreams mit dem primären Videostream mischen. Um die substreammischung zu steuern, verwenden Sie die [**imfvideomixercontrol**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) -Schnittstelle.

-   Aufrufen von [**imfvideomixercontrol:: setstreamoutputrect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) , um die Position eines Substreams innerhalb des zusammengesetzten Video Rahmens festzulegen.

-   Aufrufen von [**imfvideomixercontrol:: setstreamzorder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) zum Festlegen der z-Reihenfolge für die unter Ströme. Der EVR zeichnet die Videostreams in der Reihenfolge ihrer z-Reihen folgen Werte, beginnend mit 0 (null). Der primäre Videostream ist immer an erster Stelle in der z-Reihenfolge.

## <a name="video-processor-settings"></a>Video Prozessor Einstellungen

Der EVR-Mixer verwendet die DirectX-Videobeschleunigung (DXVA), um die Videoverarbeitung in den Eingabestreams auszuführen. Die genauen Verarbeitungsfunktionen hängen vom Grafiktreiber ab. Die Video Verarbeitungsfunktionen werden mithilfe der [**DXVA2 \_ videoprocess orcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur beschrieben. Ein bestimmter Satz von Funktionen wird als *Video Verarbeitungsmodus* bezeichnet, wobei jeder Modus durch eine GUID identifiziert wird. Eine Liste der vordefinierten GUIDs finden Sie unter [**idirectxvideoprocess orservice:: getvideoprocess ordeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). Der Treiber kann zusätzliche anbieterspezifische GUIDs definieren, die verschiedene Kombinationen von Funktionen darstellen.

Gehen Sie folgendermaßen vor, um die unterstützten Modi und die Funktionen der einzelnen Modi zu ermitteln:

1.  Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , um einen Zeiger auf die [**imfvideoprocessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) -Schnittstelle des Mischers zu erhalten.

2.  Aufrufen von [**imfvideoprocessor:: getavailablevideoprocessormodes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes). Diese Methode gibt ein Array von GUIDs zurück, mit denen die verfügbaren Videoprozessor Modi identifiziert werden. Die Liste wird in absteigender Reihenfolge zurückgegeben. der Modus mit der höchsten Qualität wird zuerst in der Liste angezeigt. Die Liste kann je nach Format des Videos geändert werden.

3.  Für jede GUID in der Liste müssen Sie [**imfvideoprocessor:: getvideoprocessorcaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) aufrufen, um die Funktionen des entsprechenden Videoprozessor Modus zu ermitteln. Die-Methode füllt eine [**DXVA2 \_ videoprocess orcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur mit einer Beschreibung der Funktionen.

4.  Um einen Modus auszuwählen, nennen Sie [**imfvideoprocessor:: setvideoprocessormode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode). Andernfalls wählt der EVR automatisch einen Modus aus, wenn das Streaming beginnt. In diesem Fall können Sie [**imfvideoprocessor:: getvideoprocessormode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) aufrufen, um zu ermitteln, welcher Modus ausgewählt wurde.

Die meisten Felder in der [**DXVA2 \_ videoprocessorcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur beschreiben das Verhalten auf niedriger Ebene und sind in einer typischen Anwendung nicht von Interesse. Die folgenden Felder sind höchstwahrscheinlich von Interesse:

-   **Deaktiviert** werden. Dieses Feld gibt an, ob die Videoverarbeitung in Hardware oder Software erfolgt und ob es sich bei dem Grafiktreiber um einen älteren DXVA 1,0-Treiber handelt.

-   **Deinterlacetechnology**. Dieses Feld gibt Aufschluss darüber, welche Ebene der deinterlacingqualität Sie erwarten können, wenn das Quellvideo mit Zeilen Sprung verknüpft ist.

-   **Procampcontrolcaps**. Dieses Feld gibt an, welche Farb Anpassungs Steuerelemente verfügbar sind. Eine Liste der möglichen Farbanpassungen finden Sie unter [ProcAmp Settings](procamp-settings.md). Wenn der Treiber keine Farbanpassung durchführen kann, ist dieses Feld NULL.

-   **Videoprocess oroperations**. Dieses Feld enthält Flags, die verschiedene Video Verarbeitungsfunktionen beschreiben. Zwei Flags von besonderer Wichtigkeit sind das \_ Flag DXVA2 videoprocess \_ Substreams und das \_ Flag DXVA2 videoprocess \_ Substreams. Mindestens eines dieser Flags muss vorhanden sein, damit das EVR-Substreams in den Verweis Videostream mischen können. Wenn keines der Flags vorhanden ist, ist der EVR auf einen Videostream beschränkt.

-   **Noisefiltertechnology**. Dieses Feld gibt an, welche Rauschfilter vom Grafiktreiber unterstützt werden. Wenn der Treiber keine Rausch Filterung unterstützt, wird der Wert DXVA2 \_ noisefiltertech nicht \_ unterstützt.

-   **Detailfiltertechnology**. Dieses Feld gibt an, welche Detail Filter vom Grafiktreiber unterstützt werden. Wenn der Treiber keine Rausch Filterung unterstützt, wird der Wert DXVA2 \_ detailfiltertech nicht \_ unterstützt.

## <a name="color-adjustment-and-image-filtering"></a>Farbanpassung und Bildfilterung

Der Grafiktreiber unterstützt möglicherweise Farbanpassungen (auch als *Prozess Verstärkung* oder einfach *ProcAmp* bezeichnet) und Bildfilterung. Bei Durchführung durch die GPU können Farbanpassung und Bildfilterung in Echtzeit ohne CPU-Aufwand durchgeführt werden.

Führen Sie die folgenden Schritte aus, um diese Features zu verwenden:

1.  Wählen Sie einen Video Verarbeitungsmodus aus, wie im vorherigen Abschnitt beschrieben.

2.  Aufrufen von [**imfvideoprocessor:: getvideoprocessorcaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) , um die Video Verarbeitungsfunktionen zu finden, wie im vorherigen Abschnitt beschrieben. Die-Methode füllt eine [**DXVA2 \_ videoprocess orcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur aus, die die Funktionen beschreibt. Dies umfasst auch, ob der Treiber Farbanpassung und Bild Filter unterstützt.

3.  Für jede Farbanpassung, die vom Treiber unterstützt wird, müssen Sie [**imfvideoprocessor:: getprocamprange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) aufrufen, um den möglichen Wertebereich für diese Einstellung zu ermitteln. Diese Methode gibt auch den Standardwert für die Einstellung zurück. Wenn Sie [**imfvideoprocessor:: getprocampvalues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) aufrufen, finden Sie den aktuellen Wert der Einstellungen. Die Werte haben keine angegebenen Einheiten. Der Treiber muss den Wertebereich definieren.

4.  Aufrufen von [**imfvideoprocessor:: setfilteringvalue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) , um einen Farb Anpassungswert festzulegen.

5.  Wenn der Treiber die Bildfilterung unterstützt, unterstützt jeder Filtertyp (Rauschen und Details) drei Einstellungen – Ebene, Radius und Schwellenwert – sowohl in Chroma als auch in Luma. (Weitere Informationen finden Sie unter [DXVA Image Filter Settings](dxva-image-filter-settings.md).) Für jede Einstellung müssen Sie [**imfvideoprocessor:: getfilteringrange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) aufrufen, um den Bereich möglicher Werte abzurufen, und [**imfvideoprocessor:: getfilteringvalue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) aufrufen, um den aktuellen Wert zu erhalten.

6.  Um eine Bild Filtereinstellung zu ändern, wenden Sie [**imfvideoprocessor:: setfilteringvalue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue)an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 



