---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Erstellen eines Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31644f25f231f7121e2e492bc3f41a81b82d0b4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354929"
---
# <a name="creating-a-device-specific-printticket"></a>Erstellen eines Device-Specific PrintTicket

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein Geräte spezifisches PrintTicket hat ein bestimmtes Gerät als Ziel und ist daher nicht auf mehreren Geräten portabel.

Die in der folgenden Liste aufgeführten Schritte sollten verwendet werden, wenn Sie ein Geräte spezifisches Print Ticket erstellen.

1.  Abrufen eines printfunktionalitäten-Dokuments, das nur die relevanten Funktions Instanzen für das Gerät enthält. Fordern Sie ein Standarddokument von printfunktionen an. Hierfür ist es nicht erforderlich, dass Sie ein Print Ticket-Eingabe Element angeben, da die Geräte Attribute (Funktions-und Options Instanzen und-Parameter), die zum Erstellen von PrintTicket verwendet werden, unabhängig von der Konfiguration sind.

2.  Erstellen Sie ein leeres XML-Dokument, das den PrintTicket-Stamm enthält. Weisen Sie dem Druckschema-Namespace ein Namespace Präfix zu, und weisen Sie Präfixe für alle anderen Namespaces zu, die von PrintTicket verwendet werden. Geben Sie die PrintTicket-Schema Version an.

3.  Sie können Einstellungen im PrintTicket für alle Features und ParameterDef-Instanzen definieren, die im Dokument "printfunktionalitäten" oder nur für Sie von Interesse sind. Wenn der PrintTicket-Schnittstelle ein "PrintTicket"-Teil angezeigt wird, werden standardmäßig bei der PrintTicket-Validierung automatisch die ausgelassene Funktion und ParameterDef-Instanzen bereitgestellt

4.  Überprüfen Sie das printfunktionsdokument auf Funktions Instanzen, und legen Sie fest, welche von Ihnen in PrintTicket definiert werden sollen. Fügen Sie diese featureinstanzen zu PrintTicket hinzu, übertragen Sie den Inhalt der Funktions Instanzen jedoch nicht an Ihr PrintTicket. Wenn Sie eine untergeordnete Funktion übertragen, muss die übergeordnete Funktion ebenfalls übertragen werden, und die über-/Unterordnungsbeziehung muss in PrintTicket beibehalten werden.

    Legen Sie für jede zu übertragenden Funktion fest, welche Options Instanzen auf Ihr Print Ticket anwendbar sind. Übertragen Sie die gesamte Option, wie im Dokument printfunktionalitäten definiert, und entfernen Sie dann alle vorhandenen Eigenschaften Instanzen. Die Eigenschaften Instanzen werden in printfunktionen-Dokumenten verwendet, dienen jedoch nicht in PrintTicket. Behalten Sie alle ScoredProperty-Instanzen bei, und stellen Sie sicher, dass Sie Ihre Position beibehalten. Sie stellen einen intrinsischen Teil der Options Definition dar.

5.  Sie können auch einer beliebigen ScoredProperty-Instanz Eigenschafts Instanzen hinzufügen. Eigenschaften Instanzen werden nur verwendet, wenn der PrintTicket-Anbieter ihre Verwendung explizit unterstützt. Jeder Anbieter sollte den Zweck und die Verwendung aller unterstützten Eigenschaften Instanzen dokumentieren. Beachten Sie, dass während der Validierung alle Eigenschaften Instanzen, die in einer Options Instanz enthalten sind, entfernt werden, es sei denn, der Namespace der Eigenschaft wird von den Ziel-printfunktionen oder dem PrintTicket-Anbieter erkannt, und im Printworks-Dokument ist eine Kandidaten Option enthalten, deren ScoredProperty-Instanzen mit den in der Option Verweis definierten Funktionen identisch sind.

