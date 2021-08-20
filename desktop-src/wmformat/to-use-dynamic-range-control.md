---
title: So verwenden Sie das Dynamische Bereichssteuerelement
description: So verwenden Sie das Dynamische Bereichssteuerelement
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Windows Medienformat-SDK, Steuerelement für dynamischen Bereich
- Windows Medienformat-SDK, Windows Medienaudio 9 Professional Codec
- Windows Medienformat-SDK, Windows Medienaudio 9– verlustfreier Codec
- Advanced Systems Format (ASF),Windows Media Audio 9 Professional Codec
- ASF (Advanced Systems Format),Windows Media Audio 9 Professional Codec
- Advanced Systems Format (ASF),Windows Media Audio 9– Verlustloser Codec
- ASF (Advanced Systems Format),Windows Media Audio 9– Verlustloser Codec
- Advanced Systems Format (ASF), Dynamische Bereichssteuerung
- ASF (Advanced Systems Format), Dynamische Bereichssteuerung
- Dynamisches Bereichssteuerelement
- Codecs,Windows Media Audio 9 Verlustfreier Codec
- Codecs,Windows Media Audio 9 Professional Codec
- 'Windows Media Audio 9: Verlustfreier Codec, Dynamische Bereichssteuerung'
- Windows Media Audio 9 Professional Codec, Dynamische Bereichssteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55251dd88ce7b9427fcee33d5988a3736b4b6f36838e269bb53a11f3b5480f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653863"
---
# <a name="to-use-dynamic-range-control"></a>So verwenden Sie das Dynamische Bereichssteuerelement

Der dynamische Bereich eines Audioinhalts ist im Grunde der Unterschied zwischen der niedrigsten und der maximalen Lautstärke. Wenn der dynamische Bereich des Inhalts zu hoch ist, können Benutzer das Volume während der Wiedergabe wiederholt anpassen. Filme weisen z. B. häufig einen hohen dynamischen Bereich auf. Wenn die Lautstärke so angepasst wird, dass der Dialog während stiller Szenen verstanden werden kann, sind andere Teile des Films mit Musik- oder Soundeffekten häufig lauter als gewünscht.

Die Windows Media Audio 9 Professional und Windows Media Audio 9 Lossless Codecs unterstützen ein Feature namens Dynamic Range Control. Zur Codierungszeit berechnet der Codec die Spitzen- und durchschnittlichen Amplitudenwerte im Inhalt, und das Writer-Objekt speichert diese Werte in den Metadaten für den Stream, wenn die Codierung abgeschlossen ist. Optional kann eine Anwendung auch "Zielwerte" als Metadaten schreiben, die Playeranwendungen und der Decoder beim Wiedergeben der Datei als Hinweise verwenden können. Zur Wiedergabezeit kann eine Anwendung die Ebene des Dynamischen Bereichssteuerelements angeben, das auf den Audiostream angewendet werden soll.

Windows Media Player implementiert die Dynamische Bereichssteuerung als Feature für den stillen Modus.

## <a name="when-to-use-dynamic-range-control"></a>Verwenden des Dynamischen Bereichssteuerelements

Das Steuerelement für den dynamischen Bereich kann den Sound des Inhalts ändern. Aus diesem Grund sollten Sie Ihre Anwendung nicht so konfigurieren, dass die Dynamische Bereichssteuerung automatisch verwendet wird. Stellen Sie benutzern stattdessen die Möglichkeit bereit, die Steuerung des dynamischen Bereichs bei Bedarf zu aktivieren oder zu deaktivieren.

## <a name="using-dynamic-range-control"></a>Verwenden des Dynamischen Bereichssteuerelements

Zur Wiedergabezeit wird die Steuerung des dynamischen Bereichs mithilfe der Ausgabeeinstellung g \_ wszDynamicRangeControl aktiviert. Verwenden Sie [**IWMReaderAdvanced2::SetOutputSetting,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) um die Einstellung zu konfigurieren. Der Wert 0 (Standard) gibt an, dass der dynamische Bereich nicht geändert werden soll. Der Wert 1 oder 2 signalisiert dem Codec die Ausführung der Dynamischen Bereichssteuerung, wobei 1 ein mittleres Maß an Dynamischer Bereichskomprimierung und 2 ein hohes Maß an Dynamischer Bereichskomprimierung ist.

Zur Codierungszeit oder Wiedergabezeit können Sie die PCM-Werte des Codecziels für die Spitzen- und Durchschnittswerte festlegen, indem Sie die Attribute [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) bzw. [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) festlegen. Diese Werte werden als Metadatenattribute gespeichert und sollten über die Methoden der [**IWMHeaderInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) aufgerufen werden. Wenn Sie einen Audiostream mit dem professionellen oder verlustfreien Codec codieren, werden die Attribute [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) und [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) automatisch auf die Spitzen- und Durchschnittswerte des ursprünglichen Inhalts festgelegt. Die Zielwerte werden standardmäßig auf die gleichen Werte wie die Verweise festgelegt.

Der Decoder berechnet zur Wiedergabezeit den dynamischen Bereich basierend auf der ausgewählten Ebene des Dynamischen Bereichssteuerelements und den Zielwerten (sofern angegeben). Die möglichen Bereiche sind in der folgenden Tabelle aufgeführt.



| Einstellungen                                                                | Bereich der übermittelten Audiodaten                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDynamicRangeControl = 0 (Beliebige Zielwerte)                       | Der gleiche Bereich wie der ursprüngliche Inhalt.                                                                                          |
| g \_ wszDynamicRangeControl = 1 (Zielwerte gleich Verweiswerten) | Die durchschnittliche Ebene wird beibehalten, und Spitzen sind auf den Durchschnitt von +12 dB beschränkt.                                                    |
| g \_ wszDynamicRangeControl = 2 (Zielwerte gleich Verweiswerten) | Die durchschnittliche Ebene wird beibehalten, und Spitzen sind auf den Durchschnitt von +6 dB beschränkt.                                                     |
| g \_ wszDynamicRangeControl = 1 (Angegebene Zielwerte)                 | Die durchschnittliche Ebene ist auf den Zieldurchschnittswert festgelegt, und die Spitzenwerte sind auf den Zielspitzenwert beschränkt.                                   |
| g \_ wszDynamicRangeControl = 2 (angegebene Zielwerte)                 | Die durchschnittliche Ebene wird auf den Zieldurchschnittswert festgelegt und die Spitzenwerte sind auf den Median des Zieldurchschnitts und der Zielspitzenwerte beschränkt. |



 

Beachten Sie, dass das Dynamische Bereichssteuerelement nur eine Funktion der Decodierung ist und nur als Metadaten in der Datei selbst vorhanden ist. Diese Einstellungen haben keine Auswirkungen auf den in der Datei gespeicherten Inhalt, es sei denn, Sie weisen den Decoder ausdrücklich an, sie zu verwenden. Das Windows Media Format SDK bietet keine Methoden zum Ändern des dynamischen Bereichs der Audiodaten zur Codierungszeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Weiterführende Themen**](advanced-topics.md)
</dt> </dl>

 

 




