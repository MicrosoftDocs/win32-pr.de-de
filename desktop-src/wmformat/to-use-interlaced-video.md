---
title: So verwenden Sie ein Zeilen Sprung Video
description: So verwenden Sie ein Zeilen Sprung Video
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media-Format-SDK, Zeilen Sprung Video
- Windows Media-Format-SDK, Videocodierung mit Zeilen Sprung
- Windows Media-Format-SDK, Codieren von verschachtelten Videos
- Windows Media-Format-SDK, Decodieren von Text mit Interlacing
- Windows Media-Format-SDK, Feld Reihenfolge
- Advanced Systems Format (ASF), Zeilen Sprung Video
- ASF (Advanced Systems Format), Zeilen Sprung Video
- Advanced Systems Format (ASF), Videocodierung mit Zeilen Sprung
- ASF (Advanced Systems Format), Video Encoding Interlacing
- Advanced Systems Format (ASF), Codieren von Zeilen Sprung Videos
- ASF (Advanced Systems Format), Codieren von Zeilen Sprung Videos
- Advanced Systems Format (ASF), Decodieren von interschnür Videos
- ASF (Advanced Systems Format), Decodieren von Zeilen Sprung Videos
- Advanced Systems Format (ASF), Feld Reihenfolge
- ASF (Advanced Systems Format), Feld Reihenfolge
- Zeilen Sprung Video, Info
- Zeilen Sprung Video, Codierung
- Zeilen Sprung Video, Decodierung
- Zeilen Sprung Video, Feld Reihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858015"
---
# <a name="to-use-interlaced-video"></a>So verwenden Sie ein Zeilen Sprung Video

Es gibt zwei grundlegende Arten der Videocodierung: progressiv und Zeilen Sprung. Bei progressiver Codierung ist jeder Frame eine codierte Darstellung eines Frame Videos. Bei der Zeilen Sprung Codierung ist jeder Frame eine codierte Darstellung von entweder allen geraden Zeilen des Videos oder allen ungeraden Zeilen. Jeder Zeilen Sprung Rahmen wird als *Feld* bezeichnet, sodass es ungerade Felder und sogar Felder gibt. Eine Zeilen Sprung Anzeige (z. b. ein Fernsehgerät) rendert die Felder einzeln und abwechselnd Felder. Eine progressive Anzeige rendert Frames alle gleichzeitig.

Das Windows Media Video 9 Advanced Profile Codec bietet Unterstützung für die Beibehaltung von interlacings in komprimierten Datenströmen.

## <a name="when-to-use-interlaced-video"></a>Verwendung von Zeilen Sprung Videos

Das Codieren von Zeilen Sprung Videos ist nur hilfreich, wenn der Inhalt auf einem Zeilen Sprung Gerät angezeigt wird. Inhalte, die in einem Fernsehgerät (über eine Top-Box oder ein anderes Gerät) angezeigt werden sollen, müssen möglicherweise mit Zeilen Sprung verknüpft werden. Inhalte, die ausschließlich auf einer Computer Anzeige angezeigt werden sollen, sollten nicht als Zeilen Sprung codiert werden.

Zum Codieren von überlappenden Videos als progressives Video müssen Sie die Eingabeeinstellungen konfigurieren. Weitere Informationen finden [Sie unter dem deinterlace-Video](to-deinterlace-video.md).

## <a name="field-order"></a>Feldreihenfolge

Bei den meisten Quellen mit Zeilen Sprung Video, z. b. Video Erfassungs Karten, werden Videobeispiele bereitstellt, die beide Felder miteinander verschachtelt sind. Das Ergebnis ähnelt einem kompletten Videorahmen, mit dem Unterschied, dass die ungeraden und geraden Zeilen etwas zeitgleich verschoben werden. Es gibt keinen universellen Standard, zu dem das Feld im überlappenden Video Beispiel erstmalig vorkommt.