6.  Wenn die Schlüsselwörter des Druck Schemas die SelectionType-Eigenschaft für eine bestimmte Funktion auf pickmany festlegen, können Sie mehrere Optionen für dieses Feature auswählen, vorausgesetzt, dass es sich bei der als identityoption bezeichneten Option nicht um eine der ausgewählten Optionen handelt. Die identityoption im Druck Schema hat dieselbe Auswirkung wie die Option None in den Dateien der PostScript PPD und Unidrv-GPD. Er dient als No-op.

7.  Untersuchen Sie das printfunktionalitäten-Dokument für ParameterDef-Instanzen, die in Ihrem PrintTicket festgelegt werden sollen. Wählen Sie für jede solche ParameterDef-Instanz einen Wert aus, der in der parameterinit-Instanz in PrintTicket verwendet werden soll. Dieser Wert muss den korrekten Datentyp aufweisen und muss innerhalb des Bereichs liegen, der in der ParameterDef-Instanz definiert ist, und muss alle anderen in der ParameterDef-Instanz angegebenen Anforderungen erfüllen. Verwenden Sie eine parameterinit-Instanz, um den-Parameter für den von Ihnen ausgewählten Wert zu initialisieren.

8.  Überprüfen Sie den Inhalt der einzelnen Options Instanzen, die im PrintTicket für Vorkommen von ParameterRef-Instanzen angezeigt werden. Wenn eine entsprechende parameterinit-Instanz nicht bereits in PrintTicket angezeigt wird, befolgen Sie den vorherigen Schritt, um eine parameterinit-Instanz in PrintTicket zu erstellen. Der Zweck dieser parameterinit-Instanz ist die Initialisierung des Parameters, auf den von der ParameterRef-Instanz verwiesen wird.

9.  Beachten Sie, dass Einschränkungs Konflikte möglicherweise verhindern, dass das Gerät die im PrintTicket angegebene Konfiguration anwendet. Bei Bedarf ändert der Überprüfungsprozess die im PrintTicket definierte Konfiguration in eine, die keine Konflikte hat.

10. Überprüfen Sie die Schlüsselwörter des Druck Schemas für Eigenschaften Instanzen, die in Ihrem PrintTicket vorhanden sein müssen. Fügen Sie Ihrem PrintTicket eine Eigenschaften Instanz für jede erforderliche hinzu, und geben Sie mit dem Value-Elementtyp einen passenden Wert an. Stellen Sie sicher, dass die Eigenschaften Instanzen innerhalb von PrintTicket ordnungsgemäß gefunden werden.

11. Überprüfen Sie die optionalen Eigenschaften Instanzen im PrintTicket-Schema. Wenn solche Eigenschaften Instanzen in Ihrem PrintTicket vorhanden sein sollten, erstellen Sie diese in Ihrem PrintTicket.

12. Sie können auch privat definierte Eigenschaften Instanzen auf der Stamm Ebene oder einer beliebigen Funktion, Option oder Eigenschaften Instanz hinzufügen. Beachten Sie jedoch, dass diese privat definierten Eigenschaften Instanzen während der Validierung entfernt werden, es sei denn, der Namespace, zu dem Sie gehören, wird von den Ziel-printfunktionen oder dem PrintTicket-Anbieter erkannt. Außerdem werden Eigenschaften Instanzen, die an einer beliebigen Stelle in einer Options Instanz angezeigt werden, während der Validierung entfernt, es sei denn, das printfunktionalitäten-Dokument enthält eine Option, die eine perfekte Entsprechung darstellt. Zwei Options Instanzen sind eine perfekte Übereinstimmung, wenn jede ScoredProperty in einer Options Instanz über eine entsprechende ScoredProperty verfügt und die Werte der ScoredProperty-Instanzen identisch sind. Weitere Informationen finden Sie unter dem privaten Schema des PrintTicket-Anbieters, um eine Liste bekannter Instanzen der privaten Eigenschaft und ihrer Verwendungsmöglichkeiten zu erhalten

13. Untergeordnete Elemente desselben Elementtyps dürfen nicht in einer Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Typ von Element, der definiert werden kann.

> [!Note]  
> Der XML-Inhalt von PrintTicket muss entweder mit UTF-8 oder UTF-16 codiert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



