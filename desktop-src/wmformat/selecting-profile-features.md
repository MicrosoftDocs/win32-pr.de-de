---
title: Auswählen von Profil Features
description: Auswählen von Profil Features
ms.assetid: 5e09000d-1417-43aa-9e9c-0aff536d52b7
keywords:
- Profile, Featureauswahl
- Profile, auswählen von Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769b10387bb4fb660c31678b406090cfc7e42743
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337979"
---
# <a name="selecting-profile-features"></a>Auswählen von Profil Features

In der folgenden Tabelle werden die Profil Funktionen aufgelistet, und es wird beschrieben, wann Sie verwendet werden sollen.



| Funktion                            | Verwendung                                                                                                                                                                                                                                                                                                                | Wann nicht zu verwenden                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gegenseitiger Ausschluss nach Bitrate (MBR) | Die Datei wird an eine Zielgruppe mit Verbindungsgeschwindigkeiten gestreamt, die von Benutzer zu Benutzer variieren (z. b. über das Internet bereitgestellte Dateien).                                                                                                                                                                              | Die Datei wird nicht über ein Netzwerk gestreamt. Die Datei wird über ein Netzwerk mit einer konstant zuverlässigen verfügbaren Bandbreite gestreamt (z. b. Dateien, die über ein lokales Unternehmensnetzwerk übermittelt werden).<br/>                                                              |
| Gegenseitiger Ausschluss nach Sprache       | Die Datei enthält Datenströme, die dieselben Daten in verschiedenen Sprachen duplizieren. (Ein Film, der in mehreren Sprachen als Beispiel bezeichnet wird, würde den Sound als sich gegenseitig ausschließende Streams codieren.)                                                                                                                         | Die Datei enthält nur Datenströme in einer einzigen Sprache. Wenn die Datei nur Datenströme enthält, die für einzelne Sprachen geändert werden müssen, kann es einfacher sein, eine neue Datei für jede Sprache zu erstellen (z. b. für einen Trainings Film mit vielen Text im Videostream).<br/> |
| Gegenseitiger Ausschluss durch Präsentation   | Sie möchten Videos in mehr als einem Seitenverhältnis bereitstellen. Eine Datei kann z. b. das gleiche Video enthalten, das für das Fernsehen und das ursprüngliche Bildformat für das Breitbildformat formatiert ist.                                                                                                                                     | Es ist nur eine Version jedes Videodaten Stroms vorhanden.                                                                                                                                                                                                                                    |
| Bandbreiten Freigabe                  | Die Datei wird gestreamt und verfügt über zwei oder mehr Datenströme, die, wenn kombiniert, weniger verfügbare Bandbreite als die Bitraten Werte beider Datenströme verwenden, die zusammen addiert werden. Da es sich bei der Bitrate eines Streams im Wesentlichen um die maximal erforderliche Bandbreite für den Datenstrom handelt, können einige Datenströme einige Zeiträume niedriger Datenübertragungen aufweisen. | Die Datei wird nicht über ein Netzwerk gestreamt. Alle Streams haben konsistente Bitraten.<br/>                                                                                                                                                                                     |
| Streampriorisierung              | Die Datei wird gestreamt, und einige Streams sind wichtiger als andere.                                                                                                                                                                                                                                                 | Die Datei wird nicht über ein Netzwerk gestreamt. Alle Streams sind von gleicher Wichtigkeit.<br/>                                                                                                                                                                                       |
| Dateneinheiten Erweiterungen               | Es gibt wichtige Informationen zu den Beispielen in einem Stream, die mit den Beispielen aufbewahrt werden müssen.                                                                                                                                                                                                                      | Die Datei ist für die Übermittlung über eine eingeschränkte Bandbreite vorgesehen. In diesem Fall kann für Dateneinheiten Erweiterungen zu viel mehr Aufwand verwendet werden.                                                                                                                                                    |



 

Es ist auch wichtig, die Codec-Features zu beachten, die Sie beim Erstellen eines Profils mit der Datei verwenden möchten. Weitere Informationen finden Sie unter [Codec-Features](codec-features.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Entwerfen von Profilen**](designing-profiles.md)
</dt> </dl>

 

 





