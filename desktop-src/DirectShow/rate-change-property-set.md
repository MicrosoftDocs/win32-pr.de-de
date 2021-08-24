---
description: Der Eigenschaftensatz Rate Change ermöglicht MPEG-2-Quell-/Parserfiltern, die Wiedergaberate zu ändern. MPEG-2-Decoder sollten diesen Eigenschaftensatz unterstützen. Der DVD-Navigator und die Streampuffer-Engine verwenden beide diese Eigenschaft, um die Wiedergaberaten zu steuern.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Rate Change Property Set (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5299b744869a4c9a12b50a9e738104999aab5dcd19a800fc0ac3ddb3717e8617
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747410"
---
# <a name="rate-change-property-set"></a>Rate Change Property Set

Der Eigenschaftensatz Rate Change ermöglicht MPEG-2-Quell-/Parserfiltern, die Wiedergaberate zu ändern. MPEG-2-Decoder sollten diesen Eigenschaftensatz unterstützen. Der DVD-Navigator und die Streampuffer-Engine verwenden beide diese Eigenschaft, um die Wiedergaberaten zu steuern.



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |



 



| Eigenschafts-ID                                                                   | BESCHREIBUNG                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**AM \_ RATE \_ CorrectTS**](am-rate-correctts-property.md)                     | Informiert den Decoder darüber, dass der Navigator die richtigen Zeitstempel festsetzt.             |
| AM \_ RATE \_ ExactRateChange                                                     | Veraltet.                                                                              |
| [**AM \_ RATE \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Fragt den Decoder nach der maximalen Datenrate des Decoders ab.                               |
| [**AM \_ RATE \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | Fragt den Decoder nach der maximalen Vollbildrate des Decoders ab.                         |
| [**AM \_ RATE \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Fragt den Decoder nach der Startzeit des Rate-Segments ab, das zuletzt festgelegt wurde. |
| [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Sendet eine Ratenänderung an den Decoder.                                                    |
| AM \_ \_ RATE-Schritt                                                                | Veraltet. Weitere Informationen finden [Sie unter Frame Stepping Property Set](frame-stepping-property-set.md).          |
| [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)           | Gibt an, welche Version des Mechanismus zur Änderung der Rate verwendet werden soll.                           |



 

## <a name="remarks"></a>Hinweise

Im Kontext dieses Eigenschaftssatzes misst rate die Rate, mit der Zeitstempel relativ zur Referenzuhr vorn sind. Bewerten Sie die Umkehrung der Wiedergabegeschwindigkeit. Wenn die Wiedergabegeschwindigkeit beispielsweise das 2-fache beträgt, müssen die Zeitstempel mit 1/2 der normalen Rate erhöht werden. Dies führt zu einer schnelleren Wiedergabegeschwindigkeit, da Beispiele früher als normal gerendert werden.

Stichproben werden mit einem Zeitstempel, der der Präsentationszeit entspricht, mit einer 1-fachen Rate an den Decoder gesendet. Der Decoder muss die Zeitstempel der Ausgabebeispiele auf die richtige Präsentationszeit für die aktuelle Rate skalieren. Wenn die Rate beispielsweise 1/2 beträgt (d. h. die Wiedergabegeschwindigkeit ist 2x), muss der Decoder die Zeitstempel um 1/2 skalieren. Im Allgemeinen verfügen nur I-Frames über Zeitstempel. Der Decoder muss die Zeitstempel für die Frames B und P interpolieren. Beachten Sie, dass zeitstempel während der umgekehrten Wiedergabe weiter zunehmen – Zeitstempel gehen nie rückwärts.

Es werden zwei Versionen des Eigenschaftensatzes Rate Change definiert: Version 1.0 und Version 1.1. Das Standardverhalten wird in Version 1.0 angegeben. Decoderanbietern wird empfohlen, Version 1.1 zu unterstützen, da sie eine reibungslosere Wiedergabeerfahrung bietet. Der DVD-Navigator verwendet derzeit Version 1.0. Die Streampuffer-Engine verwendet Version 1.1.

### <a name="rate-change-version-10"></a>Rate Change Version 1.0

Version 1.0 des Eigenschaftensatzes rate change definiert das Standardverhalten für MPEG-2-Decoder.

Der Quellfilter signalisiert eine Änderung der Rate durch Festlegen der [**\_ \_ SimpleRateChange-Eigenschaft AM RATE.**](am-rate-simpleratechange-property.md) Die Daten für diese Eigenschaft sind die neue Rate plus die Startzeit für die Eingabestichprobe, wenn die Rate wirksam wird. Der Decoder verwaltet eine Warteschlange ausstehender Ratenänderungen, sortiert nach Startzeit.

Bevor sich der DVD-Navigator in eine geschwindigkeitsfreie Geschwindigkeit ändert, stellt er alle ausstehenden Stichproben aus, legt die Rate vorübergehend auf 1,0 fest und leert das Diagramm. Anschließend wird die neue Rate definiert. Alle Änderungen an der Rate werden für das Ende der aktuellen VOBU-Einheit (Videoobjekteinheit) geplant. Beachten Sie, dass beim Leeren des Graphen die Präsentationszeit auf 0 zurückgesetzt wird.

Der DVD-Navigator arbeitet entweder im *reibungslosen Modus oder* im *Scanmodus.* Im reibungslosen Modus sendet er jeden Frame an den Decoder, einschließlich B-Frames und P-Frames. Der DVD-Navigator verwendet den reibungslosen Modus, wenn die Wiedergabegeschwindigkeit größer als 0 (null), aber kleiner als die maximale Datenrate des Decoders ist. Wenn die Wiedergabegeschwindigkeit kleiner als 0 (null) ist (umgekehrte Wiedergabe) oder die maximale Datenrate des Decoders überschreitet, verwendet der DVD-Navigator den Scanmodus, in dem er nur die I-Frames an den Decoder sendet. Bei sehr hohen Geschwindigkeiten kann es sein, dass einige I-Frames übersprungen werden. Beispielsweise kann jeder andere I-Frame gesendet werden.

Standardmäßig stummschaltt der DVD-Navigator den Audiodatenstrom für andere Raten als 1,0. Sie können dies ändern, indem [**Sie IDvdControl2::SetOption mit**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) dem DVD-Flag \_ AudioDuringFFwdRew aufrufen.

### <a name="rate-change-version-11"></a>Rate Change Version 1.1

Version 1.1 des Eigenschaftensatzes "Rate Change" folgt den gleichen Grundprinzipien wie Version 1.0, mit den folgenden Unterschieden:

-   Der Quellfilter signalisiert dem Decoder die Verwendung von Version 1.1 durch Festlegen der [**AM \_ RATE \_ UseRateVersion-Eigenschaft.**](am-rate-userateversion-property.md) Andernfalls sollte der Decoder das Verhalten der Version 1.0 verwenden.
-   Der Quellfilter leert das Diagramm nicht zwischen Denkratenänderungen. Zeitstempel erhöhen sich daher monoton über die Begrenzungen der Geschwindigkeitsänderung, anstatt auf Null zurückgesetzt zu werden.
-   Anstatt eine Änderung der Rate für eine bestimmte Referenzzeit in die Warteschlange zu stellen, kann der Quellfilter angeben, dass eine Änderung der Rate für die am stärksten vorwärts gehende Stichprobe des Decoders *gilt,* die als Stichprobe am Anfang der ausgehenden Warteschlange des Decoders definiert ist. Dazu verwendet der Quellfilter die [**AM \_ RATE \_ SimpleRateChange-Eigenschaft,**](am-rate-simpleratechange-property.md) legt die Startzeit jedoch auf -1 fest.
-   Der Quellfilter kann den Decoder nach der Startzeit der Änderung der Rate abfragen, die zuletzt in die Warteschlange gestellt wurde. Zu diesem Zweck [**wird die AM RATE \_ \_ QueryLastRateSegPTS-Eigenschaft**](am-rate-querylastratesegpts-property.md) verwendet.
-   Der Quellfilter gibt keine Stichproben aus. Wenn die Rate die maximale Datenrate des Decoders überschreitet, sollte der Decoder Frames nach Bedarf ablegen.
-   Der Quellfilter stummschaltt den Audiostream nicht, unabhängig von der maximalen Datenrate des Audiodecoders. Der Audiodecoder kann Stichproben ablegen, wenn die Wiedergabegeschwindigkeit die maximale Rate des Decoders überschreitet. Sie sollte jedoch weiterhin die Warteschlange geplanter Änderungen der Rate verwalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




