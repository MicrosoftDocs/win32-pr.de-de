---
description: Video Codierung mit Zeilen Sprung
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Video Codierung mit Zeilen Sprung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fafacb56f29964e81b040c59cdb75d8ebb35830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960590"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Video Codierung mit Zeilen Sprung (Microsoft Media Foundation)

Video Daten, die für die Verwendung mit Computern vorgesehen sind, sind in der Regel *progressiv*, was bedeutet, dass jeder Frame als einzelnes Bild codiert Einige Geräte, wie z. b. Fernsehgeräte, zeigen einen Frame nicht gleichzeitig an, sondern als zwei Bilder. Eines der Bilder oder Felder enthält alle geraden Zeilen. Das andere Feld enthält die Daten für alle ungeraden nummerierten Zeilen. Videos, die mit mehr als einem Feld pro Frame codiert sind, werden mit Zeilen Sprung bezeichnet, da es durchwechseln zwischen dem geraden Feld und dem ungeraden Feld gerendert wird.

In der Vergangenheit war der Zeilen Sprung Videoinhalt vor der Codierung mit dem Windows Media Video Codec immer deaktiviert. Ab der Windows Media 9-Serie unterstützt der Video Encoder die Komprimierung von Zeilen Sprung Inhalten, ohne Sie zuvor in progressiv umzuwandeln. Die Beibehaltung von Zeilen Sprung in einer codierten Datei ist wichtig, wenn der Inhalt jemals auf einer Zeilen Sprung Anzeige, z. b. einem Fernsehen, gerendert wird. Diese Funktion ist von größerer Bedeutung, da die Unterstützung von Windows Media-basierten Inhalten auf DVD-Player, Set-Top-Boxes und andere Home-Elektronik aufsetzt.

Die einfachste Methode zum Codieren und bereitzustellen von Zeilen Sprung Videos besteht darin, Ihre Anwendung mit dem Windows Media-Format-SDK zu entwickeln und den Inhalt in ASF-Dateien zu speichern. Die Zeilen Sprung Informationen zu Frames werden mithilfe von dateneinheits-Erweiterungen an den Codec übermittelt, die für den ASF-Inhalt gut geeignet sind, aber in anderen Containern unterstützt werden. Weitere Informationen zu Dateneinheiten Erweiterungen finden Sie unter [Verwenden von Dateneinheiten Erweiterungen](usingdataunitextensions.md).

Zur Unterstützung der interplizierung sind zwei Hauptschritte erforderlich: die Frame-Informationen werden dem Encoder und die Informationen an die renderinganwendung geliefert. Diese Schritte werden in den folgenden Abschnitten beschrieben.

## <a name="interlaced-video-and-the-encoder"></a>Zeilen Sprung Video und der Encoder

Der erste Schritt beim Codieren von Videos mit geprüfter Zeilen Sprung besteht darin, den Encoder zum Codieren von Zeilen Sprung Feldern zu konfigurieren. Legen Sie dazu die Eigenschaft " [mfpkey \_ interlacedcodingenabled](mfpkey-interlacedcodingenabledproperty.md) " auf " **true**" fest. Dadurch wird der Encoder vorbereitet, um Zeilen Sprung Beispiele zu erhalten. Jedes Eingabe Beispiel muss beide Felder enthalten.

Für jedes Beispiel, das Sie nach dem Aktivieren der Zeilen Sprung Codierung mit dem Encoder verarbeiten, sollte eine dateneinheits Erweiterung angefügt werden. Beispiele ohne die erwartete Dateneinheiten Erweiterung werden als progressiv angenommen. Die GUID, die die Erweiterung identifiziert, ist D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. Die Werte, die von den-Objekten des Windows Media Format SDK übermittelt werden, werden in der folgenden Tabelle definiert.



