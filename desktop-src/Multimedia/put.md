---
title: put-Befehl
description: Der Befehl put definiert den Bereich des Quellbilds und des Zielfensters, das für die Anzeige verwendet wird. Digitale Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- Befehl "put" Windows Multimedia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08732b0ed55464fa1a288cc13a9ac19609b480644ffa4c9dfbeb140cedbbd3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372379"
---
# <a name="put-command"></a>put-Befehl

Der Befehl put definiert den Bereich des Quellbilds und des Zielfensters, das für die Anzeige verwendet wird. Digitale Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*
</dt> <dd>

Flag zum Definieren des Bereichs. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den put-Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                                      | Bedeutung                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | Zielziel am *Rechteckrahmen* an *der Rechteckquellquelle* am *Rechteck* | Videovideo zum *Rechteckfensterfenster* am *Clientfensterclient* im *Rechteckfenster* |
| overlay      | Zielziel am *Rechteckrahmen* am *Rechteck*                             | Quelle am *Rechteck* Videovideo am *Rechteck*                                           |



 

Die folgende Tabelle enthält die Flags, die im **lpszRegions-Parameter** angegeben werden können, und ihre Bedeutungen.



| Wert                        | Bedeutung                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Wählt den gesamten Clientbereich des Zielfensters aus, um die Daten anzuzeigen.                                                                                                                                                                                                                                                                         |
| Ziel am *Rechteck*   | Wählt einen Teil des Clientbereichs des Zielfensters aus, der zum Anzeigen des Bilds verwendet wird. Wenn ein Bereich des Anzeigefensters angegeben wird und das Gerät Stretching unterstützt, wird das Quellbild auf den Zieloffset und -extent gestreckt.                                                                                                     |
| frame                        | Wählt den gesamten Framepuffer aus, um die eingehenden Videobilder zu empfangen.                                                                                                                                                                                                                                                                                 |
| Frame am *Rechteck*         | Wählt einen Teil des Framepuffers aus, um die eingehenden Videobilder zu empfangen.                                                                                                                                                                                                                                                                           |
| source                       | Wählt das gesamte Bild aus, das im Zielfenster angezeigt werden soll.                                                                                                                                                                                                                                                                                       |
| Quelle am *Rechteck*        | Wählt einen Teil des Bilds aus, der im Zielfenster angezeigt werden soll. Wenn ein Bereich des Quellbilds angegeben wird und das Gerät Stretching unterstützt, wird das Quellbild auf den Zieloffset und -extent gestreckt.                                                                                                                           |
| video                        | Wählt das gesamte eingehende Videobild aus, das im Framepuffer erfasst werden soll.                                                                                                                                                                                                                                                                               |
| Video am *Rechteck*         | Wählt einen Teil des eingehenden Videobilds aus, der im Framepuffer erfasst werden soll.                                                                                                                                                                                                                                                                         |
| Fenster                       | Stellt die Anfangsfenstergröße auf der Anzeige wieder her. Dieser Befehl zeigt auch das Fenster an.                                                                                                                                                                                                                                                               |
| Fenster am *Rechteck*        | Ändert die Größe und Position des Anzeigefensters. Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Anzeigefensters (in der Regel der Desktop), wenn das Flag "style child" für den [geöffneten](open.md) Befehl verwendet wurde. Um die Position des Fensters zu ändern, ohne seine Höhe oder Breite zu ändern, geben Sie 0 (null) für Höhe und Breite an. |
| Fensterclient                | Stellt den Clientbereich des Fensters wieder her.                                                                                                                                                                                                                                                                                                               |
| Fensterclient am *Rechteck* | Ändert die Größe und position des Clientbereichs des Fensters. Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Clientfensters. Um die Position des Fensters zu ändern, ohne seine Höhe oder Breite zu ändern, geben Sie 0 (null) für Höhe und Breite an.                                                                                      |



 

Wenn ein Flag ein Rechteck enthält, sind die Rechteckkoordinaten nach Bedarf relativ zum Fensterursprung oder zum Bildursprung und werden als **X1 Y1 X2 Y2** angegeben. Die Koordinaten **X1Y1** geben die obere linke Ecke an, und die Koordinaten **X2Y2** geben die Breite und Höhe des Rechtecks an.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digitalvideogeräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Der Befehl put definiert bei der Arbeit mit Videoüberlagerungsgeräten ein oder mehrere der folgenden Rechtecke:

-   Das Videorechteck definiert den Bereich des zu erfassenden eingehenden Videobilds.
-   Das Rahmenrechteck definiert den Bereich des Framepuffers, der das eingehende Videobild empfängt.
-   Das Quellrechteck definiert, welcher Bereich des Rahmenpuffers in das Zielrechteck kopiert wird.
-   Das Zielrechteck definiert den Bereich des Clientbereichs des Anzeigefensters, der das Videobild empfängt.

Das Videorechteck ist mit dem Rahmenrechteck auf die gleiche Weise verknüpft wie das Quellrechteck mit dem Zielrechteck. Stretching kann vom Videorechteck zum Rahmenrechteck und vom Quellrechteck zum Zielrechteck erfolgen. Nicht alle Geräte unterstützen Stretching, und Stretching muss aktiviert sein (mithilfe des [Set-Befehls).](set.md)

Der folgende Befehl definiert drei Bereiche für video, frame und source.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Die Regionen in diesem Beispiel werden wie folgt definiert:

-   Ein 200 x 200 Pixel großer Bereich der eingehenden Videodaten, beginnend bei einem Ursprung von 120 Pixeln aus der oberen linken Ecke, wird im Framepuffer erfasst.
-   Die Videodaten werden in einem Bereich von 200 x 200 Pixeln in der oberen linken Ecke des Framepuffers platziert.
-   Übertragungen erfolgen aus dem Bereich von 200 x 200 Pixeln in der oberen linken Ecke des Rahmenpuffers an das Zielfenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

