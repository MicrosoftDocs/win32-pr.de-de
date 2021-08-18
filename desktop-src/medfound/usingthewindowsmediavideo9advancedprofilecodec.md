---
description: Verwenden des Windows Media Video 9 Advanced Profile
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Verwenden des Windows Media Video 9 Advanced Profile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258c32f14d1a7a42e1450c8265e2a611bd17b3b92b98f5433c93b91251e299c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012170"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Verwenden des Windows Media Video 9 Advanced Profile

Die grundlegenden Videoverfahren, die im Abschnitt [Arbeiten mit Video](workingwithvideo.md) beschrieben werden, gelten auch direkt für das Windows Media Video 9 Advanced Profile. Es sind keine besonderen Prozeduren erforderlich.

Das Windows Media Video 9 Advanced Profile ist den Klassenbezeichnern CLSID \_ CWMV9EncMediaObject und CLSID \_ CWMVDecMediaObject zugeordnet. Der FOURCC-Wert für Medientypen, die diesen Codec verwenden, ist "WVC1".

Das Windows Media Video 9 Advanced Profile unterstützt alle gängigen Codierungsmodi sowie interlaced-Codierung, gemischte Interlaced- und progressive Codierung, Auflösungen, die sich von den Anzeigefunktionen unterscheiden, und Bereichsverringerungsfeatures. Ein weiteres Feature ist die Möglichkeit, Sequenz- und Framemetadaten im Bitstream selbst zu speichern. Zuvor musste die ASF- und Data Unit Extensions-API verwendet werden.

Die folgenden Eigenschaften des erweiterten Profils Windows Media Video 9, das mithilfe von Registrierungseinstellungen gesteuert werden kann, verfügen nicht über entsprechende **IPropertyBag-** oder **IPropertyStore-Zeichenfolgen:**

-   Dquant-Option.
-   Dquant-Stärke.
-   Überlappung erzwingen.
-   Motion Vector Cost-Methode.

## <a name="achieving-optimal-visual-quality"></a>Erzielen einer optimalen visuellen Qualität

Für die meisten Videodaten können Sie die [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft](mfpkey-compressionoptimizationtypeproperty.md) auf 1 festlegen, um mithilfe des erweiterten Profils von Windows Media Video 9 eine optimale visuelle Qualität zu erzielen.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Informationen zu den Windows Media Video 9 Advanced Profile Codecs

Die aktuelle Version des Windows Media Video 9 Advanced Profile-Codecs basiert auf dem SMPTE-Standard (Society of Motion Picture and Tv Engineers) für das erweiterte Profil VC-1 (SMPTE 421M). Dieser Codec ersetzt den früheren Codec von Windows auch als Windows Media Video 9 Advanced Profile-Codec bezeichnet, der durch den FOURCC-Code "WMVA" identifiziert wurde. Die vorherige Version des VC-1-Codecs wurde implementiert, bevor der erweiterte Profilstandard VC-1 abgeschlossen wurde, und wird nicht mehr unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> 
<dt>

[Verwenden der erweiterten Einstellungen des Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



