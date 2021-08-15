---
title: put-Befehl
description: Der Befehl put definiert den Bereich des Quellbilds und des Zielfensters, die für die Anzeige verwendet werden. Digital-Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- put-Befehl Windows Multimedia
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

Der Befehl put definiert den Bereich des Quellbilds und des Zielfensters, die für die Anzeige verwendet werden. Digital-Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

Flag zum Definieren des Bereichs. In der folgenden Tabelle sind Gerätetypen aufgeführt, die den Put-Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                                      | Bedeutung                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | Zielziel am *Rechteckrahmenrahmen* an *der Quelle des* Rechtecks am *Rechteck* | Videovideo zum *Rechteckfensterfenster* *beim* Clientfensterclient im *Rechteckfenster* |
| overlay      | Zielziel am *Rechteckrahmenrahmen* am *Rechteck*                             | Quellquelle im *Videovideo zum Rechteck* am *Rechteck*                                           |



 

In der folgenden Tabelle sind die Flags, die im **lpszRegions-Parameter angegeben** werden können, und ihre Bedeutungen aufgeführt.



| Wert                        | Bedeutung                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Wählt den gesamten Clientbereich des Zielfensters aus, um die Daten anzuzeigen.                                                                                                                                                                                                                                                                         |
| Ziel am *Rechteck*   | Wählt einen Teil des Clientbereichs des Zielfensters aus, der zum Anzeigen des Bilds verwendet wird. Wenn ein Bereich des Anzeigefensters angegeben wird und das Gerät Stretching unterstützt, wird das Quellbild auf den Zieloffset und -umfang gestreckt.                                                                                                     |
| frame                        | Wählt den gesamten Framepuffer aus, um die eingehenden Videobilder zu empfangen.                                                                                                                                                                                                                                                                                 |
| Frame am *Rechteck*         | Wählt einen Teil des Framepuffers aus, um die eingehenden Videobilder zu empfangen.                                                                                                                                                                                                                                                                           |
| source                       | Wählt das gesamte Bild für die Anzeige im Zielfenster aus.                                                                                                                                                                                                                                                                                       |
| Quelle am *Rechteck*        | Wählt einen Teil des Bilds aus, der im Zielfenster angezeigt werden soll. Wenn ein Bereich des Quellbilds angegeben wird und das Gerät Stretching unterstützt, wird das Quellbild auf den Zieloffset und -umfang gestreckt.                                                                                                                           |
| video                        | Wählt das gesamte eingehende Videobild aus, das im Framepuffer erfasst werden soll.                                                                                                                                                                                                                                                                               |
| Video am *Rechteck*         | Wählt einen Teil des eingehenden Videobilds aus, das im Framepuffer erfasst werden soll.                                                                                                                                                                                                                                                                         |
| Fenster                       | Stellt die Anfangsfenstergröße auf der Anzeige wieder auf. Mit diesem Befehl wird auch das Fenster angezeigt.                                                                                                                                                                                                                                                               |
| Fenster am *Rechteck*        | Ändert die Größe und Position des Anzeigefensters. Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Anzeigefensters (in der Regel der Desktop), wenn das Flag "style child" für den geöffneten [Befehl verwendet](open.md) wurde. Um die Position des Fensters zu ändern, ohne dessen Höhe oder Breite zu ändern, geben Sie 0 (null) für die Höhe und Breite an. |
| Window-Client                | Stellt den Clientbereich des Fensters wieder auf.                                                                                                                                                                                                                                                                                                               |
| Fensterclient beim *Rechteck* | Ändert die Größe und Position des Clientbereichs des Fensters. Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Clientfensters. Um die Position des Fensters zu ändern, ohne dessen Höhe oder Breite zu ändern, geben Sie 0 (null) für die Höhe und Breite an.                                                                                      |



 

Wenn ein Flag ein Rechteck enthält, sind die Rechteckkoordinaten relativ zum Fenster- oder Bildersprung und werden **als X1 Y1 X2 Y2 angegeben.** Die Koordinaten **X1Y1 geben** die obere linke Ecke an, und die **Koordinaten X2Y2** geben die Breite und Höhe des Rechtecks an.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digitalvideogeräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Der Befehl put definiert mindestens eines der folgenden Rechtecke bei der Arbeit mit Videoüberlagerungsgeräten:

-   Das Videorechteck definiert den Bereich des eingehenden Videobilds, das erfasst werden soll.
-   Das Rahmenrechteck definiert den Bereich des Framepuffers, der das eingehende Videobild empfängt.
-   Das Quellrechteck definiert, welcher Bereich des Framepuffers in das Zielrechteck kopiert wird.
-   Das Zielrechteck definiert den Bereich des Clientbereichs des Anzeigefensters, der das Videobild empfängt.

Das Videorechteck ist auf die gleiche Weise mit dem Framerechteck verknüpft wie das Quellrechteck mit dem Zielrechteck. Eine Streckung kann vom Videorechteck zum Rahmenrechteck und vom Quellrechteck zum Zielrechteck erfolgen. Nicht alle Geräte unterstützen Stretching, und Stretching muss aktiviert sein (mithilfe des [Set-Befehls).](set.md)

Der folgende Befehl definiert drei Regionen für das Video, den Frame und die Quelle.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Die Regionen in diesem Beispiel sind wie folgt definiert:

-   Ein Bereich von 200 x 200 Pixeln der eingehenden Videodaten, beginnend mit einem Ursprung von 120 Pixeln von der oberen linken Ecke, wird im Framepuffer erfasst.
-   Die Videodaten werden in einem Bereich von 200 bis 200 Pixeln in der oberen linken Ecke des Framepuffers platziert.
-   Übertragungen werden vom 200- bis 200-Pixel-Bereich in der oberen linken Ecke des Framepuffers zum Zielfenster vorgenommen.

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

 

