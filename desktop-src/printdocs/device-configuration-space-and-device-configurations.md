---
title: Gerätekonfigurationsbereich
description: Der Konfigurationsraum eines Geräts ist der Satz aller möglichen Werte, die allen Attributen des Geräts zugewiesen werden können.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4871da3695e81168d43504456c357b0cf566b7f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409483"
---
# <a name="device-configuration-space-and-device-configurations"></a>Gerätekonfigurationsbereich und Gerätekonfigurationen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Der *Konfigurationsraum* eines Geräts ist der Satz aller möglichen Werte, die allen Attributen des Geräts zugewiesen werden können. Die beiden wichtigsten Gründe für die Beschreibung des Konfigurationsraums des Geräts in printCapabilities lauten wie folgt.

1.  Die Informationen tragen erheblich zu einem besseren Verständnis der Funktionen des Geräts bei. Diese Informationen erleichtern es einem Client der PrintCapabilities, Benutzeroberflächenelemente zu generieren, was es dem Endbenutzer erleichtert, eine bestimmte Konfiguration zum Verarbeiten eines Auftrags auszuwählen. Indem mehr Details zu den Funktionen des Geräts für die Anwendung und letztendlich für den Endbenutzer zur Verfügung gestellt werden, kann die Druckabsicht des Benutzers effektiver erfüllt werden.

2.  Bestimmte Geräteeigenschaften, die in PrintCapabilities angezeigt werden, sind möglicherweise von der vom Client ausgewählten Konfiguration abhängig.

Einige Informationen sollten nicht in printCapabilities integriert werden. Dies schließt Informationen ein, die sich nicht auf die Art und Weise auswirken, wie ein Auftrag erstellt wird, keine Einschränkungen für die Erstellung eines Auftrags aufweist oder sich anderweitig auf die Geräteeigenschaften auswirkt. Beispielsweise kann ein Gerät Statusinformationen melden, z. B. den Satz von Aufträgen, die auf die Verarbeitung warten. Diese Informationen haben keine Auswirkungen auf die Informationen, die zum Formatieren des Auftrags erforderlich sind, und geben auch keinen Hinweis auf die auf dem Gerät verfügbaren Funktionen. Aus diesem Grund muss diese Art von Informationen nicht in printCapabilities vorhanden sein.

## <a name="device-constraints"></a>Geräteeinschränkungen

Viele Geräte unterstützen aufgrund einer Einschränkung auf dem Gerät nicht alle möglichen Konfigurationen im Konfigurationsbereich. Beispielsweise kann ein Gerät von der Durchführung von Duplexdruck auf transparenten Medien eingeschränkt werden. Eine Einschränkung kann eine physische Einschränkung darstellen: Einige Medientypen sind einfach zu fest, um bestimmte Papierpfade im Gerät zu durchlaufen, und können daher nicht in einigen Eingabeslots platziert oder an einige Ausgabebehälter weitergeleitet werden. Derzeit liegt es in der Verantwortung des PrintCapabilities- oder PrintTicket-Anbieters, die durch die Eingabe PrintTicket dargestellte Konfiguration zu überprüfen, um sicherzustellen, dass sie keine ungültige Konfiguration darstellt. Wenn die Konfiguration ungültig ist, sollte der PrintCapabilities- oder PrintTicket-Anbieter die Konfiguration so ändern, dass sie gültig wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



