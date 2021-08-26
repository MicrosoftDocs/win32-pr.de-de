---
description: Verwenden der Video Mixer Steuerelemente
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Verwenden der Video Mixer Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72506a69cb1e3a8584a92cc7052541ffc210cd307073dece61f3a9d76a4c35d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887144"
---
# <a name="using-the-video-mixer-controls"></a>Verwenden der Video Mixer Steuerelemente

Der EVR-Mixer stellt mehrere Schnittstellen bereit, mit denen eine Anwendung steuern kann, wie der Mixer Videos verarbeitet. Diese Schnittstellen können entweder in DirectShow oder in Media Foundation.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BENUTZEROBERFLÄCHEVideoMixerBitmap-Schnittstelle**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)   | Alpha kombiniert ein statisches Bitmapbild in das Video.                                                                                                                                                                                          |
| [**BENUTZEROBERFLÄCHEVideoMixerControl-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) | Steuert, wie die EVR Videounterstreams gemischt.                                                                                                                                                                                                |
| [**BENUTZEROBERFLÄCHEVideoProcessor-Schnittstelle**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)       | Steuert die Farbanpassung, Bildfilter und andere Videoverarbeitungsfunktionen. Diese Schnittstelle bietet Zugriff auf funktionen, die vom Grafiktreiber implementiert werden, sodass die genauen Funktionen vom Grafiktreiber des Benutzers abhängen. |



 

Die richtige Methode zum Erhalten von Zeigern auf diese Schnittstellen hängt davon ab, ob Sie die DirectShow-Version der EVR oder die Media Foundation verwenden. Für die Media Foundation EVR hängt es auch davon ab, ob Sie die EVR direkt oder über die [Mediensitzung verwenden.](media-session.md) (In der Regel verwendet eine Anwendung die EVR über die Mediensitzung, nicht direkt.)

Gehen Sie wie folgt vor, um einen Zeiger auf eine dieser Schnittstellen zu erhalten:

1.  Hier erhalten Sie einen Zeiger auf [**die BENUTZEROBERFLÄCHEGetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) auf der EVR.

    -   Wenn Sie den DirectShow EVR-Filter verwenden, rufen Sie **QueryInterface für** den Filter auf.

    -   Wenn Sie die EVR-Mediensenke direkt verwenden, rufen Sie **QueryInterface** in der Mediensenke auf.

    -   Wenn Sie die Mediensitzung verwenden, rufen Sie **QueryInterface** für die Mediensitzung auf.

2.  Wenn Sie die Mediensitzung verwenden, warten Sie, bis die Mediensitzung das [MESessionTopologyStatus-Ereignis](mesessiontopologystatus.md) mit dem Statuswert MF \_ TOPOSTATUS \_ READY sendet. (Überspringen Sie diesen Schritt, wenn Sie die Mediensitzung nicht verwenden.)

3.  Rufen [**SieGEGetService::GetService auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) um die Mixerschnittstelle zu erhalten. Verwenden Sie den Dienstbezeichner MR \_ VIDEO \_ MIXER \_ SERVICE.

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Alphablending einer Bitmap in das Video

Sie können die [**BENUTZEROBERFLÄCHEVIDEOMixerBitmap verwenden,**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) um eine statische Bitmap während der Wiedergabe in das Video zu überblenden. Sie können die Bitmap auf einer Direct3D-Oberfläche speichern, die als **IDirect3DSurface9-Zeiger** angegeben ist, oder eine GDI-Bitmap verwenden.

Wenn Sie eine Direct3D-Oberfläche für die Bitmap verwenden, kann die Oberfläche Alphadaten pro Pixel enthalten, die verwendet werden, wenn der Mixer das Bild alphanumeriert. Alternativ können Sie einen Farbschlüssel definieren, d. b. eine einzelne Farbe, die unabhängig davon transparent ist, wo sie in der Bitmap angezeigt wird. Außerdem können Sie einen Alphawert angeben, der auf das gesamte Bild angewendet wird. Sie können auch ein Quellrechteck zum Zuschneiden der Bitmap und ein Zielrechteck festlegen, um die Bitmap innerhalb des Videoframes zu positionieren.

Rufen Sie ZUM Festlegen der Bitmap [**DEN Aufruf VON BITMAPVideoMixerBitmap::SetAlphaBitmap auf.**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap) Diese Methode verwendet einen Zeiger auf eine [**MFVideoAlphaBitmap-Struktur,**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) die die Bitmap und die Alphablendingparameter angibt. Beispielcode finden Sie im Referenzthema für die **SetAlphaBitmap-Methode.**

