---
title: Player. openstate
description: Die openstate-Eigenschaft ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player. openstate-Windows-Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367531"
---
# <a name="playeropenstate"></a>Player. openstate

Die **openstate** -Eigenschaft ruft einen Wert ab, der den Zustand der Inhaltsquelle angibt.

## <a name="syntax"></a>Syntax

*Player* . **openstate**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**). Die Enumerationskonstante im C-Stil kann durch Voranstellen des Zustands Werts mit "wmpos" abgeleitet werden. Beispielsweise ist die Konstante für den playlistopening-Zustand **wmposplaylistopening**.



| Wert | State                   | BESCHREIBUNG                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nicht definiert               | Windows Media Player befindet sich in einem nicht definierten Zustand.                                                                                                         |
| 1     | Playlistchanging        | Neue Wiedergabeliste wird geladen.                                                                                                                    |
| 2     | Playlistlokalisierung        | Windows Media Player versucht, die Wiedergabeliste zu finden. Die Wiedergabeliste kann lokal (Bibliothek oder Metadatei mit der Dateinamenerweiterung. ASX) oder Remote sein. |
| 3     | Playlistconnecting      | Verbindung mit der Wiedergabeliste wird hergestellt.                                                                                                                            |
| 4     | Playlistload         | Die Wiedergabeliste wurde gefunden und wird jetzt abgerufen.                                                                                                    |
| 5     | Playlistopening         | Die Wiedergabeliste wurde abgerufen und nun analysiert und geladen.                                                                                        |
| 6     | Playlistopennomedia     | Die Wiedergabeliste ist geöffnet.                                                                                                                                      |
| 7     | Playlistchanged         | **Currentwiedergabe** wurde eine neue Wiedergabeliste zugewiesen.                                                                                               |
| 8     | Mediachanging           | Ein neues Medien Element soll geladen werden.                                                                                                                |
| 9     | Medialocating           | Das Medien Element wird von Windows Media Player gefunden. Die Datei kann lokal oder Remote sein.                                                                      |
| 10    | Mediaconnecting         | Verbindung mit dem Server, der das Medien Element enthält.                                                                                                    |
| 11    | Medialoading            | Das Medien Element wurde gefunden und wird jetzt abgerufen.                                                                                                |
| 12    | Mediaopening            | Das Medien Element wurde abgerufen und wird jetzt geöffnet.                                                                                                 |
| 13    | Mediaopen               | Das Medien Element ist jetzt geöffnet.                                                                                                                                |
| 14    | Begincodecerwerbs   | Die Codec-Übernahme wird gestartet.                                                                                                                            |
| 15    | Endcodecerwerbs     | Die Codec-Erfassung ist fertiggestellt.                                                                                                                         |
| 16    | Beginliceneracquisition | Erwerben einer Lizenz für die Wiedergabe von DRM-geschütztem Inhalt.                                                                                                     |
| 17    | Endliceneracquisition   | Lizenz zum Wiedergeben von DRM-geschütztem Inhalt wurde abgerufen.                                                                                               |
| 18    | Beginindividual alization  | Beginnen Sie mit DRM-Individualisierung.                                                                                                                           |
| 19    | Umdindividualization    | Die DRM-Individualisierung wurde abgeschlossen.                                                                                                              |
| 20    | Mediawaiting            | Es wird auf ein Medien Element gewartet.                                                                                                                                |
| 21    | Openingunknownurl       | Öffnen einer URL mit einem unbekannten Typ.                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten. Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf. Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. OpenStateChange-Ereignis**](player-player-openstatechange.md)
</dt> </dl>

 

 





