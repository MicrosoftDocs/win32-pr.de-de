---
description: Verwenden der Windows Media Video 9,1-Image Kategorie
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Verwenden der Windows Media Video 9,1-Image Kategorie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361129"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Verwenden der Windows Media Video 9,1-Image Kategorie

Die Windows Media Video 9,1-Image Kategorie unterscheidet sich von den anderen Ausgabe Kategorien, die vom Windows Media Video 9-Encoder und-Decoder unterstützt werden. Anstatt nicht komprimiertes Video zu verarbeiten, werden spezielle Eingabe Beispiele benötigt, die aus strukturierten Transformations Daten bestehen, und gelegentlich RGB-Bitmapbilder, auf denen die Transformationen ausgeführt werden.

Der codierte Windows Media Video 9,1-Bildinhalt ist praktisch identisch mit regulärem Windows Media Video 9-codiertem Inhalt, wird aber durch seinen eigenen FourCC ("wmvp") identifiziert.

Der Encoder-Ausgabetyp für das Videobild wird auf genau dieselbe Weise wie standardmäßige Windows Media-Videos festgelegt, mit der Ausnahme, dass der Untertyp und die Komprimierungs Werte auf die Video bildbezeichner festgelegt werden müssen. Dies umfasst auch die Notwendigkeit, private Codec-Daten abzurufen und an die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur anzufügen. Weitere Informationen finden Sie unter [Konfigurieren der Video Codierung](configuringvideoencoding.md).

Die Eingabetyp Konfiguration für das Video Bild ähnelt der Eingabe Konfiguration auch den anderen Video Encodern. Sie können einen teilweise abgeschlossenen [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) aus dem Encoder abrufen, indem Sie [**imediaobject:: getinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)aufrufen, oder wenn Sie das Media Foundation SDK verwenden, indem Sie [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) aufrufen und den **DMO- \_ \_ Medientyp** mithilfe von [**mfcreateammediatypfrommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)abrufen. Anschließend legen Sie die Frame Größe und die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format Struktur so fest, wie Sie es bei Standard Videos tun würden. Wie beim Ausgabetyp müssen Sie sicherstellen, dass der Untertyp und die Komprimierungs Werte entsprechend festgelegt sind.

## <a name="creating-input-samples"></a>Erstellen von Eingabe Beispielen

Die Eingabe Beispiele für den videobildcodec sind strukturiert. Die Definition der für das Video Bild verwendeten Struktur und Konstanten ist nicht in den Windows Media Audio-und Videocodec-Schnittstellen enthalten. Diese Definitionen sind im SDK für den Windows Media-Format enthalten, und ihre Verwendung wird in der Dokumentation zum Windows Media-Format SDK ausführlich erläutert.

## <a name="decoding"></a>Decodierung

Es gibt keine besonderen Anforderungen für das Decodieren von Bildschirm Erfassungs Videos. Abgesehen von einem anderen Untertyp (mediasubtype \_ wmvp), der für die decodereingabe verwendet wird, ist der komprimierte Video Bild Datenstrom im Grunde mit einem Standard Windows Media Video Datenstrom identisch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 
