---
title: Ausgabeeinstellungen
description: Ausgabeeinstellungen
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- Windows Media-Format-SDK, globale Konstanten
- Advanced Systems Format (ASF), globale Konstanten
- ASF (Advanced Systems Format), globale Konstanten
- Globale Konstanten, Liste der
- Windows Media-Format-SDK, Konstanten
- Advanced Systems Format (ASF), Konstanten
- ASF (Advanced Systems Format), Konstanten
- Konstanten, Liste der
- Windows Media-Format-SDK, Ausgabeeinstellungen
- Advanced Systems Format (ASF), Ausgabeeinstellungen
- ASF (Advanced Systems Format), Ausgabeeinstellungen
- Ausgabeeinstellungen
- synchrone Reader, Ausgabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5a02d508f76057dd72e34558a7ca8d29de4847
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101234"
---
# <a name="output-settings"></a>Ausgabeeinstellungen

Die folgenden globalen Konstanten werden verwendet, um Ausgabeeinstellungen für das Reader-und das synchrone Reader-Objekt zu identifizieren.



| Globale Konstante                | WMT \_ attr- \_ DataType  | Beschreibung von *pValue*                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszzuzugwinterlacedoutput    | **WMT- \_ Typ \_ bool**  | True gibt an, dass der Reader Zeilen Sprung Frames bereitstellt, wenn dies von der Ausgabe unterstützt wird.                                                                                                                                                                                                                                            |
| g \_ wszdediereddeliverythread  | **WMT- \_ Typ \_ bool**  | True gibt an, dass für diese Ausgabe ein dedizierter Thread erstellt wird, der für die Übermittlung der Beispiele erstellt wurde. Wird für den synchronen Reader nicht unterstützt.                                                                                                                                                                                            |
| g \_ wszdeliveronreceive         | **WMT- \_ Typ \_ bool**  | True gibt an, dass die Beispiele für diese Ausgabe übermittelt werden, sobald Sie vom Reader verfügbar sind. Dies kann dazu führen, dass Beispiele aus dieser Ausgabe nicht in der richtigen Reihenfolge und vor den entsprechenden Beispielen aus anderen Ausgaben zugestellt werden.                                                                                            |
| g \_ wszdynamicrangecontrol      | **WMT- \_ Typ \_ DWORD** | Gibt die Ebene des dynamischen Bereichs Steuer Elements an, das für die Ausgabe verwendet werden soll. Legen Sie auf einen Wert zwischen 0 und 2 fest, wobei 0 auf kein dynamisches Bereichs Steuerelement (Standard) und 2 die maximale Ebene des dynamischen Bereichs Steuer Elements (der kleinste dynamische Bereich) angibt.                                                                                |
| g \_ wszearlydatadelivery        | **WMT- \_ Typ \_ DWORD** | Zeit (in Millisekunden), die angibt, wie viel früher die Stichproben bereitstellt. Wenn dieser Wert größer als 0 (null) ist, werden die Beispiele aus dieser Ausgabe abgerufen und decodiert, sodass die Beispiele vor den Beispielen für andere Ausgaben übermittelt werden. Normalerweise liefert der Reader Beispiele in der Reihenfolge der Präsentationszeit.         |
| g \_ wszene ablediskreteoutput     | **WMT- \_ Typ \_ bool**  | True gibt an, dass der Reader die hochauflösende Multichannel-Audioausgabe aktiviert. Diese Einstellung ist nur für Audiostreams gültig, die mit dem Windows Media Audio 9 Professional-Codec codiert sind. Wenn diese Einstellung auf true festgelegt ist, müssen Sie auch die Sprecher Konfiguration des Client Computers angeben, indem Sie g \_ wszspeakerconfig festlegen. |
| g \_ wszene ableframeinterpolations | **WMT- \_ Typ \_ bool**  | True gibt an, dass der Codec den Videostream mit einer höheren [*Framerate*](wmformat-glossary.md)bereitstellt, wobei die Frames algorithmisch interpolieren werden.                                                                                                                                                          |
| g \_ wszjustintimedecode         | **WMT- \_ Typ \_ bool**  | True gibt an, dass die Daten so spät wie möglich decodiert werden müssen. Wird im synchronen Reader nicht unterstützt.                                                                                                                                                                                                                            |
| g \_ wszneeditvioussample      | **WMT- \_ Typ \_ bool**  | Wenn der Wert true ist, muss das vorherige Beispiel für das Beispiel entpackt werden. Diese Einstellung gilt nur für Delta Frames in komprimiertem Video und ist schreibgeschützt.                                                                                                                                                                       |
| g \_ wszscrambledaudio           | **WMT- \_ Typ \_ bool**  | Wenn der Wert true ist, wird für diese Ausgabe das abgeblichungs Schema der Debugmeldung verwendet. Dies ist eine gültige Einstellung nur für Audioausgaben.                                                                                                                                                                                                |
| g \_ wszsingleoutputbuffer       | **WMT- \_ Typ \_ bool**  | True gibt an, dass ein einzelner Ausgabepuffer verwendet werden muss (z. b. eine DirectDraw-® Video Puffer). Wird im synchronen Reader nicht unterstützt.                                                                                                                                                                                           |
| g \_ wszsoftwareskalierung          | **WMT- \_ Typ \_ bool**  | Bei "false" wird das Video nicht skaliert. (Es müssen keine Änderungen an der Auflösung vorgenommen werden.)                                                                                                                                                                                                                                                |
| g \_ wszspeakerconfig            | **WMT- \_ Typ \_ DWORD** | Wenn die Multichannel-Audiodecodierung durch Festlegen von g \_ wszene ablediskreteoutput aktiviert ist, gibt diese Einstellung die Sprecher Konfiguration des Client Computers an. Legen Sie auf eine der DirectSound-Sprecher Konfigurations Konstanten fest.                                                                                                   |
| g \_ wszstreamlanguage           | **WMT \_ - \_ typwort**  | Der Index in der Sprachliste der Sprache, die für diese Ausgabe übermittelt werden soll. Wird für Ausgaben verwendet, die nach Sprache ausschließende Datenströme darstellen.                                                                                                                                                                      |
| g \_ wszvideosampledurations     | **WMT- \_ Typ \_ bool**  | True gibt an, dass der Reader genaue Stichproben Dauer bereitstellt.                                                                                                                                                                                                                                                                |
| g \_ wszene ablewmaprospdif Output  | **WMT- \_ Typ \_ bool**  | True gibt an, dass der Reader das digitale Schnittstellen Format (S/PDIF) von Sony/Phillips in die enumerierten Ausgabetypen einschließt.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReaderAdvanced2:: getoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting)
</dt> <dt>

[**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Iwmsynkreader:: getoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting)
</dt> <dt>

[**Iwmsynkreader:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting)
</dt> </dl>

 

 




