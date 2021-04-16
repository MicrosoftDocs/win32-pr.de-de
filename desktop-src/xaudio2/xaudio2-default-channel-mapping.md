---
description: Ein XAudio2-Client hat die vollständige Kontrolle über die Zuordnung von den Kanälen einer Stimme zu den Kanälen der einzelnen Ziel Stimmen.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: XAudio2 Standard Kanal Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d77371223ccef02d6f0831a7aea182326f8477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485859"
---
# <a name="xaudio2-default-channel-mapping"></a>XAudio2 Standard Kanal Zuordnung

Ein XAudio2-Client hat die vollständige Kontrolle über die Zuordnung von den Kanälen einer Stimme zu den Kanälen der einzelnen Ziel voicesit steuert die Zuordnung durch die Verwendung der [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) -Methode. In einigen Fällen vereinfacht XAudio2 diese Aufgabe jedoch, indem automatisch eine standardmäßige Sende Matrix eingerichtet wird. Dies erfolgt mithilfe der Kanalmaske, sofern vorhanden, die den Audiokanälen einer Stimme zugeordnet ist. Eine Kanalmaske ist eine Kombination aus Lautsprecher \_ xxx-Bitmasken, die in X3DAudio. h und an anderen Stellen definiert sind. XAudio2 erfordert, dass Kanalmasken 0 sind oder die gleiche Anzahl von Bits als Anzahl von Kanälen festgelegt ist.

In der folgenden Tabelle werden die Anforderungen an die Kanalmaske und die Standardwerte für die von XAudio2 unterstützten Formate angezeigt. 

| Format | Kanalmasken Anforderung             | Standard Maske                        | Entsprechendes Strukturmember                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | Die Datei enthält möglicherweise eine Kanalmaske.    | Die Kanalmaske ist 0 (null) oder nicht vorhanden.        | WAVEFORMATEXTENSIBLE. dwchannelmask oder None (WaveFormatEx) |
| ADPCM  | Die Datei enthält keine Kanalmaske. | Standard Kanalmaske wird immer verwendet. | None (ADPCMWAVEFORMAT)                                    |



 

Für unter Mischungs-und Mastering-Stimmen und für Quell Stimmen ohne Kanalmaske oder Kanalmaske 0 nimmt XAudio2 die Standard Sprecherpositionen gemäß der folgenden Tabelle an. 

| Channels  | Implizite channelpositionen                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Wird immer frontleft und frontRight in vollem Umfang in beiden Referenten zugeordnet (Sonderfall für Mono-Sounds).                 |
| 2         | Frontleft, frontRight (grundlegende Stereo Konfiguration)                                                                    |
| 3         | Frontleft, frontRight, lowfrequency (2,1-Konfiguration)                                                               |
| 4         | Frontleft, frontRight, backLeft, backright (Quadraphonic)                                                             |
| 5         | Frontleft, frontRight, frontcenter, sideleft, sideright (5,0-Konfiguration)                                           |
| 6         | Frontleft, frontRight, frontcenter, lowfrequency, sideleft, sideright (5,1-Konfiguration) (siehe folgende Hinweise) |
| 7         | Frontleft, frontRight, frontcenter, lowfrequency, sideleft, sideright, backcenter (6,1-Konfiguration)                 |
| 8         | Frontleft, frontRight, frontcenter, lowfrequency, backLeft, backright, sideleft, sideright (7,1-Konfiguration)        |
| 9 oder mehr | Keine impliziten Positionen (eins-zu-Eins-Zuordnung)                                                                            |



 

Wenn ein angegebenes Sprachpaar im audiodiagramm keine Redner Positionen hat, die entweder mit der Quell-oder Ziel Stimme verknüpft sind (eine Stimme hat mehr als acht Kanäle), wird keine Stimme erst wiedergegeben, wenn die Quellsprache eine Sende Matrix explizit mithilfe der [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) -Methode festgelegt hat. Das Aufrufen der [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) -Methode für jede Stimme schlägt fehl, bis Sie dies tun.

Wenn die Stimme der Quellsprache und die Zielstimme unterschiedliche Zahlen von Redner Positionen aufweisen und [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) nicht auf der Quellsprache aufgerufen wurde, sendet XAudio2 jeden Quell Kanal an den nächstgelegenen Ziel Sprecher (oder die sprechenden Referenten), der proportional zur Art und Weise, wie nah Sie für den beabsichtigten Redner sind. Es gibt zwei Sonderfälle, in denen das Standardverhalten anders ist.

1.  Wenn die Audioquelle Mono ist und sich an der Sprech \_ Spitze im Vordergrund befindet \_ oder über keine definierte Position verfügt, wird Sie immer an den Redner \_ Vordergrund und den Sprecher Front-Right gesendet, \_ \_ \_ Wenn Sie in der Ausgabeaudiodatei vorhanden sind. Wenn Sie nicht vorhanden sind, werden Sie auf den Normalfall zurückgegriffen.
2.  Wenn die Quelle und das Ziel beide 6-Kanal sind und sich auf einer der standardmäßigen 5,1-Sprecher-Setups befinden (links + rechts + Center + Sub + backl + backr oder Left + Right + Center + Sub + Sidel + sider), werden die Kanäle nacheinander zugeordnet. Mit anderen Worten: sideleft/Right und backLeft/right werden gleichwertig behandelt. Dies liegt daran, dass in Bezug auf diese Setups Verlaufs Verwirrung aufgetreten ist. Daher wird angenommen, dass es sich um eine Zuordnung handelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stimmen](voices.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[**Getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
