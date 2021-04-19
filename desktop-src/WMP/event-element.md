---
title: Event-Element (WMP-SDK)
description: Das-Ereignis Element definiert ein Verhalten oder eine Aktion, die von Windows Media Player ausgeführt wird, wenn ein Skript Befehl, der als Ereignis bezeichnet wird, empfangen wird.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Windows Media Player-Ereignis Element
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370529"
---
# <a name="event-element"></a>Event-Element

Das- **Ereignis** Element definiert ein Verhalten oder eine Aktion, die von Windows Media Player ausgeführt wird, wenn ein Skript Befehl, der als Ereignis bezeichnet wird, empfangen wird.

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a>Attribute

**Name** (erforderlich)

Der Name des Ereignisses.

**Whendone** (erforderlich)

Ein Wert, der definiert, welche Windows-Media Player nach dem Wiedergeben des referenzierten Inhalts funktioniert.

Die folgenden Werte sind möglich.



| Wert  | BESCHREIBUNG                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RESUME | Der aktuelle Eintrag (der durch das Ereignis unterbrochene Clip) setzt die Wiedergabe fort. Wenn der Inhalt als Inhalt gespeichert wird, wird er an derselben Stelle fortgesetzt, an der er angehalten wurde. Wenn der Inhalt übertragen wird, wird er an der aktuellen Position fortgesetzt.        |
| NEXT   | Das nächste **Entry** -Element wird so abgespielt, als wäre das Ereignis nicht aufgetreten, und Windows Media Player hat das Ende des aktuellen Clips erreicht.                                                                                             |
| BREAK  | Wenn sich der aktuelle Eintrag innerhalb einer **Wiederholungs** Schleife befindet, wird die Schleife beendet, als ob die Wiederholungs Anzahl abgeschlossen wurde. Andernfalls springt Windows Media Player zum Ende der Wiedergabeliste, als wäre der abschließende Eintrag wie gewohnt abgeschlossen worden. |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                |
|-----------------|-------------------------|
| Übergeordnete Elemente | **ASX**                 |
| Untergeordnete Elemente  | **Eintrag**, **ENTRYREF** |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert ein Verhalten oder eine Aktion, die von Windows Media Player ausgeführt wird, wenn ein Skript Befehl, der als Ereignis bezeichnet wird, empfangen wird. Bei einem Ereignis handelt es sich um einen bestimmten Typ von Skript Befehl, der in einen an Windows gesendeten Stream eingebettet ist Media Player der aus einer doppelten Zeichenfolge besteht. Die erste Zeichenfolge ist das Wort "Event", die zweite Zeichenfolge ist der Ereignis Name. Der Ereignis Name in der zweiten Zeichenfolge muss mit dem in der Metadatei definierten Ereignis Namen identisch sein. (Bei der Entsprechung wird die Groß-/Kleinschreibung nicht beachtet. Ereignisse können an Windows gesendet werden, Media Player einen Echtzeit-Stream empfängt, oder Sie können in einer. ASF-, WMA-oder WMV-Datei gespeichert werden, die als Bedarfs gesteuerter unicaststream zugestellt wird. Wenn Windows Media Player den Skript Befehl empfängt, wird das-Ereignis wie im- **Ereignis** Element definiert verarbeitet.

Dieses Element definiert einen Bereich von **Entry** -oder **ENTRYREF** -Elementen, die verarbeitet werden, wenn Windows Media Player den Skript Befehl mit dem benannten Ereignis empfängt. **ENTRYREF** kann eine URL sein, die auf eine ASP-Seite verweist. Mit diesem Element können Sie ein Verhalten für den Datenstrom Wechsel nahezu in Echtzeit angeben, im Gegensatz zu vordefinierten streamänderungen, die Verweise auf andere Inhalts Teile oder Windows Media-Metadateien verwenden.

Wenn Sie ASP-Seiten zum Generieren von Wiedergabelisten verwenden, müssen Sie einen Wert für die *Antwort* angeben. **ContentType** -Eigenschaft und die *Antwort*. **läuft** die Eigenschaft auf der ASP-Seite aufgrund von Latenzproblemen mit Windows-Media Player ab. Die *Antwort*. **ContentType** muss eine gültige Dateinamenerweiterung für Windows Media-Metadateien sein. Gültige Typen sind:. ASF,. ASX,. WMA,. Wax,. WMV und. wvx.

Ausführliche Informationen zur Verwendung des **Antwort** Objekts in ASP finden Sie im Platform SDK.

Dieses Element kann an beliebiger Stelle innerhalb des **ASX** -Elements vorkommen. Wenn mehrere **Ereignis** Elemente in einem **ASX** -Element identische Werte für Ihre **namens** Attribute aufweisen, verwendet Windows Media Player das erste Vorkommen innerhalb des Elements " **ASX** " und ignoriert alle anderen Elemente. Wenn **Ereignis** Elemente über unterschiedliche **namens** Attribute verfügen, spielt die Reihen **Folge im-Element des-** Elements keine Rolle.

Windows Media Player verwirft Ereignisse, die während der Verarbeitung eines anderen Ereignisses empfangen werden. Das Schachteln von Ereignissen wird nicht unterstützt. Wenn sich Windows Media Player im Vorschaumodus befindet, wird der Ereignis Inhalt durch das **previewduration** -Element nicht eingeschränkt. die vollständige Länge der Ereignis Inhalte kann auch dann wiedergegeben werden, wenn die Vorschau Dauer für das aktive **Eintrags** Element vor dem Ende des Ereignisses abläuft.

## <a name="examples"></a>Beispiele

Wenn in diesem Beispiel Windows Media Player das Skript Befehls Ereignis und die Befehls Zeichenfolge "AdLINK" in den Streamingmedien empfängt, das Sie rendert, wird die Wiedergabeliste nach einem **EventName** "AdLINK" durchsucht. Windows Media Player schaltet von dem Stream, den er rendert, und gibt den Inhalt wieder, auf den im **Ereignis**"" verwiesen wird https://example.microsoft.com/adlink.htm .

Das **Eintrags** Attribut **clientskip** ist auf Nein festgelegt, um zu verhindern, dass der **Ereignis** Clip ausgelassen wird. Er muss wiedergegeben werden.

Das Skript `WHENDONE="RESUME"` weist Windows Media Player an, die Wiedergabe des vorherigen Mediums fortzusetzen, von dem es gewechselt hat, sobald "AdLINK. ASF" abgeschlossen ist.


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> <dt>

[**Windows Media Player-Objektmodell**](windows-media-player-object-model.md)
</dt> </dl>

 

 





