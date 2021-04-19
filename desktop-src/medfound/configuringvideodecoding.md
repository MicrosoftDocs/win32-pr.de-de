---
description: Konfigurieren der Video Decodierung
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Konfigurieren der Video Decodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343210"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Konfigurieren der Video Decodierung (Microsoft Media Foundation)

Die Decodierung ist im Grunde das Gegenteil der Codierung in Bezug auf die Konfiguration. Der Decoder unterstützt nur sehr wenige Eigenschaften, und keine davon ist erforderlich. Legen Sie den Eingabetyp auf den Typ fest, der für die decoderausgabe verwendet wird (einschließlich der privaten Codec-Daten) Legen Sie dann die Ausgabe auf das gewünschte nicht komprimierte Format fest, legen Sie die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur auf die richtige Frame Größe fest, und beginnen Sie mit der Verarbeitung von Beispielen.

Sie müssen den Decoder mit einem Medientyp bereitstellen, der die privaten Codec-Daten enthält, die unmittelbar nach der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur positioniert sind. Der Decoder kann den Inhalt ohne diese Daten nicht decodieren. Die vom Decoder ausgeführte Format Validierung überprüft nicht die privaten Daten. Wenn die privaten Codec-Daten fehlen oder falsch sind, antwortet der Decoder so, als ob der Bitstream beschädigt ist. Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 
