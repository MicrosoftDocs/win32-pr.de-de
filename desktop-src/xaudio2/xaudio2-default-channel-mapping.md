---
description: Ein XAudio2-Client hat die vollständige Kontrolle über die Zuordnung von den Kanälen einer Stimme zu den Kanälen der einzelnen Zielstimmen.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: XAudio2-Standardkanalzuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42bb2f67709586532a19d86a916d3b7852652e76f9b6ce1ae115f1fc670e37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025948"
---
# <a name="xaudio2-default-channel-mapping"></a>XAudio2-Standardkanalzuordnung

Ein XAudio2-Client hat die vollständige Kontrolle über die Zuordnung zwischen den Kanälen einer Stimme und den Kanälen der einzelnen Zielstimmen. Er steuert die Zuordnung mithilfe der [**IXAudio2Voice::SetOutputMatrix-Methode.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) In einigen Fällen vereinfacht XAudio2 diese Aufgabe jedoch, indem automatisch eine Standardsendenmatrix eingerichtet wird. Hierzu wird ggf. die Kanalmaske verwendet, die den Audiokanälen einer Stimme zugeordnet ist. Eine Kanalmaske ist eine Kombination aus SPEAKER \_ xxx-Bitmasken, wie in X3DAudio.h und an anderer Stelle definiert. XAudio2 erfordert, dass Kanalmasken 0 sind oder die gleiche Anzahl von Bits wie die Anzahl der Kanäle festgelegt ist.

In der folgenden Tabelle sind die Anforderungen und Standardwerte für die Kanalmasken für die von XAudio2 unterstützten Formate aufgeführt. 

| Format | Kanalmaskenanforderung             | Standardmaske                        | Entsprechender Strukturmember                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | Die Datei kann eine Kanalmaske enthalten.    | Kanalmaske ist "0" oder "nicht vorhanden"        | WAVEFORMATEXTENSIBLE.dwChannelMask oder none (WAVEFORMATEX) |
| Adpcm  | Die Datei enthält keine Kanalmaske. | Die Standardkanalmaske wird immer verwendet. | None (ADPCMWAVEFORMAT)                                    |



 

Für Submix- und Masteringstimmen sowie für Quellstimmen ohne Kanalmaske oder Kanalmaske von 0 nimmt XAudio2 gemäß der folgenden Tabelle standardlautende Positionen an. 

| Kanäle  | Implizite Kanalpositionen                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Wird in beiden Lautsprechern immer frontLeft und FrontRight in vollem Umfang zugeordnet (Sonderfall für Mono-Sounds).                 |
| 2         | FrontLeft, FrontRight (grundlegende Stereokonfiguration)                                                                    |
| 3         | FrontLeft, FrontRight, LowFrequency (2.1-Konfiguration)                                                               |
| 4         | FrontLeft, FrontRight, BackLeft, BackRight (quadraphonic)                                                             |
| 5         | FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (5.0-Konfiguration)                                           |
| 6         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (5.1-Konfiguration) (siehe die folgenden Hinweise) |
| 7         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, BackCenter (6.1-Konfiguration)                 |
| 8         | FrontLeft, FrontRight, FrontCenter, LowFrequency, BackLeft, BackRight, SideLeft, SideRight (7.1-Konfiguration)        |
| 9 oder mehr | Keine impliziten Positionen (1:1-Zuordnung)                                                                            |



 

Wenn einem bestimmten Stimmenpaar im Audiographen weder die Quell- noch die Zielstimme zugeordnet ist (eine Stimme hat mehr als acht Kanäle), kann keine Stimme wiedergegeben werden, bis für die Quellstimme eine Sendematrix explizit mit der [**IXAudio2Voice::SetOutputMatrix-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) festgelegt wurde. Der Aufruf der [**IXAudio2SourceVoice::Start-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) für beide Stimmen schlägt fehl, bis Sie dies tun.

Wenn die Quellstimme und die Zielstimme eine unterschiedliche Anzahl von Sprecherpositionen aufweisen und [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) nicht auf der Quellstimme aufgerufen wurde, sendet XAudio2 jeden Quellkanal an den nächsten verfügbaren Ziellautgeber (bzw. die nächsten verfügbaren Sprecher), proportional zur Nähe des gewünschten Sprechers. Es gibt zwei Sonderfälle, in denen sich das Standardverhalten unterscheidet.

1.  Wenn das Quellaudio mono ist und sich im SPEAKER FRONT CENTER befindet \_ oder über keine definierte Position \_ verfügt, wird es immer an SPEAKER \_ FRONT LEFT und SPEAKER FRONT RIGHT \_ \_ \_ gesendet, wenn sie in der Ausgabeaudio vorhanden sind. Wenn sie nicht vorhanden sind, greift dies auf den normalen Fall zurück.
2.  Wenn die Quelle und das Ziel beide über 6 Kanäle verfügen und an einer der standard 5.1-Lautsprechersetups positioniert sind (Left+Right+Center+Sub+BackL+BackR oder Left+Right+Center+Sub+SideL+SideR), werden Kanäle eins zu eins zugeordnet. Anders ausgedrückt: SideLeft/Right und BackLeft/Right werden gleichwertig behandelt. Dies liegt daran, dass diese Setups in der Vergangenheit verwechslungen sind. Daher besteht die angenommene Absicht immer darin, eins zu eins zuzuordnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stimmen](voices.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
