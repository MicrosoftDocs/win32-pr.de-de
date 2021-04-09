---
title: Printworks-Konfigurations Abhängigkeit
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7f376d8bd0dab823adb3a2e0665db27508b1d7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869640"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Konfigurations Abhängigkeit im printfunktionalitäten-Schema

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Das printfunktionalitäten-Schema ist in Bezug auf die verwendeten Elemente und die allgemeine Struktur, die von übergeordneten und untergeordneten Elementen ausgedrückt wird, eng mit dem Druck Schema Framework vergleichbar. Konfigurations Abhängigkeiten, die speziell für Print-Funktionen gelten, werden hier als Erweiterung des allgemeinen Frameworks aufgeführt. Konfigurations Abhängigkeiten verweisen auf die Tatsache, dass einige Elemente, einschließlich ihrer Inhalte, geändert oder sogar aus einem printfunktionalitäten-Dokument in das nächste gelöscht werden können, da Abhängigkeiten von der Konfiguration abhängig sind. Selbst wenn ein übergeordnetes Element von der Konfiguration unabhängig sein muss, verfügen seine untergeordneten Elemente möglicherweise über Abhängigkeiten. Solche Abhängigkeiten werden mithilfe von \* Switch/ \* Case-Konstrukten in GPD-Dateien ausgedrückt.

Beachten Sie als Beispiel für eine Konfigurations Abhängigkeit die Werte, die den einzelnen Eigenschaften im printfunktionalitäten-Dokument zugeordnet sind. Jedes Dokument von printfunktionalitäten kann sich in den Eigenschafts Instanzen, die definiert sind, und in den Wert Instanzen unterscheiden, die diesen Eigenschaften Instanzen zugewiesen sind.



| Elementtyp                                                                                                                                                                             | Konfigurations Abhängigkeit                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktion <br/> Option<br/> Parameterinit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Eigenschaft<br/> ScoredProperty<br/> | Diese Elemente dürfen keine Konfigurations Abhängigkeiten aufweisen.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | ParameterDef-Elemente und-Elemente, die in einer beliebigen Schachtelungs Ebene enthalten sind, dürfen keine Konfigurations Abhängigkeiten aufweisen.<br/>                                                                                        |
| Eigenschaft <br/>                                                                                                                                                                     | Eigenschaften Elemente können Konfigurations Abhängigkeiten aufweisen, außer wenn Sie in ParameterDef-Elementen angezeigt werden.<br/>                                                                                                       |
| Wert <br/>                                                                                                                                                                        | Wert Elemente, die in ScoredProperty-Elementen angezeigt werden, dürfen keine Konfigurations Abhängigkeiten aufweisen. Wert Elemente, die in einem Property-Element angezeigt werden, haben möglicherweise beliebige Abhängigkeiten von der Konfiguration.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




