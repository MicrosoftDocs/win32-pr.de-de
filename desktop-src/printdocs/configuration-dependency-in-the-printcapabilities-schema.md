---
title: PrintCapabilities-Konfigurationsabhängigkeit
description: Konfigurationsabhängigkeiten beziehen sich auf die Tatsache, dass einige Elemente von einem PrintCapabilities-Dokument zum nächsten geändert oder sogar gelöscht werden können.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20f01c8e7bd9a036a53048996ec5a38246471f67
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409663"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Konfigurationsabhängigkeit im PrintCapabilities-Schema

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das PrintCapabilities-Schema ist hinsichtlich der verwendeten Elemente und der allgemeinen Struktur, die von übergeordneten und untergeordneten Elementen ausgedrückt wird, eng parallel zum Druckschemaframework. Konfigurationsabhängigkeiten, die sich speziell auf printCapabilities beziehen, werden hier als Erweiterung für das allgemeine Framework aufgeführt. Konfigurationsabhängigkeiten beziehen sich darauf, dass einige Elemente, einschließlich ihrer Inhalte, aufgrund von Abhängigkeiten von der Konfiguration von einem PrintCapabilities-Dokument zum nächsten geändert oder sogar gelöscht werden können. Selbst wenn ein übergeordnetes Element unabhängig von der Konfiguration sein muss, können seine untergeordneten Elemente Abhängigkeiten aufweisen. Solche Abhängigkeiten werden mithilfe von \* \* Switch/Case-Konstrukten in GPD-Dateien ausgedrückt.

Betrachten Sie als Beispiel für eine Konfigurationsabhängigkeit die Werte, die den einzelnen Eigenschaften im PrintCapabilities-Dokument zugeordnet sind. Jedes PrintCapabilities-Dokument kann sich in den definierten Eigenschafteninstanzen und in den Wertinstanzen unterscheiden, die diesen Eigenschafteninstanzen zugewiesen sind.



| Elementtyp                                                                                                                                                                             | Konfigurationsabhängigkeit                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktion <br/> Option<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Eigenschaft<br/> ScoredProperty<br/> | Diese Elemente dürfen keine Konfigurationsabhängigkeiten aufweisen.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | ParameterDef-Elemente und darin enthaltene Elemente auf einer beliebigen Schachtelungsebene dürfen keine Konfigurationsabhängigkeiten aufweisen.<br/>                                                                                        |
| Eigenschaft <br/>                                                                                                                                                                     | Eigenschaftselemente können Konfigurationsabhängigkeiten aufweisen, es sei denn, sie werden in ParameterDef-Elementen angezeigt.<br/>                                                                                                       |
| Wert <br/>                                                                                                                                                                        | Wertelemente, die in ScoredProperty-Elementen angezeigt werden, dürfen keine Konfigurationsabhängigkeiten aufweisen. Wertelemente, die in einem Property-Element angezeigt werden, können beliebige Abhängigkeiten von der Konfiguration aufweisen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




