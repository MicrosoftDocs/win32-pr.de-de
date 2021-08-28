---
description: Um Einschränkungskonflikte zu vermeiden, müssen PrintTicket-Anbieter die Validierung unterstützen, die Von Clients zum Durchführen der Validierung für ihr PrintTicket verwendet wird.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Einschränkungen und PrintTicket-Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b973373ca98e25d3a167ff28ab433d6e61821de3be822d0e9a8699a025d71f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939130"
---
# <a name="constraints-and-printticket-validation"></a>Einschränkungen und PrintTicket-Überprüfung

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Wie im Abschnitt PrintCapabilities-Schema erläutert, sind einige der möglichen Konfigurationsergebnisse, die in einem PrintCapabilities-Dokument ausgedrückt werden, für das Gerät ungültig. Ungültige Konfigurationen werden als Einschränkungskonflikte bezeichnet (ein Begriff, der in der Welt der PPD-/GPD-Dateien verwendet wird). Um Einschränkungskonflikte zu vermeiden, müssen PrintTicket-Anbieter einen PrintTicket-Validierungsvorgang unterstützen, den Clients zum Durchführen der Überprüfung auf ihrem PrintTicket verwenden. Dieser Vorgang sollte erkennen, ob die angegebene Konfiguration auf dem Gerät auftreten kann. Wenn die Konfiguration nicht ausgeführt werden kann (weil die angegebenen Elemente Feature und Option auf dem aktuellen Gerät nicht vorhanden sind oder weil die Konfiguration eingeschränkt ist), sollte der Vorgang die Eingabe PrintTicket so ändern, dass sie gültige, nicht eingeschränkte Einstellungen enthält. Der Vorgang kann auch andere Informationen im PrintTicket entfernen oder überprüfen. Beachten Sie, dass beim Auftreten eines Einschränkungskonflikts der Validierungscode die Einstellung eines der Geräteattribute ändern muss, um den Einschränkungskonflikt zu vermeiden. [Optionsdefinitionen](option-definitions.md) schlagen vor, dass ein vom Gerätetreiber definierter Bewertungsprozess verwendet werden soll, um zu bestimmen, welches Geräteattribut geändert werden soll, um die ursprüngliche Absicht des Benutzers am besten beizubehalten. Der Validierungscode kann den Bewertungsprozess hartcodieren, um ein Geräteattribut gegenüber einem anderen zu bevorzugen, oder er verwendet Informationen, die von einer bestimmten Eigenschaftsinstanz im PrintTicket bereitgestellt werden, um die Auflösung zu steuern. Da in den Schlüsselwörtern für das Druckschema keine Eigenschaft definiert ist, mit der Clients die relative Priorität jedes Geräteattributs angeben können, werden alle privaten PrintTicket Property-Elemente, die für diesen Zweck verwendet werden, wahrscheinlich von anderen PrintTicket-Anbietern ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