Nachdem Sie die Bitmap festgelegt haben, können Sie die Mischungsparameter, einschließlich der Quell- und Zielverschränkungen, aktualisieren, indem Sie [**DEN PARAMETERNVIDEOMixerBitmap::UpdateAlphaBitmapParameters aufrufen.**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters) Das Update wird auf den nächsten Videoframe wirksam. Das Video muss abspielt werden, damit das Update erfolgt. Sie können diese Methode verwenden, um einfache Animationen für die Bitmap durchzuführen. (Wenn Sie anspruchsvollere Effekte benötigen, sollten Sie einen benutzerdefinierten EVR-Mixer schreiben.)

Um die Bitmap zu löschen, rufen [**Sie DANNVideoMixerBitmap::ClearAlphaBitmap auf.**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap)

## <a name="controlling-substreams"></a>Steuern von Unterstreams

Der EVR kann einen oder mehrere Videounterstreams in den primären Videostream mischen. Um das Mischen von Unterstreams zu steuern, verwenden Sie [**die SCHNITTSTELLE ZUEIGERVideoMixerControl.**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)

-   Rufen [**Sie DANNVideoMixerControl::SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) auf, um die Position eines Unterstreams innerhalb des zusammengesetzten Videoframes zu festlegen.

-   Rufen [**Sie ZUEhmVideoMixerControl::SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) auf, um die Z-Reihenfolge für die Unterstreams zu festlegen. Der EVR zeichnet die Videostreams in der Reihenfolge ihrer Werte in der Z-Reihenfolge, beginnend mit 0 (null). Der primäre Videostream befindet sich immer an erster Stelle in der Z-Reihenfolge.

## <a name="video-processor-settings"></a>Videoprozessor-Einstellungen

Der EVR-Mixer verwendet die DirectX-Videobeschleunigung (DXVA), um die Videoverarbeitung für die Eingabestreams durchzuführen. Die genauen Verarbeitungsfunktionen hängen vom Grafiktreiber ab. Die Videoverarbeitungsfunktionen werden mithilfe der [**DXVA2 \_ VideoProcessorCaps-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) beschrieben. Ein bestimmter Satz von Funktionen wird als *Videoverarbeitungsmodus bezeichnet.* Jeder Modus wird durch eine GUID identifiziert. Eine Liste vordefinierter GUIDs finden Sie unter [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). Der Treiber kann zusätzliche herstellerspezifische GUIDs definieren, die verschiedene Kombinationen von Funktionen darstellen.

Gehen Sie wie folgt vor, um die unterstützten Modi und Funktionen der einzelnen Modi zu finden:

1.  Rufen [**SieGEGETService::GetService auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) um einen Zeiger auf die [**BENUTZEROBERFLÄCHE DES MIXERVideoProcessor zu**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) erhalten.

2.  Rufen [**Sie DEN MODUSVIDEOProcessor::GetAvailableVideoProcessorModes auf.**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes) Diese Methode gibt ein Array von GUIDs zurück, die die verfügbaren Videoprozessormodi identifizieren. Die Liste wird in absteigender Reihenfolge zurückgegeben. Der Modus mit der höchsten Qualität wird zuerst in der Liste angezeigt. Die Liste kann sich je nach Format des Videos ändern.

3.  Rufen Sie für jede GUID in der Liste [**DEN CALLVIDEOProcessor::GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) auf, um die Funktionen des entsprechenden Videoprozessormodus zu finden. Die -Methode füllt eine [**DXVA2 \_ VideoProcessorCaps-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) mit einer Beschreibung der Funktionen auf.

4.  Um einen Modus auszuwählen, rufen [**Sie DANNVideoProcessor::SetVideoProcessorMode auf.**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode) Andernfalls wählt der EVR automatisch einen Modus aus, wenn das Streaming beginnt. In diesem Fall können Sie [**DIE VIDEOProcessor::GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) aufrufen, um zu suchen, welcher Modus ausgewählt wurde.

Die meisten Felder in der [**DXVA2 \_ VideoProcessorCaps-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) beschreiben das Verhalten von Treibern auf niedriger Ebene und sind in einer typischen Anwendung nicht von Interesse. Die folgenden Felder sind höchstwahrscheinlich von Interesse:

