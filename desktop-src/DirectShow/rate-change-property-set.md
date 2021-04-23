---
description: Der Eigenschaftensatz "Rate Change" aktiviert MPEG-2-Quell-/Parserfilter, um die Wiedergaberate zu ändern. MPEG-2-Decoder sollten diesen Eigenschaftensatz unterstützen. Der DVD-Navigator und die Streampuffer-Engine verwenden beide diese Eigenschaft, um die Wiedergaberaten zu steuern.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Ratenänderungseigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb222f8a2fe388d8ea582448d2ba5aa6c9d7e80
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909608"
---
# <a name="rate-change-property-set"></a>Ratenänderungseigenschaftensatz

Der Eigenschaftensatz "Rate Change" aktiviert MPEG-2-Quell-/Parserfilter, um die Wiedergaberate zu ändern. MPEG-2-Decoder sollten diesen Eigenschaftensatz unterstützen. Der DVD-Navigator und die Streampuffer-Engine verwenden beide diese Eigenschaft, um die Wiedergaberaten zu steuern.



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |



 



| Eigenschafts-ID                                                                   | BESCHREIBUNG                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**AM \_ RATE \_ CorrectTS**](am-rate-correctts-property.md)                     | Informiert den Decoder, dass der Navigator die richtigen Zeitstempel festlegt.             |
| AM \_ RATE \_ ExactRateChange                                                     | Veraltet.                                                                              |
| [**AM \_ RATE \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Fragt den Decoder nach der maximalen Datenrate des Decoders ab.                               |
| [**AM \_ RATE \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | Fragt den Decoder nach der maximalen Vollbildrate des Decoders ab.                         |
| [**AM \_ RATE \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Fragt den Decoder nach der Startzeit des zuletzt festgelegten Ratensegments ab. |
| [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Sendet eine Ratenänderung an den Decoder.                                                    |
| AM \_ \_ RATE-Schritt                                                                | Veraltet. Weitere Informationen finden [Sie unter Frame Stepping Property Set](frame-stepping-property-set.md).          |
| [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)           | Gibt an, welche Version des Mechanismus zur Änderung der Rate verwendet werden soll.                           |



 

## <a name="remarks"></a>Bemerkungen

Im Kontext dieses Eigenschaftssatzes misst rate die Rate, mit der Zeitstempel relativ zur Referenzuhr vorn sind. Bewerten Sie die Umkehrung der Wiedergabegeschwindigkeit. Wenn die Wiedergabegeschwindigkeit beispielsweise 2x beträgt, müssen die Zeitstempel mit 1/2 der normalen Rate erhöht werden. Dies führt zu einer schnelleren Wiedergabegeschwindigkeit, da Beispiele früher als normal gerendert werden.

Stichproben werden mit einem Zeitstempel, der der Präsentationszeit entspricht, mit einer 1-fachen Rate an den Decoder gesendet. Der Decoder muss die Zeitstempel der Ausgabebeispiele auf die richtige Präsentationszeit für die aktuelle Rate skalieren. Wenn die Rate beispielsweise 1/2 beträgt (d. h. die Wiedergabegeschwindigkeit ist 2x), muss der Decoder die Zeitstempel um 1/2 skalieren. Im Allgemeinen verfügen nur I-Frames über Zeitstempel. Der Decoder muss die Zeitstempel für die Frames B und P interpolieren. Beachten Sie, dass zeitstempel während der umgekehrten Wiedergabe weiter zunehmen – Zeitstempel gehen nie rückwärts.

Es werden zwei Versionen des Eigenschaftensatzes Rate Change definiert: Version 1.0 und Version 1.1. Das Standardverhalten wird in Version 1.0 angegeben. Decoderanbietern wird empfohlen, Version 1.1 zu unterstützen, da sie eine reibungslosere Wiedergabeerfahrung bietet. Der DVD-Navigator verwendet derzeit Version 1.0. Die Streampuffer-Engine verwendet Version 1.1.

### <a name="rate-change-version-10"></a>Rate Change Version 1.0

Version 1.0 des Eigenschaftensatzes "Rate Change" definiert das Standardverhalten für MPEG-2-Decoder.

Der Quellfilter signalisiert eine Ratenänderung, indem er die [**AM \_ RATE \_ SimpleRateChange-Eigenschaft**](am-rate-simpleratechange-property.md) festlegt. Die Daten für diese Eigenschaft sind die neue Rate zuzüglich der Startzeit für das Eingabebeispiel, wenn die Rate wirksam wird. Der Decoder verwaltet eine Warteschlange mit ausstehenden Ratenänderungen, sortiert nach Startzeit.

Bevor der DVD-Navigator in eine Geschwindigkeit ungleich 1 geändert wird, werden alle ausstehenden Stichproben übermittelt, die Rate vorübergehend auf 1,0 festgelegt und das Diagramm geleert. Anschließend wird die neue Rate festgelegt. Alle Ratenänderungen werden für das Ende der aktuellen VOBU (Videoobjekteinheit) geplant. Beachten Sie, dass durch das Leeren des Diagramms die Präsentationszeit auf 0 (null) zurückgesetzt wird.

Der DVD-Navigator arbeitet entweder im *smooth-Modus* oder im *Scanmodus.* Im smooth-Modus sendet er jeden Frame an den Decoder, einschließlich B- und P-Frames. Der DVD-Navigator verwendet den smooth-Modus, wenn die Wiedergabegeschwindigkeit größer als 0 (null), aber kleiner als die maximale Datenrate des Decoders ist. Wenn die Wiedergabegeschwindigkeit kleiner als 0 (umgekehrte Wiedergabe) ist oder die maximale Datenrate des Decoders überschreitet, verwendet der DVD-Navigator den Scanmodus, in dem nur die I-Frames an den Decoder gesendet werden. Bei sehr hohen Geschwindigkeiten können einige I-Frames übersprungen werden. Beispielsweise kann er jeden anderen I-Frame senden.

Standardmäßig stummschaltt der DVD-Navigator den Audiostream für andere Raten als 1,0. Sie können dies ändern, indem Sie [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) mit dem FLAG DVD \_ AudioDuringFFwdRew aufrufen.

### <a name="rate-change-version-11"></a>Rate Change Version 1.1

Version 1.1 des Eigenschaftensatzes "Rate Change" folgt den gleichen Grundprinzipien wie Version 1.0, mit den folgenden Unterschieden:

-   Der Quellfilter signalisiert dem Decoder, Version 1.1 zu verwenden, indem er die [**AM \_ RATE \_ UseRateVersion-Eigenschaft**](am-rate-userateversion-property.md) festlegt. Andernfalls sollte der Decoder das Verhalten von Version 1.0 verwenden.
-   Der Quellfilter leert das Diagramm nicht zwischen Ratenänderungen. Zeitstempel erhöhen sich daher monoton über die Begrenzungen der Geschwindigkeitsänderung, anstatt auf 0 zurückgesetzt zu werden.
-   Anstatt eine Änderung der Rate für eine bestimmte Referenzzeit in die Warteschlange zu stellen, kann der Quellfilter angeben, dass eine Änderung der Rate für die am häufigsten weitergeleitete Stichprobe des Decoders *gilt,* die als Stichprobe am Anfang der ausgehenden Warteschlange des Decoders definiert ist. Dazu verwendet der Quellfilter die [**AM \_ RATE \_ SimpleRateChange-Eigenschaft,**](am-rate-simpleratechange-property.md) legt die Startzeit jedoch auf -1 fest.
-   Der Quellfilter kann den Decoder nach der Startzeit der Änderung der Rate abfragen, die zuletzt in die Warteschlange gestellt wurde. Zu diesem Zweck [**wird die AM \_ \_ RATE-Eigenschaft QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) verwendet.
-   Der Quellfilter gibt keine Stichproben aus. Wenn die Rate die maximale Datenrate des Decoders überschreitet, sollte der Decoder Frames nach Bedarf ablegen.
-   Der Quellfilter stummschaltt den Audiodatenstrom nicht, unabhängig von der maximalen Datenrate des Audiodecoders. Der Audiodecoder kann Stichproben ablegen, wenn die Wiedergabegeschwindigkeit die maximale Rate des Decoders überschreitet. Es sollte jedoch weiterhin die Warteschlange geplanter Änderungen der Rate erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




