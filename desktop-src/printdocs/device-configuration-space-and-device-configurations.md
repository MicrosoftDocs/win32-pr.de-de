---
title: Gerätekonfigurationsraum
description: Der Konfigurationsraum eines Geräts ist der Satz aller möglichen Werte, die allen Attributen des Geräts zugewiesen werden können.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09eabf7c84e1990e0aaf6b2d9fab1d9043f788fef32c3863a71d9ca1e6b61a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092114"
---
# <a name="device-configuration-space-and-device-configurations"></a>Gerätekonfigurationsraum und Gerätekonfigurationen

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Der Konfigurationsraum *eines Geräts* ist der Satz aller möglichen Werte, die allen Attributen des Geräts zugewiesen werden können. Die beiden wichtigsten Gründe für die Beschreibung des Konfigurationsraums des Geräts in PrintCapabilities sind die folgenden.

1.  Die Informationen tragen erheblich zu einem besseren Verständnis der Funktionen des Geräts bei. Diese Informationen erleichtern es einem Client von PrintCapabilities, Benutzeroberflächenelemente zu generieren. Dadurch kann der Endbenutzer eine bestimmte Konfiguration einfacher auswählen, um einen Auftrag zu verarbeiten. Durch die Bereitstellung von mehr Details zu den Funktionen des Geräts für die Anwendung und letztendlich für den Endbenutzer kann die Druckabsicht des Benutzers effektiver erfüllt werden.

2.  Bestimmte Geräteeigenschaften, die in PrintCapabilities dargestellt werden, sind möglicherweise von der vom Client ausgewählten Konfiguration abhängig.

Einige Informationen sollten nicht in PrintCapabilities integriert werden. Dies schließt Informationen ein, die sich nicht auf die Art und Weise auswirken, wie ein Auftrag erstellt wird, keine Einschränkungen für die Art und Weise, wie ein Auftrag erstellt wird, oder anderweitig die Geräteeigenschaften beeinflussen. Beispielsweise kann ein Gerät Statusinformationen melden, z. B. die Gruppe von Aufträgen, die auf die Verarbeitung warten. Diese Informationen wirken sich weder auf die Informationen aus, die zum Formatieren des Auftrags erforderlich sind, noch geben sie Aufschluss über die auf dem Gerät verfügbaren Funktionen. Aus diesem Grund muss diese Art von Informationen nicht in printCapabilities vorhanden sein.

## <a name="device-constraints"></a>Geräteeinschränkungen

Viele Geräte unterstützen aufgrund einer Einschränkung auf dem Gerät nicht alle möglichen Konfigurationen im Konfigurationsbereich. Beispielsweise kann ein Gerät davon eingeschränkt werden, Duplexdruck auf transparenten Medien zu verwenden. Eine Einschränkung kann eine physische Einschränkung darstellen: Einige Medientypen sind einfach zu starr, um bestimmte Papierpfade auf dem Gerät zu verlassen. Daher können sie nicht in einigen Eingabeslots platziert oder an einige Ausgabebehälter geroutet werden. Derzeit liegt es in der Verantwortung des PrintCapabilities- oder PrintTicket-Anbieters, die konfiguration zu überprüfen, die durch die Eingabe PrintTicket dargestellt wird, um sicherzustellen, dass es keine ungültige Konfiguration repräsentiert. Wenn die Konfiguration ungültig ist, sollte der PrintCapabilities- oder PrintTicket-Anbieter die Konfiguration so ändern, dass sie gültig wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