Sie sollten es Benutzern ermöglichen, die Feld Reihenfolge anzugeben, wenn Sie überlappende Beispiele an die Anwendung übergeben.

## <a name="encoding-interlaced-video"></a>Codieren von interschnür Videos

Führen Sie die folgenden Schritte aus, um die Zeilen Sprung Codierung zu verwenden:

1.  Konfigurieren Sie den Videostream im Profil so, dass die Inhaltstyp-Dateneinheiten Erweiterung verwendet wird, indem Sie die [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) -Methode aufrufen. Die Beispiel Erweiterungs-GUID für die Inhaltstyp Erweiterung ist WM \_ sampleextensionsguid \_ ContentType.
2.  Legen Sie den Stream im Profil fest, und konfigurieren Sie den Writer wie gewohnt mit dem Profil.
3.  Bevor Sie Zeilen Sprung Beispiele an den Writer übergeben, müssen Sie die [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) -Methode aufzurufen, um die \_ Eingabe Einstellung g wszinterlacedcoding auf **true** festzulegen.
4.  Aufrufen Sie für jedes mit dem Writer übergebene Zeilen Sprung Beispiel die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode, um den Inhaltstyp festzulegen. Inhaltstyp Werte sind Kombinationen der Flags in der folgenden Tabelle.



| Flag                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zeilen Sprung mit \_ der WM-Geschwindigkeit \_           | Legen Sie dieses Flag immer fest, wenn Sie Zeilen Sprung Inhalt codieren. Wenn Sie dieses Flag verwenden, ohne ein Flag für die Feld Reihenfolge festzulegen ("WM \_ CT \_ Bottom \_ Field \_ First" oder "WM \_ CT \_ Top \_ Field First" \_ ), nimmt der Codec an, dass das oberste Feld zuerst ist. Wenn der Codec die falsche Feld Reihenfolge verwendet, sollte die Bildqualität nicht beeinträchtigt werden, aber die Codierungseffizienz wird beeinträchtigt. |
| letzte Zeile, \_ \_ \_ \_ erstes Feld | In Kombination mit dem "WM CT"- \_ \_ Zeilen Sprung Flag gibt dieses Flag an, dass das untere Feld (das Feld, das mit der zweiten Zeile im Beispiel beginnt) zum ersten Mal auftritt.                                                                                                                                                                                          |
| \_ \_ \_ erstes erstes Feld, \_ erstes Feld    | In Kombination mit dem "WM CT"- \_ \_ Zeilen Sprung Flag gibt dieses Flag an, dass das oberste Feld (das Feld, das mit der ersten Zeile im Beispiel beginnt) zum ersten Mal auftritt.                                                                                                                                                                                              |
| WM \_ CT \_ , \_ erstes \_ Feld wiederholen | Gibt an, dass das erste Feld im Beispiel bei der Wiedergabe wiederholt werden soll. Dieses Flag wird für Video verwendet, das vom telecine-Prozess aus dem Film erstellt wurde. Wenn kein Flag für die Feld Reihenfolge in Verbindung mit diesem Flag festgelegt wird, wird davon ausgegangen, dass das oberste Feld zum ersten Mal auftritt.<br/>                                                                             |



 

> [!Note]  
> Wenn das "WM CT"-Zeilen Sprung \_ \_ Flag nicht festgelegt ist, wird angenommen, dass das Beispiel einen progressiven Videorahmen enthält.

 

## <a name="decoding-interlaced-video"></a>Decodieren von interschnür Videos

Beim Decodieren von Videos mit Zeilen Sprung müssen Sie die \_ Einstellung "g wszzuweisung winterlacedoutput" mithilfe der [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) -Methode auf " **true** " festlegen. Andernfalls liefert der Codec progressive Frames.

Die-Inhaltstyp-Dateneinheiten Erweiterung wird in den Ausgabe Beispielen beibehalten. Sie sollten die Feld Ausrichtung an das renderinggerät übergeben, um eine ordnungsgemäße Wiedergabe sicherzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> </dl>

 

 





