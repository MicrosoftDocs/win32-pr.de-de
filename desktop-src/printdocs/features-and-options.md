---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Features und Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866cead02021b8d933ca03483e77de832d8d094a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106361135"
---
# <a name="features-and-options"></a>Features und Optionen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Funktions-/Options-und Parameterkonstrukte werden in einem printfunktionalitäten-Dokument verwendet, um Geräte Attribute darzustellen, die zur Definition der Gerätekonfiguration beitragen. Ein Beispiel für ein Funktions-/optionskonstrukt ist ein Druck Gerät, das in mehreren Auflösungen Druck fähig ist. Das Device-Attribut, das die Auflösung definiert, kann als Funktions Instanz dargestellt werden, wobei jeder der möglichen Ausgabe Auflösungswerte als einzelne Options Instanz dargestellt wird. Eine Options Instanz kann eine Auflösung von 300 dpi darstellen, eine andere kann eine Auflösung von 600 dpi darstellen usw.

Beachten Sie, dass das Druck Schema erfordert, dass die Liste der Funktionen, Optionen und ParameterDef-Instanzen, die in den einzelnen Printworks-Dokumenten gemeldet werden, unabhängig von der Konfiguration konstant bleiben muss. Dadurch können Konfigurationen und Abhängigkeiten von Konfigurationen auf eindeutige Weise ausgedrückt werden. Diese Anforderung impliziert, dass jede Funktion und Unterfunktion über eine klar definierte Einstellung verfügen muss, unabhängig von der Einstellung anderer Features oder unter Funktionen. Daher muss jede Unterfunktion über eine Option verfügen, die einer No-op-Einstellung (Off, deaktiviert oder None) entspricht, die automatisch für alle unter Features ausgewählt wird, wenn der Benutzer die Option Nein-op in der übergeordneten Funktion auswählt. Wenn eine der unter Funktionen auf eine aktivierte Option festgelegt ist, werden die übergeordnete Funktion und andere zugehörige unter Funktionen ebenfalls aktiviert. In der Zwischenzeit muss der PrintTicket-Anbieter sicherstellen, dass die Einstellungen für alle Funktions-und unter Funktions Instanzen unabhängig von der Gerätekonfiguration definiert werden und dass die Einstellungen der untergeordneten Funktion mit den Einstellungen der übergeordneten Funktion konsistent sind. Dadurch wird sichergestellt, dass dem Gerät kein inkonsistentes PrintTicket zugewiesen ist, in dem einige unter Features angeben, dass beispielsweise das Heften aktiviert ist, andere unter Features jedoch, dass das Heften deaktiviert ist.

Beachten Sie, dass printfunktionsautoren die Schachtelungs Funktionen von Funktions Elementen nicht verwenden müssen. Wenn Sie dies bevorzugen, können Sie alle Funktions Instanzen in einer flachen Struktur als gleich geordnete Elemente darstellen. Beachten Sie auch, dass eine Auflistung von featureinstanzen vereinfacht werden kann, indem alle unter Features auf die Stamm Ebene verschoben werden. Die einzige Vorsichtsmaßnahme besteht darin, sicherzustellen, dass die namens Attribute dieser Funktions Instanzen eindeutig sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



