---
description: Überprüfen Sie GPD-Schlüsselwörter ohne PrintCapabilities-Dokumententsprechungen. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Hinweis für GPD-Autoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fe9d0c4ce36cf603d492688f4faa426e3050b9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119815"
---
# <a name="note-to-gpd-authors"></a>Hinweis für GPD-Autoren

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Für Autoren von PrintCapabilities-Dokumenten, die mit GPD-Dateien vertraut sind, weisen einige GPD-Schlüsselwörter keine Entsprechungen im PrintCapabilities-Dokument auf. Die folgende Tabelle enthält die GPD-Schlüsselwörter ohne eine PrintCapabilities-Dokumententsprechung und den Grund, warum es keine Entsprechung gibt.



| GPD-Schlüsselwort                                                                            | Erklärung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Einschränkungen<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | Einschränkungen werden im PrintCapabilities-Dokument nicht definiert, da von PrintCapabilities-Clients nicht erwartet wird, dass sie verarbeitet, erzwungen oder aufgelöst werden. Diese Aufgaben müssen während der PrintTicket-Überprüfung vom PrintTicket-Anbieter ausgeführt werden. Unidrv-Plug-Ins können einen eigenen PrintTicket-Validierungscode bereitstellen oder unidrv verwenden, um diese Überprüfung durchzuführen. Im letzteren Fall erzwingt Unidrv alle in der GPD-Datei definierten Einschränkungen.<br/> Monolithische Treiber müssen ihren eigenen PrintTicket-Validierungscode und eine eigene Methode zum Ausdrücken und Erzwingen von Einschränkungen bereitstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*DefaultOption<br/>                                                             | Es gibt eine PrintTicket-Methode, die ein Standard-PrintTicket zurückgibt, das definitionsgemäß über alle Standardeinstellungen für jedes Feature verfügt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Ein Feature kann in drei verschiedene Kategorien unterteilt werden:<br/> Ein Feature, dessen Einstellungen in einem PrintTicket definiert sind. Diese Art von Feature wird als dokumentaufbetont bezeichnet, da diese Einstellungen direkt bestimmen, wie ein Dokument verarbeitet wird.<br/> Ein Feature, dessen Einstellungen physische Geräteattribute widerspiegeln, die nicht vom Benutzer gesteuert werden, z. B. die Menge an Arbeitsspeicher auf dem Gerät, oder die auf das Vorhandensein optionaler Add-Ons wie Papierfeeder oder Duplexer hinweisen. Diese Art von Feature wird als "Geräte-sticky" oder "printer-sticky" bezeichnet. Der Status dieser Art von Feature ist wichtig, da er eine Option einschränken kann, die zu einem Dokument-Sticky-Feature gehört.<br/> Ein feature-sticky- oder printer-sticky-Feature kann weiter kategorisiert werden, entweder als Benutzeroberfläche (UI) printer-sticky Feature oder auto printer-sticky Feature. Ein Benutzeroberflächendrucker-Sticky-Feature muss auf einer Benutzeroberfläche angezeigt werden, die ein Administrator festlegen kann. Das Gerät erkennt automatisch ein automatisches Drucker-Sticky-Feature.<br/> |
| \*Switch ... \* Fall<br/>                                                         | Ein PrintCapabilities-Anbieter muss eine Methode implementieren, mit der ein PrintCapabilities-Dokument erstellt wird, das abhängig vom vom Aufrufer angegebenen Typ entweder "printer-sticky" oder "document-sticky Features" aufzählt. Aus diesem Grund ist es nicht erforderlich, die gleichen Informationen über das PrintCapabilities-Dokument selbst darzustellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




