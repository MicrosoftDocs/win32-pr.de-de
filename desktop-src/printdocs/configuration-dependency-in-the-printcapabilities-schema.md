---
title: PrintCapabilities-Konfigurationsabhängigkeit
description: Konfigurationsabhängigkeiten beziehen sich auf die Tatsache, dass einige Elemente von einem PrintCapabilities-Dokument zum nächsten geändert oder sogar gelöscht werden können.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56e05e7b41ecfacf26556cdc7c38fa00087b440e92b476b2d6121f7ee082574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950460"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Konfigurationsabhängigkeit im PrintCapabilities-Schema

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das PrintCapabilities-Schema ist hinsichtlich der verwendeten Elemente und der allgemeinen Struktur, die von übergeordneten und untergeordneten Elementen ausgedrückt wird, eng mit dem Druckschemaframework parallel. Konfigurationsabhängigkeiten, die speziell für PrintCapabilities gelten, werden hier als Erweiterung des allgemeinen Frameworks aufgeführt. Konfigurationsabhängigkeiten beziehen sich auf die Tatsache, dass einige Elemente, einschließlich ihrer Inhalte, geändert oder sogar von einem PrintCapabilities-Dokument zum nächsten gelöscht werden können, als Folge von Abhängigkeiten von der Konfiguration. Auch wenn ein übergeordnetes Element unabhängig von der Konfiguration sein muss, können seine untergeordneten Elemente Abhängigkeiten aufweisen. Solche Abhängigkeiten werden mit \* \* switch/case-Konstrukten in GPD-Dateien ausgedrückt.

Betrachten Sie als Beispiel für eine Konfigurationsabhängigkeit die Werte, die den einzelnen Eigenschaften im PrintCapabilities-Dokument zugeordnet sind. Jedes PrintCapabilities-Dokument kann sich in den property -Instanzen unterscheiden, die definiert sind, und in den Value-Instanzen, die diesen Property-Instanzen zugewiesen sind.



| Elementtyp                                                                                                                                                                             | Konfigurationsabhängigkeit                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Komponente <br/> Option<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Eigenschaft<br/> ScoredProperty<br/> | Diese Elemente dürfen keine Konfigurationsabhängigkeiten aufweisen.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | ParameterDef-Elemente und darin enthaltene Elemente auf einer Schachtelungsebene dürfen keine Konfigurationsabhängigkeiten aufweisen.<br/>                                                                                        |
| Eigenschaft <br/>                                                                                                                                                                     | Eigenschaftselemente können Konfigurationsabhängigkeiten aufweisen, es sei denn, sie werden in ParameterDef-Elementen angezeigt.<br/>                                                                                                       |
| Wert <br/>                                                                                                                                                                        | Wertelemente, die in ScoredProperty-Elementen angezeigt werden, dürfen keine Konfigurationsabhängigkeiten aufweisen. Wertelemente, die innerhalb eines Property-Elements angezeigt werden, können beliebige Abhängigkeiten von der Konfiguration aufweisen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




