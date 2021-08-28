---
description: Interlaced Video Encoding
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Interlaced Video Encoding (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15269aca3f2878504fef56c62b1a1d70ecd89295c237164ba864b15aaae371d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724390"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Interlaced Video Encoding (Microsoft Media Foundation)

Videodaten, die für die Verwendung mit Computern vorgesehen sind, sind in der Regel *progressiv.* Das bedeutet, dass jeder Frame als einzelnes Bild codiert ist. Einige Geräte, z. B. Fernsehgeräte, zeigen keinen Rahmen auf einmal an, sondern als zwei Bilder. Eines der Bilder oder Felder enthält alle gerade nummerierten Zeilen. Das andere Feld enthält die Daten für alle ungeraden nummerierten Zeilen. Video, das mit mehr als einem Feld pro Frame codiert ist, wird als interlaced bezeichnet, da es durch Wechseln zwischen dem geraden Feld und dem ungeraden Feld gerendert wird.

In der Vergangenheit wurden Interlacingvideoinhalte vor der Codierung mit dem Windows Media Video-Codec immer deinterlaced. Ab Windows Media 9-Serie unterstützt der Videoencoder jedoch die Komprimierung von interlaced-Inhalten, ohne sie zuerst in progressiv zu konvertieren. Das Beibehalten des Interlacings in einer codierten Datei ist wichtig, wenn der Inhalt jemals auf einer Interlacinganzeige gerendert wird, z. B. einem Fernsehgerät. Dieses Feature ist von zunehmender Bedeutung, da die Unterstützung für Windows medienbasierte Inhalte auf DVD-Player, Set-Top-Boxs und andere Heimgeräte verteilt wird.

Die einfachste Möglichkeit zum Codieren und Übermitteln von videoverschachtelten Videos besteht darin, Ihre Anwendung mit dem Windows Media Format SDK zu entwickeln und den Inhalt in ASF-Dateien zu speichern. Die interlaced-Informationen zu Frames werden mithilfe von Dateneinheitenerweiterungen an den Codec übergeben, die für ASF-Inhalte gut geeignet sind, aber in anderen Containern etwas schwieriger zu unterstützen sind. Weitere Informationen zu Dateneinheitenerweiterungen finden Sie unter [Verwenden von Dateneinheitenerweiterungen.](usingdataunitextensions.md)

Die Unterstützung der Interlacingcodierung umfasst zwei Hauptschritte: das Abrufen der Frameinformationen an den Encoder und das Bereitstellen der Informationen an die Renderinganwendung. Diese Schritte werden in den folgenden Abschnitten beschrieben.

## <a name="interlaced-video-and-the-encoder"></a>Interlaced Video und der Encoder

Der erste Schritt beim Codieren von Videos mit beibehaltener Interlacing besteht darin, den Encoder für die Codierung von Feldern mit Zeilensprung zu konfigurieren. Legen Sie hierzu die [MFPKEY \_ INTERLACEDCODINGENABLED-Eigenschaft](mfpkey-interlacedcodingenabledproperty.md) auf **TRUE** fest. Dadurch wird der Encoder auf den Empfang von Interlacingbeispielen vorbereitet. Jedes Eingabebeispiel muss beide Felder enthalten.

An jedes Beispiel, das Sie nach dem Aktivieren der Interlacingcodierung mit dem Encoder verarbeiten, sollte eine Dateneinheitenerweiterung angefügt sein. Stichproben ohne die erwartete Dateneinheitenerweiterung werden als progressiv angenommen. Die GUID, die die Erweiterung identifiziert, ist D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. Die werte, die von den Objekten des Windows Media Format SDK übergeben werden, werden in der folgenden Tabelle definiert.



| Wert      | Beschreibung                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Gibt an, dass das Beispiel zuerst mit dem unteren Feld codiert wird. Dieser Wert ist nur sinnvoll, wenn er mit dem interlaced-Wert kombiniert wird. |
| 0x00000040 | Gibt an, dass das Beispiel zuerst mit dem oberen Feld codiert wird. Dieser Wert ist nur sinnvoll, wenn er mit dem interlaced-Wert kombiniert wird.    |
| 0x00000080 | Gibt an, dass das Beispiel mit einem Zeilensprung verknüpft ist. Dies ist der einzige Wert, der für die Codec-DMOs von Bedeutung ist.                                    |



 

Einer der ersten beiden Werte wird immer mit 0x80 kombiniert, wobei ein bitweises **OR** verwendet wird, bevor er für das Beispiel festgelegt wird. Der Encoder überprüft jedoch nur 0x80 und ignoriert den Rest der Erweiterung. Wenn die Erweiterung das Beispiel als Interlacing identifiziert, behält der Encoder das Sample-Interlacing im komprimierten Stream bei und bettet ein Anzeigeflag in den Stream ein, damit der Decoder Interlacingframes identifizieren kann. Jedes Interlacingbeispiel ist markiert, sodass Quellinhalt, der eine Mischung aus progressivem und interlaced-Muster ist, zusammen in einen Stream codiert werden kann.

Das Windows Media Format SDK Writer-Objekt enthält die Inhaltstyp-Dateneinheitserweiterungen in den Beispielen, die in den Datenabschnitt des ASF-Containers geschrieben werden, damit sie zum Zeitpunkt des Renderings verwendet werden können.

## <a name="reading-and-rendering-interlaced-video"></a>Lesen und Rendern von videoverschachtelten Videos

Der Decoder identifiziert Verschachtelungsbeispiele basierend auf dem Flag, das vom Encoder im Stream festgelegt wurde. Standardmäßig deinterniert der Decoder die Stichproben und liefert progressive Ausgaben. Die Playeranwendung kann den Decoder so konfigurieren, dass Ausgaben mit Interlacing verarbeitet werden, indem die [ \_ \_ DEINTERLACING-Eigenschaft des MFPKEY-DECODERs](mfpkey-decoder-deinterlacingproperty.md) festgelegt wird.

Die Schwierigkeiten bei der Videowiedergabe mit Zeilensprung treten auf, nachdem der Decoder die Beispiele übermittelt hat. Der Renderer (Grafikkarte oder Chip auf einem Gerät) kann den Videoinhalt nicht ordnungsgemäß anzeigen, ohne zu wissen, welches Feld das ist. In Anwendungen, die das Windows Media Format SDK verwenden, wird die Inhaltstyp-Dateneinheiterweiterung aus den nicht komprimierten Beispielen abgerufen und kann an das Gerät übergeben werden.

Bei direkter Verwendung der Codecobjekte erfolgt keine dieser Datenübertragungen automatisch. Sie müssen unterstützung für Dateneinheitenerweiterungen sowohl in Ihren Pufferobjekten als auch in dem Container implementieren, den Sie für Ihren codierten Inhalt verwenden. Die meisten gängigen Mediencontainertypen (z. B. AVI) unterstützen keine Metadaten auf Beispielebene. Sie können Ihr eigenes System implementieren, um die Daten in der Datei zu speichern und sie einzelnen Beispielen zuzuordnen, aber nur ein benutzerdefinierter Reader kann sie abrufen.

> [!Note]  
> Das Festlegen der [MFPKEY \_ INTERLACEDCODINGENABLED-Eigenschaft](mfpkey-interlacedcodingenabledproperty.md) auf **TRUE** und das anschließende Senden von Beispielen mit angefügter Inhaltstyp-Dateneinheitserweiterung kann dazu führen, dass der Encoder abstürzt. Legen Sie den Encoder für die Interlacingcodierung nur fest, wenn Sie Überlingbeispiele bereitstellen müssen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



