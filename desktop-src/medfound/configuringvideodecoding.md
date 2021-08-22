---
description: Konfigurieren der Videodecodierung
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Konfigurieren der Videodecodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7c49d42b47b4b6745731287e2b0bf0ee2d21c1eb503ed561274a5fb4cc8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035338"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Konfigurieren der Videodecodierung (Microsoft Media Foundation)

Die Decodierung ist im Wesentlichen das Gegenteil der Codierung in Bezug auf die Konfiguration. Der Decoder unterstützt nur sehr wenige Eigenschaften, und keine davon ist erforderlich. Legen Sie den Eingabetyp auf den Typ fest, der für die Decoderausgabe verwendet wird (einschließlich der privaten Codecdaten). Legen Sie dann die Ausgabe auf das gewünschte nicht komprimierte Format fest, legen Sie die [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) auf die richtige Framegröße fest, und beginnen Sie mit der Verarbeitung von Beispielen.

Sie müssen den Decoder mit einem Medientyp ausliefern, der die privaten Codecdaten enthält, die unmittelbar nach der [**VIDEOINFOHEADER-Struktur positioniert**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) sind. Der Decoder kann den Inhalt ohne diese Daten nicht decodieren. Die vom Decoder durchgeführte Formatüberprüfung überprüft die privaten Daten nicht. Wenn die privaten Codecdaten fehlen oder falsch sind, antwortet der Decoder so, als wäre der Bitstream beschädigt. Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden privater Videocodec-Daten](usingvideocodecprivatedata.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 
