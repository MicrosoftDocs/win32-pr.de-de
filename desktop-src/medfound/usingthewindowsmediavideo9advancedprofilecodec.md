---
description: Verwenden des erweiterten Profils Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Verwenden des erweiterten Profils Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366545"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Verwenden des erweiterten Profils Windows Media Video 9

Die grundlegenden Video Prozeduren, die im Abschnitt [Arbeiten mit Videos](workingwithvideo.md) beschrieben werden, gelten auch direkt für das erweiterte Profil Windows Media Video 9. Es sind keine speziellen Prozeduren erforderlich.

Das erweiterte Profil Windows Media Video 9 ist mit den Klassen Bezeichner CLSID \_ CWMV9EncMediaObject und CLSID \_ cwmvdecmediaobject verknüpft. Der FourCC-Wert für Medientypen, die diesen Codec verwenden, ist "WVC1".

Das erweiterte Profil Windows Media Video 9 unterstützt alle gängigen Codierungs Modi sowie die Zeilen Sprung Codierung, gemischte und Progressive Codierung, Auflösungen, die sich von der Anzeige unterscheiden, sowie Bereichs Reduzierungs Features. Ein weiteres Feature ist die Möglichkeit, Sequenz-und Frame Metadaten im Bitstream selbst zu speichern. zuvor war hierfür die Verwendung der ASF-und der Dateneinheiten Erweiterungen-API erforderlich.

Die folgenden Eigenschaften des erweiterten Profils Windows Media Video 9, die mithilfe von Registrierungs Einstellungen gesteuert werden können, verfügen nicht über die entsprechenden **IPropertyBag** -oder **IPropertyStore** -Zeichen folgen:

-   DQuant-Option.
-   Die DQuant-Stärke.
-   Überlappende erzwingen.
-   Bewegungsvektor kostenmethode.

## <a name="achieving-optimal-visual-quality"></a>Erzielen optimaler visueller Qualität

Für die meisten Videodaten können Sie die Eigenschaft " [ \_ compressionoptimizationtype" von "mfpkey](mfpkey-compressionoptimizationtypeproperty.md) " auf "1" festlegen, um eine optimale visuelle Windows Media Video Qualität zu erzielen.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Informationen zu den vorherigen Windows Media Video 9 Advanced Profile Codecs

Die aktuelle Version von Windows Media Video 9 Advanced Profile Codec basiert auf dem erweiterten Profil "Society of Motion Picture and TV Engineers (SMPTE) Standard for VC-1 (SMPTE 421m)". Dieser Codec ersetzt den früheren Codec von Windows, der auch als "Windows Media Video 9 Advanced Profile Codec" bezeichnet wird, der durch den FourCC-Code "wmva" identifiziert wurde. Die vorherige Version des VC-1-Codecs wurde implementiert, bevor der erweiterte VC-1-Profil-Standard fertiggestellt wurde, und wird nicht mehr unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> 
<dt>

[Verwenden der erweiterten Einstellungen von Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



