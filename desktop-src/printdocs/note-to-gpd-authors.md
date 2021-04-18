---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Hinweis für GPD-Autoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942bd1e8725428ee49bb937f3978622413160476
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106365013"
---
# <a name="note-to-gpd-authors"></a>Hinweis für GPD-Autoren

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Für Autoren von printfunktionalitäten-Dokumenten, die mit GPD-Dateien vertraut sind, haben einige GPD-Schlüsselwörter keine Entsprechungen im printfunktionalitäten-Dokument. In der folgenden Tabelle sind die GPD-Schlüsselwörter ohne printfunktionalitäten-Dokument Äquivalent enthalten, und der Grund dafür ist keine Entsprechung.



| GPD-Schlüsselwort                                                                            | Erklärung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Einschränkungen<br/> \*Invalidkombination<br/> \*Conflictpriority<br/> | Einschränkungen sind nicht im printfunktionalitäten-Dokument definiert, da printfunktionen Clients diese nicht verarbeiten, erzwingen oder auflösen. Diese Aufgaben müssen vom PrintTicket-Anbieter während der PrintTicket-Validierung durchgeführt werden. Unidrv-Plug-Ins können Ihren eigenen PrintTicket-Validierungscode bereitstellen, oder Sie können sich auf Unidrv verlassen, um diese Validierung auszuführen. Im letzteren Fall erzwingt Unidrv alle Einschränkungen, die in der GPD-Datei definiert sind.<br/> Monolithische Treiber müssen ihren eigenen PrintTicket-Validierungscode bereitstellen und ihre eigene Methode zum Ausdrücken und Erzwingen von Einschränkungen bereitstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*Defaultoption<br/>                                                             | Es gibt eine PrintTicket-Methode, die einen standardmäßigen PrintTicket-Wert zurückgibt, der definitionsgemäß alle Standardeinstellungen für die einzelnen Features enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Eine Funktion kann in drei verschiedene Kategorien unterteilt werden:<br/> Eine Funktion, deren Einstellungen in einem PrintTicket definiert sind. Diese Art von Feature wird als "Dokument-Kurzform" bezeichnet, da durch diese Einstellungen direkt festgelegt wird, wie ein Dokument verarbeitet wird.<br/> Eine Funktion, deren Einstellungen physische Geräte Attribute widerspiegeln, die nicht vom Benutzer gesteuert werden, wie z. b. die Menge an Arbeitsspeicher im Gerät oder das vorhanden sein Optionaler Add-ons, wie z. b. Papier-oder duplexern. Diese Art von Feature wird als Geräte Kurznotiz oder Drucker Kurznotiz bezeichnet. Der Status dieses Funktions Typs ist wichtig, da er eine Option einschränken kann, die zu einer Dokument-Kurzform gehört.<br/> Eine Funktion zur Geräte-oder Drucker Kurznotiz kann auch als Drucker Kurznotiz-Feature (UI) oder als automatische Drucker Kurzform kategorisiert werden. Eine UI-druckerkurzfunktion muss auf einer Benutzeroberfläche angezeigt werden, die von einem Administrator festgelegt werden kann. Das Gerät erkennt automatisch eine automatische Drucker Kurznotiz.<br/> |
| \*Wechseln... \* Sollten<br/>                                                         | Ein Print-Funktionen-Anbieter muss eine Methode implementieren, die ein Printworks-Dokument erstellt, das entweder Drucker-oder Dokument persistente Features auflistet, abhängig von dem Typ, der vom Aufrufer angegeben wird. Aus diesem Grund ist es nicht erforderlich, die gleichen Informationen über das printfunktionalitäten-Dokument selbst darzustellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




