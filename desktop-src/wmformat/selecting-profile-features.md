---
title: Auswählen von Profilfeatures
description: Auswählen von Profilfeatures
ms.assetid: 5e09000d-1417-43aa-9e9c-0aff536d52b7
keywords:
- Profile, Funktionsauswahl
- Profile, Auswählen von Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573e234d9e8e35d8d15f4e658b2a0657c43998181c1cf4b5873a205f5833b8cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654192"
---
# <a name="selecting-profile-features"></a>Auswählen von Profilfeatures

In der folgenden Tabelle werden die Profilfeatures aufgelistet und beschrieben, wann Sie sie verwenden möchten oder nicht.



| Feature                            | Verwendung                                                                                                                                                                                                                                                                                                                | Ungeeignete Fälle für                                                                                                                                                                                                                                                                     |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gegenseitiger Ausschluss nach Bitrate (MBR) | Die Datei wird an eine Zielgruppe mit Verbindungsgeschwindigkeiten gestreamt, die von Benutzer zu Benutzer variieren (z. B. Dateien, die über das Internet übermittelt werden).                                                                                                                                                                              | Die Datei wird nicht über ein Netzwerk gestreamt. Die Datei wird über ein Netzwerk mit einer konsistent zuverlässigen verfügbaren Bandbreite gestreamt (z. B. Dateien, die über ein lokales Unternehmensnetzwerk übermittelt werden).<br/>                                                              |
| Gegenseitiger Ausschluss nach Sprache       | Die Datei enthält Streams, die die gleichen Daten in verschiedenen Sprachen duplizieren. (Für einen Film, der in mehreren Sprachen veröffentlicht wurde, wäre das Buch beispielsweise als sich gegenseitig ausschließende Streams codiert.)                                                                                                                         | Die Datei enthält nur Datenströme in einer einzigen Sprache. Wenn die Datei nur Datenströme enthält, die für einzelne Sprachen geändert werden müssen, ist es möglicherweise einfacher, eine neue Datei für jede Sprache zu erstellen (z. B. für einen Trainingsvideo mit viel Text im Videostream).<br/> |
| Gegenseitiger Ausschluss nach Präsentation   | Sie möchten Videos in mehr als einem Seitenverhältnis bereitstellen. Eine Datei kann z. B. das gleiche Video enthalten, das für Fernsehsendungen und für das ursprüngliche Breitbildformat formatiert ist.                                                                                                                                     | Es gibt nur eine Version jedes Videostreams.                                                                                                                                                                                                                                    |
| Bandbreitenfreigabe                  | Die Datei wird gestreamt und verfügt über zwei oder mehr Datenströme, die in Kombination weniger verfügbare Bandbreite als die Bitratenwerte beider datenströme verwenden, die zusammen addiert werden. Da die Bitrate eines Datenstroms im Wesentlichen die maximal erforderliche Bandbreite für den Datenstrom ist, weisen einige Datenströme möglicherweise einige Zeiträume mit geringerer Datenübertragung auf. | Die Datei wird nicht über ein Netzwerk gestreamt. Alle Datenströme weisen konsistente Bitraten auf.<br/>                                                                                                                                                                                     |
| Streampriorisierung              | Die Datei wird gestreamt, und einige Streams sind wichtiger als andere.                                                                                                                                                                                                                                                 | Die Datei wird nicht über ein Netzwerk gestreamt. Alle Streams sind von gleicher Wichtigkeit.<br/>                                                                                                                                                                                       |
| Dateneinheitenerweiterungen               | Es gibt wichtige Informationen im Zusammenhang mit den Stichproben in einem Stream, die mit den Stichproben aufbewahrt werden müssen.                                                                                                                                                                                                                      | Die Datei ist für die Übermittlung über eine eingeschränkte Bandbreite vorgesehen. In diesem Fall können Dateneinheiterweiterungen zu viel Aufwand verbrauchen.                                                                                                                                                    |



 

Es ist auch wichtig, die Codecfunktionen zu berücksichtigen, die Sie beim Erstellen eines Profils mit Ihrer Datei verwenden möchten. Weitere Informationen finden Sie unter [Codecfunktionen.](codec-features.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Entwerfen von Profilen**](designing-profiles.md)
</dt> </dl>

 

 





