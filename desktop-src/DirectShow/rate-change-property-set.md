---
description: Der Satz ändern-Eigenschaften Satz ermöglicht MPEG-2-Quell-/Parserfilter zum Ändern der Wiedergabe Rate. MPEG-2-Decoder sollten diesen Eigenschaften Satz unterstützen. Der DVD-Navigator und die Streampuffer-Engine verwenden diese Eigenschaft, um die Wiedergabe Raten zu steuern.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Eigenschaften Satz für Raten Änderung (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56b679b0ce9b0127b15c69cd02b016a4990b6f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370089"
---
# <a name="rate-change-property-set"></a>Eigenschaften Satz für Raten Änderung

Der Satz ändern-Eigenschaften Satz ermöglicht MPEG-2-Quell-/Parserfilter zum Ändern der Wiedergabe Rate. MPEG-2-Decoder sollten diesen Eigenschaften Satz unterstützen. Der DVD-Navigator und die Streampuffer-Engine verwenden diese Eigenschaft, um die Wiedergabe Raten zu steuern.



|                   |                               |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropltid \_ |



 



| Eigenschafts-ID                                                                   | BESCHREIBUNG                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**Bei \_ Raten \_ Korrekturen**](am-rate-correctts-property.md)                     | Informiert den Decoder, dass der Navigator die richtigen Zeitstempel festlegt.             |
| \_Ate \_ exactratechange                                                     | Veraltet.                                                                              |
| [**\_Rate \_ maxfulldatarate**](am-rate-maxfulldatarate-property.md)         | Fragt den Decoder nach der maximalen Datenrate des Decoders ab.                               |
| [**\_Rate \_ queryfullframerate**](am-rate-queryfullframerate-property.md)   | Fragt den Decoder nach der maximalen voll Bild Rate des Decoders ab.                         |
| [**\_Rate der \_ querylastratesegpts**](am-rate-querylastratesegpts-property.md) | Fragt den Decoder nach der Startzeit des Raten Segments ab, das zuletzt festgelegt wurde. |
| [**AM \_ raten Sie \_ simpleratechange**](am-rate-simpleratechange-property.md)       | Sendet eine Raten Änderung an den Decoder.                                                    |
| \_Raten \_ Schritt                                                                | Veraltet. Siehe [Frame Stepping-Eigenschaften Satz](frame-stepping-property-set.md).          |
| [**\_ \_ Userateversion für ATE**](am-rate-userateversion-property.md)           | Gibt an, welche Version des Raten Änderungs Mechanismus verwendet werden soll.                           |



 

## <a name="remarks"></a>Bemerkungen

Im Zusammenhang mit diesem Eigenschaften Satz misst die Rate die Rate, mit der Zeitstempel relativ zur Referenzuhr fortgesetzt werden. Die Umkehrung der Wiedergabegeschwindigkeit bewerten. Wenn die Wiedergabegeschwindigkeit beispielsweise 2 x beträgt, müssen die Zeitstempel um 1/2 den normalen Kurs erhöhen. Dies führt zu einer schnelleren Wiedergabegeschwindigkeit, da Beispiele vor der normalen Darstellung gerendert werden.

Die Beispiele werden an den Decoder mit einem Zeitstempel gesendet, der der Präsentationszeit bei der 1X-Rate entspricht. Der Decoder muss die Zeitstempel der Ausgabe Beispiele auf die richtige Präsentationszeit für die aktuelle Rate skalieren. Wenn die Rate z. b. 1/2 beträgt (was bedeutet, dass die Wiedergabegeschwindigkeit 2X ist), muss der Decoder die Zeitstempel um 1/2 skalieren. Im Allgemeinen haben nur I-Frames Zeitstempel. Der Decoder muss die Zeitstempel für die Rahmen B und P interpolieren. Beachten Sie, dass Zeitstempel während der umgekehrten Wiedergabe weiter zunehmen – Zeitstempel werden nie rückwärts geschaltet.

Es sind zwei Versionen der Eigenschaften Gruppe "Raten Änderung" definiert: Version 1,0 und Version 1,1. Das Standardverhalten wird durch Version 1,0 angegeben. Decoderhersteller werden empfohlen, Version 1,1 zu unterstützen, da Sie ein glatteres Wiedergabe Verhalten bietet. Der DVD-Navigator verwendet zurzeit Version 1,0. Die streampufferengine verwendet die Version 1,1.

