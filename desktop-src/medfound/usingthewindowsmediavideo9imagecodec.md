---
description: Verwenden der Windows Media Video 9.1-Bildkategorie
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Verwenden der Windows Media Video 9.1-Bildkategorie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c630be78ec3edef1a47322b31f6a2331f15134a0cdffa4107b5a79daa86e9091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972629"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Verwenden der Windows Media Video 9.1-Bildkategorie

Die Windows Media Video 9.1-Bildkategorie ist anders als die anderen Ausgabekategorien, die vom Windows Media Video 9-Encoder und -Decoder unterstützt werden. Anstatt unkomprimierte Videos zu verarbeiten, werden spezielle Eingabebeispiele verwendet, die aus strukturierten Transformationsdaten und gelegentlich RGB-Bitmapbildern bestehen, auf denen die Transformationen ausgeführt werden.

Der codierte Windows Media Video 9.1-Bildinhalt ist praktisch identisch mit regulären Windows Media Video 9-codierten Inhalten, wird jedoch durch einen eigenen FOURCC -Inhalt (WMVP) identifiziert.

Der Encoderausgabetyp für Videobilder wird auf die gleiche Weise wie standard Windows Media video festgelegt, mit der Ausnahme, dass der Untertyp und die Komprimierungswerte auf die Videobildbezeichner festgelegt werden müssen. Dies schließt die Notwendigkeit ein, private Codecdaten zu erhalten und an die [**VIDEOINFOHEADER-Struktur anfügen.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) Weitere Informationen finden Sie unter [Konfigurieren der Videocodierung.](configuringvideoencoding.md)

Die Eingabetypkonfiguration für Videobilder ähnelt auch der Eingabekonfiguration für die anderen Videoencoder. Sie können einen teilweise abgeschlossenen [**DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) aus dem Encoder abrufen, indem Sie [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)aufrufen, oder wenn Sie das Media Foundation SDK verwenden, indem Sie DURCH AUFRUFEN [**VONGESICHTTRANSFORM::GetInputAvailableType und**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) Abrufen des DMO MEDIA **\_ \_ TYPE** mithilfe von [**MFCreateAMMediaTypeFromMFMediaType .**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype) Anschließend legen Sie die Framegröße und die [**Formatstruktur VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) wie bei Standardvideos fest. Wie beim Ausgabetyp müssen Sie sicherstellen, dass der Untertyp und die Komprimierungswerte entsprechend festgelegt sind.

## <a name="creating-input-samples"></a>Erstellen von Eingabebeispielen

Die Eingabebeispiele für den Videobildcodec sind strukturiert. Die Definition der -Struktur und -Konstanten, die für Videobilder verwendet werden, ist nicht in den Windows Media Audio- und Videocodecschnittstellen enthalten. Diese Definitionen sind im Windows Media Format SDK enthalten, und ihre Verwendung wird in der Dokumentation zum Windows Media Format SDK vollständig erläutert.

## <a name="decoding"></a>Decodierung

Es gibt keine besonderen Anforderungen für die Decodierung von Bildschirmaufnahmevideos. Anders als bei einem anderen Untertyp (MEDIASUBTYPE WMVP), der für decoder-Eingaben verwendet wird, ist der komprimierte Videobildstream im Wesentlichen identisch mit einem Windows \_ Media Video-Stream.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 