-   **DeviceCaps**. Dieses Feld gibt an, ob die Videoverarbeitung in Hardware oder Software erfolgt und ob der Grafiktreiber ein älterer DXVA 1.0-Treiber ist.

-   **DeinterlaceTechnology**. Dieses Feld gibt einen Hinweis darauf, welche Deinterlacingqualität Sie erwarten können, wenn das Quellvideo verschachtelt ist.

-   **ProcAmpControlCaps**. Dieses Feld gibt an, welche Farbanpassungssteuerelemente verfügbar sind. Eine Liste der möglichen Farbanpassungen finden Sie unter [ProcAmp Einstellungen](procamp-settings.md). Wenn der Treiber keine Farbanpassung durchführen kann, ist dieses Feld 0 (null).

-   **VideoProcessorOperations**. Dieses Feld enthält Flags, die verschiedene Videoverarbeitungsfunktionen beschreiben. Zwei Flags von besonderer Wichtigkeit sind das DXVA2 \_ VideoProcess \_ SubStreams-Flag und das DXVA2 \_ VideoProcess \_ SubStreams-Flag. Mindestens eines dieser Flags muss vorhanden sein, damit der EVR Unterstreams in den Referenzvideostream mischen kann. Wenn keines der Flags vorhanden ist, ist die EVR auf einen Videostream beschränkt.

-   **NoiseFilterTechnology**. Dieses Feld gibt an, welche Rauschfilter vom Grafiktreiber unterstützt werden. Wenn der Treiber keine Rauschfilterung unterstützt, ist der Wert DXVA2 \_ NoiseFilterTech \_ Unsupported.

-   **DetailFilterTechnology**. Dieses Feld gibt an, welche Detailfilter vom Grafiktreiber unterstützt werden. Wenn der Treiber keine Rauschfilterung unterstützt, ist der Wert DXVA2 \_ DetailFilterTech \_ Unsupported.

## <a name="color-adjustment-and-image-filtering"></a>Farbanpassung und Bildfilterung

Der Grafiktreiber unterstützt möglicherweise die Farbanpassung (auch als Prozessvergrößerung oder *einfach* *ProcAmp* bezeichnet) und Bildfilterung. Wenn sie von der GPU ausgeführt wird, können Farbanpassung und Bildfilterung in Echtzeit ohne CPU-Mehraufwand erfolgen.

Führen Sie die folgenden Schritte aus, um diese Features zu verwenden:

1.  Wählen Sie einen Videoverarbeitungsmodus aus, wie im vorherigen Abschnitt beschrieben.

2.  Rufen [**Sie DIE VIDEOProzessor::GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) auf, um die Videoverarbeitungsfunktionen wie im vorherigen Abschnitt beschrieben zu finden. Die -Methode füllt eine [**DXVA2 \_ VideoProcessorCaps-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) aus, die die Funktionen beschreibt, einschließlich der Unterstützung der Farbanpassung und des Bildfilters durch den Treiber.

3.  Rufen Sie für jede farbanpassung, die vom Treiber unterstützt wird, [**DEN WERTVIDEOProcessor::GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) auf, um den möglichen Wertbereich für diese Einstellung zu finden. Diese Methode gibt auch den Standardwert für die Einstellung zurück. Rufen [**Sie AUF, UM DEN**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) aktuellen Wert der Einstellungen zu finden. Die Werte haben keine angegebenen Einheiten. Der Treiber muss den Wertebereich definieren.

4.  Rufen Sie ZUM Festlegen eines Farbanpassungswerts [**DEN WERT FÜR DIE FARBVIDEOPROCESSOR::SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) auf.

5.  Wenn der Treiber Bildfilterung unterstützt, unterstützt jeder Filtertyp (Rauschen und Detail) drei Einstellungen – Ebene, Radius und Schwellenwert – sowohl in Rauschen als auch in Luma. (Siehe [DXVA-Bildfilter Einstellungen](dxva-image-filter-settings.md).) Rufen Sie für jede Einstellung [**DIE VIDEOProcessor::GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) auf, um den Bereich der möglichen Werte zu erhalten, und rufen Sie [**DANNVideoProcessor::GetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) auf, um den aktuellen Wert zu erhalten.

6.  Um eine Bildfiltereinstellung zu ändern, rufen [**Sie DANNVideoProcessor::SetFilteringValue auf.**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 



