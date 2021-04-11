---
title: Put-Befehl
description: Der Put-Befehl definiert den Bereich des Quell Bilds und des Zielfensters, das für die Anzeige verwendet wird. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- Put-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105705"
---
# <a name="put-command"></a>Put-Befehl

Der Put-Befehl definiert den Bereich des Quell Bilds und des Zielfensters, das für die Anzeige verwendet wird. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszregions*
</dt> <dd>

Flag zum Definieren des Bereichs. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den Put-Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                                      | Bedeutung                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Digitalvideo | Zielziel bei *rechtedem Frame Rahmen* bei *Rechteck Quell Quelle* bei *Rechteck* | Video *Video* in *Rechteck Fenster im* Fenster Client Fenster Client *im Rechteck* |
| overlay      | Zielziel bei *Rechteck Rahmen Rahmen* bei *Rechteck*                             | Quell Quelle bei *Rechteck* Video Video bei *Rechteck*                                           |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszregions** -Parameter und deren Bedeutung angegeben werden können.



| Wert                        | Bedeutung                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Wählt den gesamten Client Bereich des Zielfensters aus, um die Daten anzuzeigen.                                                                                                                                                                                                                                                                         |
| Ziel bei *Rechteck*   | Wählt einen Teil des Client Bereichs des Zielfensters aus, in dem das Bild angezeigt wird. Wenn ein Bereich des Anzeige Fensters angegeben wird und das Gerät die Streckung unterstützt, wird das Quellbild auf den Ziel Offset und-Block gestreckt.                                                                                                     |
| frame                        | Wählt den gesamten Frame Puffer zum Empfangen der eingehenden Videobilder aus.                                                                                                                                                                                                                                                                                 |
| Rahmen bei *Rechteck*         | Wählt einen Teil des Frame Puffers zum Empfangen der eingehenden Videobilder aus.                                                                                                                                                                                                                                                                           |
| source                       | Wählt das gesamte Bild aus, das im Zielfenster angezeigt werden soll.                                                                                                                                                                                                                                                                                       |
| Quelle beim *Rechteck*        | Wählt einen Teil des Bilds aus, der im Zielfenster angezeigt werden soll. Wenn ein Bereich des Quell Bilds angegeben wird und das Gerät die Streckung unterstützt, wird das Quell Abbild auf den Ziel Offset und-Block gestreckt.                                                                                                                           |
| video                        | Wählt das gesamte eingehende Videobild aus, das im Frame Puffer erfasst werden soll.                                                                                                                                                                                                                                                                               |
| Video mit *Rechteck*         | Wählt einen Teil des eingehenden Video Bilds aus, der im Frame Puffer erfasst werden soll.                                                                                                                                                                                                                                                                         |
| Fenster                       | Stellt die anfängliche Fenstergröße auf der Anzeige wieder her. Mit diesem Befehl wird auch das-Fenster angezeigt.                                                                                                                                                                                                                                                               |
| Fenster mit *Rechteck*        | Ändert die Größe und Position des Anzeige Fensters. Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Anzeige Fensters (normalerweise der Desktop), wenn das Flag "Style Child" für den Befehl " [Öffnen](open.md) " verwendet wurde. Um die Position des Fensters zu ändern, ohne die Höhe oder Breite zu ändern, geben Sie 0 für Höhe und Breite an. |
| Fenster Client                | Stellt den Client Bereich des Fensters wieder her.                                                                                                                                                                                                                                                                                                               |
| Fenster Client bei *Rechteck* | Ändert die Größe und Position des Client Bereichs des Fensters. Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Client Fensters. Um die Position des Fensters zu ändern, ohne die Höhe oder Breite zu ändern, geben Sie 0 für Höhe und Breite an.                                                                                      |



 

Wenn ein Flag ein Rechteck enthält, sind die Rechteck Koordinaten relativ zum Fenster Ursprung oder dem Bild Ursprung, wenn dies erforderlich ist, und werden als **x1 y1 x2 Y2** angegeben. Die Koordinaten **X1Y1** geben die linke obere Ecke an, und die Koordinaten **X2Y2** geben die Breite und Höhe des Rechtecks an.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Der Put-Befehl definiert bei der Arbeit mit Video Überlagerungs Geräten mindestens eine der folgenden Rechtecke:

-   Das Video Rechteck definiert den Bereich des zu erfassenden eingehenden Video Bilds.
-   Das Rahmen Rechteck definiert den Bereich des Frame Puffers, der das eingehende Video Bild empfängt.
-   Das Quell Rechteck definiert, welcher Bereich des Frame Puffers in das Ziel Rechteck kopiert wird.
-   Das Ziel Rechteck definiert den Bereich des Client Bereichs des Anzeige Fensters, der das Video Bild empfängt.

Das Video Rechteck ist mit dem Frame Rechteck identisch, ebenso wie das Quell Rechteck mit dem Ziel Rechteck verknüpft ist. Die Streckung kann vom Video Rechteck bis zum Frame Rechteck und vom Quell Rechteck bis zum Ziel Rechteck erfolgen. Nicht alle Geräte unterstützen die Streckung, und die Streckung muss aktiviert sein (mit dem [Set](set.md) -Befehl).

Mit dem folgenden Befehl werden drei Bereiche für das Video, den Frame und die Quelle definiert.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Die Regionen in diesem Beispiel werden wie folgt definiert:

-   Ein Bereich von 200 bis 200 Pixel der eingehenden Videodaten, beginnend bei einem Ursprung 120 Pixel von der oberen linken Ecke, wird im Frame Puffer aufgezeichnet.
-   Die Videodaten werden in einem Bereich von 200 bis 200 Pixel in der oberen linken Ecke des Frame Puffers platziert.
-   Übertragungen werden vom Bereich 200 bis 200 Pixel in der linken oberen Ecke des Frame Puffers zum Zielfenster durchgeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

