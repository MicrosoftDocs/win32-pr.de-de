---
description: Konfigurieren der Video Codierung
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Konfigurieren der Video Codierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd82240ea9f540f283e0fb6340c06be00336226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127949"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Konfigurieren der Video Codierung (Microsoft Media Foundation)

Um den Video Encoder zu konfigurieren, führen Sie die folgenden Schritte aus:

1.  Legen Sie mithilfe von **IPropertyBag:: Write** alle Eigenschaften für den Encoder DMO fest. In der folgenden Liste wird der minimale Satz von Eigenschaften zusammengefasst, die zum Codieren eines CBR-Videostreams erforderlich sind (alle diese Werte haben Standardwerte, die verwendet werden können):

    -   Die[mfpkey \_ videowindow](mfpkey-videowindowproperty.md) -Eigenschaft gibt das Puffer Fenster an, das für den Datenstrom verwendet werden soll. Weitere Informationen zur Einstellung "Buffer Windows" und deren Auswirkungen auf den Inhalt finden Sie unter [Codierungs Methoden](encodingmethods.md). Das Standard Puffer Fenster beträgt drei Sekunden, was für viele Szenarien geeignet ist.
    -   Die Video Komplexität ist so festgelegt, dass der Kompromiss zwischen der Qualität des codierten Inhalts und der Zeit, die zum Codieren erforderlich ist, festgelegt wird. Wenn Sie keinen Wert festlegen, wird der Standardwert verwendet. Sie können jedoch die empfohlenen Modi für einen bestimmten Codec ermitteln, indem Sie [iwmcodec-Eigenschaften:: getcodecprop](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) aufrufen, um g \_ wszwmvccomplexityexlive, g \_ wszwmvccomplexityexoffline und g \_ wszwmvccomplexityexmax abzurufen. Anschließend können Sie [mfpkey \_ complexityex](mfpkey-complexityexproperty.md) auf einen Wert zwischen 0 und der gemeldeten maximalen Komplexität festlegen.
    -   [Mfpkey \_ Mit Crisp](mfpkey-crispproperty.md) wird die relative Wichtigkeit der Video Glätte und die Bildqualität codierter Frames angegeben. In den meisten Fällen funktioniert der Standardwert einwandfrei.
    -   Für Videoinhalte, die in einem anderen Container als "ASF" gespeichert sind, muss die Eigenschaft " [mfpkey \_ asfoverheadperframe](mfpkey-asfoverheadperframeproperty.md) " auf "0" festgelegt werden. Dies ist nicht der Standardwert.

    Weitere Informationen zum Konfigurieren von VBR-Streams finden [Sie unter Verwenden der VBR-Codierung](usingvbrencoding.md).

2.  Konfigurieren Sie die [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur für den Eingabetyp, oder verwenden Sie bei Verwendung des Media Foundation SDK die Funktion [**mfinitmediatypfromvideoinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) . Verwenden Sie eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur, die den unkomprimierten Eingabe Inhalt beschreibt. Der Codec ändert nicht die Größe des Videos oder konvertiert den Farb Raum.
3.  Legen Sie den Eingabetyp mithilfe von [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) oder [**IMF Transform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)fest.
4.  Konfigurieren Sie den Ausgabetyp für den Encoder. Nachdem der Eingabetyp festgelegt wurde, listet der Encoder die ausgegebene Ausgabetypen auf, ausgenommen den **dwbitrate** -Member der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur oder das [**MF \_ MT \_ AVG- \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut der [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle. Wenn Sie einen Ausgabetyp abrufen, bevor Sie einen Eingabetyp festlegen, wird der übermittelten [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur kein **videoinfoheader** zugeordnet.
5.  Rufen Sie die privaten Codec-Daten ab, und fügen Sie Sie an die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur an, die Sie an die [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur oder an [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)übergeben. Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md).
6.  Legen Sie den Ausgabetyp fest, indem Sie die [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) -Methode oder die [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode aufrufen. Übergeben Sie entweder die [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur mit der abgeschlossenen [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur (einschließlich angefügter privater Daten), auf die im **pbformat** -Member verwiesen wird, oder erstellen Sie einen [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) durch Aufrufen von [**mfinitmediatypfromvideoinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> Das Video Encoder-Objekt unterstützt zwei Ausgaben. Die zweite Ausgabe ist für den Encoder "Post View". Es werden die nicht komprimierten Beispiele bereitgestellt, die vom Decoder übermittelt werden. Dies ermöglicht es Ihnen, die Qualität der Codierung zu überwachen, ohne zu warten, bis der gesamte Stream verarbeitet wird. Diese Ausgabe ist optional. Wenn Sie diese verwenden möchten, konfigurieren Sie Ihren Typ nach dem gleichen Prozess, der auch zum Festlegen des encodereingabetyps verwendet wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 
