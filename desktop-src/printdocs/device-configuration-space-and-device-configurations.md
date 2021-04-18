---
title: Geräte Konfigurationsbereich
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e12b6480675dba6e735390f4820a8782edc5c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366379"
---
# <a name="device-configuration-space-and-device-configurations"></a>Geräte Konfigurationsbereich und Geräte Konfigurationen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Der *Konfigurationsbereich* eines Geräts ist der Satz aller möglichen Werte, die allen Attributen des Geräts zugewiesen werden können. Die zwei wichtigsten Gründe, den Konfigurationsbereich des Geräts in den Print-Funktionen zu beschreiben, sind wie folgt.

1.  Die Informationen tragen wesentlich zu einem besseren Verständnis der Gerätefunktionen bei. Diese Informationen erleichtern es einem Client der printfunktionen, Benutzeroberflächen Elemente (UI) zu generieren, was es dem Endbenutzer erleichtert, eine bestimmte Konfiguration zum Verarbeiten eines Auftrags auszuwählen. Durch die Bereitstellung ausführlichere Informationen zu den Funktionen des Geräts für die Anwendung und letztendlich zum Endbenutzer kann die Druck Absicht des Benutzers effektiver erfüllt werden.

2.  Bestimmte Geräteeigenschaften, die in den Print-Funktionen angezeigt werden, sind möglicherweise von der jeweiligen Konfiguration abhängig, die vom Client ausgewählt wird.

Einige Informationen sollten nicht in die Print-Funktionen eingebunden werden. Dies umfasst Informationen, die sich nicht auf die Art und Weise auswirken, wie ein Auftrag erstellt wird, keine Einschränkungen der Art und Weise der Erstellung eines Auftrags auferlegt und die Geräteeigenschaften anderweitig nicht beeinträchtigt werden. Ein Gerät kann z. b. Statusinformationen melden, z. b. den Satz von Aufträgen, die auf die Verarbeitung warten. Diese Informationen wirken sich nicht auf die Informationen aus, die zum Formatieren des Auftrags erforderlich sind, und es gibt auch keine Hinweise auf die auf dem Gerät verfügbaren Funktionen. Aus diesem Grund muss diese Art von Informationen nicht in den Print-Funktionen vorhanden sein.

## <a name="device-constraints"></a>Geräte Einschränkungen

Viele Geräte unterstützen nicht alle möglichen Konfigurationen im Konfigurationsbereich aufgrund einer Einschränkung auf dem Gerät. Ein Gerät kann z. b. von der Durchführung des Duplex Drucks auf transparenten Medien eingeschränkt werden. Eine Einschränkung kann eine physische Einschränkung darstellen: einige Medientypen sind einfach zu starr, um bestimmte Papier Pfade im Gerät zu durchlaufen, und können daher nicht in einigen Eingabe Slots abgelegt oder an einige Ausgabebehälter weitergeleitet werden. Derzeit liegt es in der Verantwortung des Print-oder PrintTicket-Anbieters, die Konfiguration zu überprüfen, die durch die Print Ticket-Eingabe dargestellt wird, um sicherzustellen, dass Sie keine ungültige Konfiguration darstellt. Wenn die Konfiguration ungültig ist, sollte der printfunktionen-oder PrintTicket-Anbieter die Konfiguration so ändern, dass Sie gültig wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