| Wert      | BESCHREIBUNG                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Gibt an, dass das Beispiel zuerst mit dem untersten Feld codiert wird. Dieser Wert ist nur in Kombination mit dem Zeilen Sprung Wert sinnvoll. |
| 0x00000040 | Gibt an, dass das Beispiel zuerst mit dem obersten Feld codiert wird. Dieser Wert ist nur in Kombination mit dem Zeilen Sprung Wert sinnvoll.    |
| 0x00000080 | Gibt an, dass das Beispiel mit Zeilen Sprung dargestellt wird. Dies ist der einzige Wert, der für die Codec-DMOS von Bedeutung ist.                                    |



 

Einer der ersten beiden Werte wird immer mit 0x80 kombiniert, indem ein bitweises **or** verwendet wird, bevor er für das Beispiel festgelegt wird. Der Encoder prüft jedoch nur 0x80 und ignoriert den Rest der Erweiterung. Wenn die Erweiterung das Beispiel als Zeilen Sprung bezeichnet, behält der Encoder das Sample-Zeilen Sprung im komprimierten Stream bei und bettet ein Kennzeichen im Stream ein, sodass der Decoder Zeilen Sprung Frames identifizieren kann. Jedes Zeilen Sprung Beispiel ist als markiert, sodass Quell Inhalte, die eine Mischung aus progressivem und Zeilen Sprung sind, zusammen in einen Stream codiert werden können.

Das Windows Media Format SDK Writer-Objekt enthält die Inhaltstyp-Dateneinheiten Erweiterungen in den Beispielen, die beim Rendern in den Daten Abschnitt des ASF-Containers geschrieben werden.

## <a name="reading-and-rendering-interlaced-video"></a>Lesen und Rendern von Video Dateien

Der Decoder identifiziert Zeilen Sprung Proben basierend auf dem im Stream festgelegten Flag durch den Encoder. Standardmäßig deinstalübergibt der Decoder die Beispiele und stellt Progressive Ausgaben bereit. Die Player Anwendung kann den Decoder so konfigurieren, dass Ausgaben mit Zeilen Sprung verarbeitet werden, indem die Eigenschaft [debuglacing des mfpkey- \_ Decoders \_ ](mfpkey-decoder-deinterlacingproperty.md) festgelegt wird.

Die Schwierigkeit bei der Zeilen Sprung Videowiedergabe tritt auf, nachdem der Decoder die Beispiele bereitstellt. Der Renderer (Grafikkarte oder Chip in einem Gerät) kann den Videoinhalt nicht ordnungsgemäß anzeigen, ohne zu wissen, welches Feld zu welchem Feld gehört. In Anwendungen, die das SDK für den Windows Media-Format verwenden, wird der Inhaltstyp für die Dateneinheiten Erweiterung aus den nicht komprimierten Beispielen abgerufen und kann an das Gerät übermittelt werden.

Wenn Sie die Codec-Objekte direkt verwenden, erfolgt keine automatische Datenübertragung. Sie müssen Unterstützung für Daten-Einheiten Erweiterungen sowohl in den Puffer Objekten als auch in dem Container implementieren, den Sie für den codierten Inhalt verwenden. Die meisten gängigen Typen von Medien Containern (wie AVI) unterstützen keine Metadaten auf Stichproben Ebene. Sie können ein eigenes System implementieren, um die Daten in der Datei zu speichern und Sie einzelnen Beispielen zuzuordnen, aber nur ein benutzerdefinierter Reader kann Sie abrufen.

> [!Note]  
> Wenn Sie die Eigenschaft " [mfpkey \_ interlacedcodingenabled](mfpkey-interlacedcodingenabledproperty.md) " auf " **true**" festlegen und dann keine Stichproben mit der angefügten dateneinheits Erweiterung "Content-Type" senden, kann der Encoder abstürzen. Legen Sie den Encoder für die Zeilen Sprung Codierung nur dann fest, wenn Sie über Sprung Proben zur Bereitstellung verfügen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



