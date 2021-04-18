---
title: So verwenden Sie das dynamische Bereichs Steuerelement
description: So verwenden Sie das dynamische Bereichs Steuerelement
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Windows Media-Format-SDK, dynamisches Bereichs Steuerelement
- Windows Media-Format-SDK, Windows Media Audio 9 Professional-Codec
- Windows Media-Format-SDK, Windows Media Audio 9 Verlust lose Codec
- Advanced Systems Format (ASF), Windows Media Audio 9 Professional Codec
- ASF (Advanced Systems Format), Windows Media Audio 9 Professional Codec
- Advanced Systems Format (ASF), Windows Media Audio 9 Verlust lose Codec
- ASF (Advanced Systems Format), Windows Media Audio 9 Verlust lose Codec
- Advanced Systems Format (ASF), dynamisches Bereichs Steuerelement
- ASF (Advanced Systems Format), dynamisches Bereichs Steuerelement
- Dynamisches Bereichs Steuerelement
- Codecs, Windows Media Audio 9 Verlust lose Codec
- Codecs, Windows Media Audio 9 Professional-Codec
- Windows Media Audio 9 verlustloses Codec, dynamisches Bereichs Steuerelement
- Windows Media Audio 9 Professional-Codec, dynamisches Bereichs Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106340477"
---
# <a name="to-use-dynamic-range-control"></a>So verwenden Sie das dynamische Bereichs Steuerelement

Der dynamische Bereich eines Audioinhalts ist im Grunde der Unterschied zwischen dem niedrigsten Volume und dem maximalen Volume. Wenn der dynamische Bereich des Inhalts zu hoch ist, können Benutzer das Volume möglicherweise wiederholt während der Wiedergabe anpassen. Filme haben beispielsweise häufig einen hohen dynamischen Bereich. Wenn das Volume so angepasst wird, dass das Dialogfeld in stillen Szenen verstanden werden kann, sind andere Teile des Films mit Musik-oder Soundeffekten häufig lauter als gewünscht.

Die Windows Media Audio 9 Professional-und Windows Media Audio 9-Codecs ohne Verlust unterstützen eine Funktion mit dem Namen "Dynamic Range Control". Zur Codierungs Zeit berechnet der Codec die Spitzen-und durchschnittlichen Amplitude-Werte im Inhalt, und das Writer-Objekt speichert diese Werte in den Metadaten für den Datenstrom, wenn die Codierung abgeschlossen ist. Optional kann eine Anwendung auch "Ziel"-Werte als Metadaten schreiben, die von Player Anwendungen und dem Decoder als Hinweise zum Wiedergeben der Datei verwendet werden können. Zum Zeitpunkt der Wiedergabe kann eine Anwendung die Ebene des dynamischen Bereichs Steuer Elements angeben, die auf den Audiostream angewendet werden soll.

Windows Media Player implementiert das dynamische Bereichs Steuerelement als Funktion für den stillen Modus.

## <a name="when-to-use-dynamic-range-control"></a>Verwendung des dynamischen Bereichs Steuer Elements

Das dynamische Bereichs Steuerelement kann den Sound des Inhalts ändern. Aus diesem Grund sollten Sie die Anwendung nicht für die automatische Verwendung der dynamischen Bereichs Steuerung konfigurieren. Stellen Sie Benutzern stattdessen die Möglichkeit bereit, das dynamische Bereichs Steuerelement bei Bedarf ein-oder auszuschalten.

## <a name="using-dynamic-range-control"></a>Verwenden der dynamischen Bereichs Steuerung

Zum Zeitpunkt der Wiedergabe wird das dynamische Bereichs Steuerelement mithilfe der Ausgabe Einstellung g \_ wszdynamicrangecontrol aktiviert. Verwenden Sie [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) , um die Einstellung zu konfigurieren. Der Wert 0 (null) (Standardwert) gibt an, dass der dynamische Bereich nicht geändert werden soll. Der Wert 1 oder 2 signalisiert dem Codec, ein dynamisches Bereichs Steuerelement auszuführen, wobei 1 eine mittlere Ebene dynamischer Bereichs Komprimierung und 2 ein hohes Maß an dynamischer Bereichs Komprimierung ist.

Bei der Codierungs-oder Wiedergabezeit können Sie den Codec-Ziel-PCM-Werten für die Spitzen-und Durchschnittswerte zuweisen, indem Sie die Attribute [**WM/wmadrcpeer Target**](wm-wmadrcpeaktarget.md) bzw. [**WM/wmadrcaveragetarget**](wm-wmadrcaveragetarget.md) festlegen. Diese Werte werden als Metadatenattribute gespeichert und sollten mithilfe der Methoden der [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle aufgerufen werden. Wenn Sie einen Audiostream mit dem Professional-oder Verlust losen Codec codieren, werden die Attribute [**WM/wmadrcpeer Reference**](wm-wmadrcpeakreference.md) und [**WM/wmadrcaveragereferenzierung**](wm-wmadrcaveragereference.md) automatisch auf die höchst-und Durchschnittswerte der ursprünglichen Inhalte festgelegt. Die Zielwerte werden standardmäßig auf die gleichen Werte festgelegt wie die Verweise.

Der Decoder berechnet zum Zeitpunkt der Wiedergabe den dynamischen Bereich auf der Grundlage der ausgewählten Ebene des dynamischen Bereichs Steuer Elements und der Zielwerte (sofern vorhanden). Die möglichen Bereiche sind in der folgenden Tabelle aufgeführt.



| Einstellungen                                                                | Bereich der übermittelten Audiodaten                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszdynamicrangecontrol = 0 (beliebige Zielwerte)                       | Der gleiche Bereich wie der ursprüngliche Inhalt.                                                                                          |
| g \_ wszdynamicrangecontrol = 1 (Zielwerte gleich Verweis Werten) | Die durchschnittliche Ebene wird gewartet, und die Spitzen sind auf die durchschnittliche + 12 dB beschränkt.                                                    |
| g \_ wszdynamicrangecontrol = 2 (Zielwerte gleich Verweis Werten) | Die durchschnittliche Ebene wird verwaltet, und die Spitzen sind auf die durchschnittliche + 6-Datenbank beschränkt.                                                     |
| g \_ wszdynamicrangecontrol = 1 (Zielwerte angegeben)                 | Die durchschnittliche Ebene, die auf den durchschnittlichen Ziel Wert festgelegt ist, und die Spitzen auf den Ziel Spitzenwert.                                   |
| g \_ wszdynamicrangecontrol = 2 (Zielwerte angegeben)                 | Die durchschnittliche Ebene, die auf den durchschnittlichen Ziel Wert festgelegt ist, und Spitzenwerte, die auf den Median der Ziel Spitzenwerte beschränkt sind. |



 

Beachten Sie, dass das dynamische Bereichs Steuerelement nur eine Funktion der Decodierung ist und nur als Metadaten in der Datei selbst vorhanden ist. Diese Einstellungen haben keine Auswirkung auf den in der Datei gespeicherten Inhalt, es sei denn, Sie weisen den Decoder explizit an, Sie zu verwenden. Das Windows Media-Format SDK bietet keine Methoden zum Ändern des dynamischen Bereichs der Audiodaten zur Codierungs Zeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> </dl>

 

 




