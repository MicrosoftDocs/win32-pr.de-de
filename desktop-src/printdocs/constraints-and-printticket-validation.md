---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Einschränkungen und PrintTicket-Validierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddcc1f6f3ad496b6bfb6ed201cf93c2b4a10679
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961244"
---
# <a name="constraints-and-printticket-validation"></a>Einschränkungen und PrintTicket-Validierung

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Wie im Abschnitt "printfunktionalitäten Schema" erläutert, sind einige der möglichen Konfigurations Ergebnisse, die in einem printfunktionalitäten-Dokument ausgedrückt werden, für das Gerät ungültig. Ungültige Konfigurationen enthalten Einschränkungs Konflikte (einen Begriff, der in der Welt von PPD/GPD-Dateien verwendet wird). Um Einschränkungs Konflikte zu vermeiden, müssen PrintTicket-Anbieter einen PrintTicket-Überprüfungs Vorgang unterstützen, den Clients zum Durchführen der Validierung Ihres Print Ticket verwenden. Mit diesem Vorgang sollte erkannt werden, ob die angegebene Konfiguration auf dem Gerät erfolgen kann. Wenn die Konfiguration nicht ausgeführt werden kann (weil die angegebenen Funktions-und Options Elemente im aktuellen Gerät nicht vorhanden sind oder die Konfiguration eingeschränkt ist), sollte der Vorgang das PrintTicket-Eingabe Element so ändern, dass es gültige, nicht eingeschränkte Einstellungen enthält. Der Vorgang kann auch andere Informationen im PrintTicket entfernen oder überprüfen. Beachten Sie Folgendes: Wenn ein Einschränkungs Konflikt auftritt, muss der Validierungscode die Einstellung eines der Geräte Attribute ändern, um den Einschränkungs Konflikt zu vermeiden. Mit [options Definitionen](option-definitions.md) wird vorgeschlagen, dass ein Gerätetreiber definierter Bewertungsprozess verwendet werden soll, um zu bestimmen, welches Geräte Attribut geändert werden soll, um die ursprüngliche Absicht des Benutzers am besten zu erhalten. Der Validierungscode kann den Bewertungsprozess hart codieren, um ein Geräte Attribut für ein anderes zu bevorzugen, oder es kann Informationen verwenden, die von einer bestimmten Eigenschaften Instanz im PrintTicket bereitgestellt werden, um die Auflösung zu steuern. Da in den Druck Schema Schlüsselwörtern keine Eigenschaft definiert ist, die es Clients ermöglicht, die relative Priorität der einzelnen Geräte Attribute anzugeben, werden alle privaten PrintTicket-Eigenschafts Elemente, die für diesen Zweck verwendet werden, wahrscheinlich von anderen PrintTicket-Anbietern ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



