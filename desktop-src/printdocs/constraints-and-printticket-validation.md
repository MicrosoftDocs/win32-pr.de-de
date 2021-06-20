---
description: Um Einschränkungskonflikte zu vermeiden, müssen PrintTicket-Anbieter die Validierung unterstützen, die Clients verwenden, um die Validierung für ihr PrintTicket durchzuführen.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Einschränkungen und PrintTicket-Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08abc07f0ef96e94720f8f9431a192e5dbcac669
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409573"
---
# <a name="constraints-and-printticket-validation"></a>Einschränkungen und PrintTicket-Überprüfung

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Wie im Abschnitt PrintCapabilities-Schema erläutert, sind einige der möglichen Konfigurationsergebnisse, die in einem PrintCapabilities-Dokument ausgedrückt werden, für das Gerät ungültig. Konfigurationen, die ungültig sind, enthalten Einschränkungskonflikte (ein Begriff, der in der Welt von PPD-/GPD-Dateien verwendet wird). Um Einschränkungskonflikte zu vermeiden, müssen PrintTicket-Anbieter einen PrintTicket-Überprüfungsvorgang unterstützen, den Clients verwenden, um die Validierung für ihr PrintTicket durchzuführen. Dieser Vorgang sollte erkennen, ob die angegebene Konfiguration auf dem Gerät erfolgen kann. Wenn die Konfiguration nicht erfolgen kann (da die angegebenen Feature- und Option-Elemente auf dem aktuellen Gerät nicht vorhanden sind oder weil die Konfiguration eingeschränkt ist), sollte der Vorgang die Eingabe PrintTicket so ändern, dass sie gültige, constrained-Einstellungen enthält. Der Vorgang kann auch andere Informationen im PrintTicket entfernen oder überprüfen. Beachten Sie, dass beim Auftreten eines Einschränkungskonflikts der Validierungscode die Einstellung eines der Geräteattribute ändern muss, um den Einschränkungskonflikt zu vermeiden. [Optionsdefinitionen](option-definitions.md) deuten darauf hin, dass ein vom Gerätetreiber definierter Bewertungsprozess verwendet werden sollte, um zu bestimmen, welches Geräteattribut geändert werden soll, um die ursprüngliche Absicht des Benutzers optimal zu erhalten. Der Validierungscode kann den Bewertungsprozess hartcodieren, um ein Geräteattribut gegenüber einem anderen zu bevorzugen, oder er verwendet informationen, die von einer bestimmten Property-Instanz im PrintTicket bereitgestellt werden, um die Auflösung zu unterstützen. Da in den Druckschemaschlüsselwörtern keine Eigenschaft definiert ist, mit der Clients die relative Priorität jedes Geräteattributs angeben können, werden alle privaten PrintTicket Property-Elemente, die für diesen Zweck verwendet werden, wahrscheinlich von anderen PrintTicket-Anbietern ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