### <a name="rate-change-version-10"></a>Änderungs Rate Version 1,0

Version 1,0 des Eigenschaften Satzes "Raten Änderung" definiert das Standardverhalten für MPEG-2-Decoders.

Der Quell Filter signalisiert eine Änderung der Rate durch Festlegen der "ATE"- [**\_ \_ simpleratechange**](am-rate-simpleratechange-property.md) -Eigenschaft. Die Daten für diese Eigenschaft sind die neue Rate, zuzüglich der Startzeit für das Eingabe Beispiel, wenn die Rate wirksam wird. Der Decoder verwaltet eine Warteschlange mit ausstehenden Raten Änderungen, sortiert nach Startzeit.

Bevor der DVD-Navigator zu einer nicht-1-x-Geschwindigkeit wechselt, werden alle ausstehenden Beispiele übermittelt, die Rate temporär auf 1,0 festgelegt und das Diagramm geleert. Anschließend wird die neue Rate festgelegt. Alle Raten Änderungen werden für das Ende der aktuellen vobu (Video Object Unit) geplant. Beachten Sie, dass beim Leeren des Diagramms die Präsentationszeit auf 0 zurückgesetzt wird.

Der DVD-Navigator funktioniert entweder im *Smooth-Modus* oder im Überprüfungs *Modus*. Im Smooth-Modus wird jeder Frame an den Decoder gesendet, einschließlich B-Frames und P-Frames. Der DVD-Navigator verwendet den Smooth-Modus, wenn die Wiedergabegeschwindigkeit größer als 0 (null), aber kleiner als die erneute fehlerhafter-Datenrate des Decoders Wenn die Wiedergabegeschwindigkeit kleiner als 0 (null) ist oder die maximale Datenrate des Decoders überschreitet, verwendet der DVD-Navigator den Überprüfungs Modus, in dem nur die I-Frames an den Decoder gesendet werden. Mit sehr hoher Geschwindigkeit können einige I-Frames übersprungen werden. Beispielsweise kann Sie alle anderen I-Frames senden.

Standardmäßig trauert der DVD-Navigator den Audiostream auf andere Raten als 1,0. Sie können dies ändern, indem Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) mit dem DVD \_ audioduringffwdrew-Flag aufrufen.

### <a name="rate-change-version-11"></a>Änderungs Rate Version 1,1

Die Version 1,1 der festgelegten Eigenschaft "Raten Änderung" folgt denselben Grundprinzipien wie Version 1,0, mit den folgenden unterschieden:

-   Der Quell Filter signalisiert dem Decoder, Version 1,1 zu verwenden, indem die Eigenschaft für die [**\_ \_ userateversion**](am-rate-userateversion-property.md) -Eigenschaft festgelegt wird. Andernfalls sollte der Decoder das Verhalten der Version 1,0 verwenden.
-   Der Quell Filter leert das Diagramm nicht zwischen Raten Änderungen. Zeitstempel werden daher monoton über Kurs Änderungs Grenzen hinweg erhöht und nicht auf Null zurückgesetzt.
-   Anstatt eine Raten Änderung für eine bestimmte Verweis Zeit in die Warteschlange zu stellen, kann der Quell Filter angeben, dass eine Raten Änderung für das *am weitesten* oben stehende Beispiel des Decoders gilt, das als Beispiel am Anfang der ausgehenden Warteschlange des Decoders definiert ist. Zu diesem Zweck verwendet der Quell Filter die " [**am \_ Rate \_ simpleratechange**](am-rate-simpleratechange-property.md) "-Eigenschaft, legt jedoch die Startzeit auf-1 fest.
-   Der Quell Filter kann den Decoder nach der Startzeit der in der Warteschlange befindlichen Änderungs Rate Abfragen. Zu diesem Zweck wird die [**\_ Bitrate \_ querylastratesegpts**](am-rate-querylastratesegpts-property.md) -Eigenschaft verwendet.
-   Der Quell Filter löscht keine Stichproben. Wenn die Rate die maximale Datenrate des Decoders überschreitet, sollte der Decoder bei Bedarf Frames löschen.
-   Der Quell Filter stumm lässt den Audiodatenstrom nicht, unabhängig von der maximalen Datenrate des Audiodecoders. Der Audiodecoder kann Beispiele ablegen, wenn die Wiedergabegeschwindigkeit die maximale Rate des Decoders überschreitet. Die Warteschlange für geplante Raten Änderungen sollte jedoch weiterhin beibehalten werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




