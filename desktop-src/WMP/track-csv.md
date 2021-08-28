---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player,track.csv
- Onlineshops,track.csv
- Geben Sie 1 Onlineshops ein, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9561897fb68f53aaa4ba33e433cf6d6120ec315
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474916"
---
# <a name="trackcsv"></a>track.csv

Diese Datei enthält einen Eintrag für jede Spur im Katalog. Jeder Eintrag ist eine Zeile, die aus den Feldern mit Tabstopptrennzeichen besteht, die in der folgenden Tabelle beschrieben sind. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Die Spalte Format in der folgenden Tabelle beschreibt die Formatierung der einzelnen Unicode-Textfelder. Er bezieht sich nicht auf den Datentyp des Inhalts. Wenn beispielsweise Integer in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen ganzen Zahl darstellt.




| Feld | Erforderlich | Format | BESCHREIBUNG | 
|-------|----------|--------|-------------|
| Trackid | Ja | Nicht negative ganze Zahl. Beispiel: 32789<br /> | Eindeutiger Bezeichner, der vom Inhaltsanbieter bereitgestellt wird. Muss kleiner als 2^32 sein. Leistungstipp: Wenn die IDs, die Titeln aus dem gleichen Album zugewiesen sind, fortlaufend nummeriert werden, ist die Katalogkomprimierung effizienter. Die fortlaufende Nummerierung von Albumtiteln ist jedoch nicht erforderlich.<br /> | 
| TrackTitle | Ja | Unicode-Zeichenfolge. Beispiel: Raygun-Blaublau | Name der Spur | 
| Duration | Ja | Nicht negative ganze Zahl. Beispiel: 543<br /> | Dauer der Spur in Sekunden. | 
| TrackNumber | Ja | Nicht negative ganze Zahl. Beispiel: 7<br /> | Titelnummer auf dem Album des Titels. Nachverfolgungsnummern beginnen bei 1 und erhöhen sich über Datenträgersätze hinweg. Die Tracknummer muss kleiner als 256 sein. Eine Titelnummer größer oder gleich 256 verursacht unerwartetes Verhalten in Windows Media Player. | 
| TrackPrice | Ja | Unicode-Zeichenfolge. Beispiel: 0,99 USD. | Nachverfolgen des Preises. Das Währungssymbol sollte enthalten sein. Die leere Zeichenfolge 0 und - haben eine besondere Bedeutung. Eine leere Zeichenfolge gibt an, dass der Preis unbekannt ist. Eine Null in diesem Feld bedeutet, dass die Spur frei ist, und ein Bindestrich (-) gibt an, dass die Spur nicht gekauft werden kann. | 
| CanStream | Ja | Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br /> | Gibt an, ob die Spur gestreamt werden kann. | 
| CanDownload | Ja | Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br /> | Gibt an, ob die Spur heruntergeladen werden kann. | 
| HasPreviewClip | Ja | Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br /> | Gibt an, ob die Spur über einen Vorschauclip verfügt. | 
| HasVideoClip | Ja | Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br /> | Gibt an, ob die Spur über einen Videoclip verfügt. | 
| ParentalRating | Ja | Enumeration. Kann N, E oder C sein. Beispiel: N<br /> | Gibt die Bewertung der Elternempfehlung an. Die Werte N, E und C stehen für Normal, Explicit und Clean. | 
| LinkedGekoppeltID | Ja | Nicht negative ganze Zahl. Muss die ID eines Albums sein. Beispiel: 32423 | Die ID des Albums, das diesen Titel enthält.<blockquote>[!Note]<br />Jeder Titel muss zu einem Album gehören. Das heißt, dass das Feld Linked Dateitypid für jeden Titel einer der Album-IDs in der album.csv sein muss.</blockquote><br /> | 
| LinkedTrackArtist_ArtistIDs | Ja | Liste der ganzen Zahlen. Die Liste enthält durch Semikolons getrennte Interpreten-IDs. Beispiel: 41322;12321; 82123; | Eine Liste der IDs, die den Mitwirkenden entspricht. | 
| Composer | Nein | Unicode-Zeichenfolge. Beispiel: Über | Der Composer des Titels. Wenn für das Genre der Spur das Feld HasComposer nicht festgelegt ist, wird der Wert Composer Felds ignoriert. Wird in der Regel nur für Jazz- oder klassische Spuren verwendet. | 
| Beliebtheit | Ja | Nicht negative ganze Zahl oder Float.Beispiel: 1252.6<br /> | Bestimmt die Position der Spur in der Liste, wenn sie nach Beliebtheit sortiert ist. Eine niedrigere Zahl weist auf eine höhere Beliebtheit hin. | 
| StarRating | Nein | Float.Example: 4.21<br /> | Die Sternbewertung wird auf den nächsten 1/4-Stern gerundet, indem Windows Media Player wird, bevor sie auf der Windows Media Player angezeigt wird. | 




 

 

 





