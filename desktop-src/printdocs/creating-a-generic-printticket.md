---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Erstellen eines generischen PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34281eda82a48ea0ac4077248547522ddc305ea
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366376"
---
# <a name="creating-a-generic-printticket"></a>Erstellen eines generischen PrintTicket

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Wenn das Printworks-Dokument für das Gerät nicht verfügbar ist oder wenn das Zielgerät unbekannt ist, sollten Sie ein allgemeines PrintTicket erstellen. Da es kein printfunktionsdokument gibt, das einen Satz von Funktions-und Options Elementen oder Parametern bereitstellt, müssen die unterstützten Instanzen dieser Elementtypen direkt aus den Schlüsselwörtern des Print-Schemas abgerufen werden.

Die in der folgenden Liste aufgeführten Schritte sollten verwendet werden, wenn Sie ein allgemeines PrintTicket erstellen.

1.  Erstellen Sie ein leeres XML-Dokument, das den PrintTicket-Stamm enthält. Weisen Sie dem Druckschema-Namespace ein Namespace Präfix zu. Geben Sie die Schema Version an.

2.  Überprüfen Sie die Funktions Instanzen in den Print Schema-Schlüsselwörtern, und legen Sie fest, welche der in Ihrem PrintTicket definierten werden soll. Fügen Sie diese Funktions Instanzen zu PrintTicket hinzu. Wenn Sie eine untergeordnete Funktion übertragen, müssen Sie die übergeordnete Funktion übertragen und die über-/Unterordnungsbeziehung zwischen der Funktion und der Unterfunktion in PrintTicket beibehalten.

    Legen Sie für jede zu übertragenden Funktions Instanz fest, welche Options Instanzen auf Ihr Print Ticket anwendbar sind. Übertragen Sie aus diesem Satz von Options Instanzen jede vollständige Options Instanz, wie Sie im Druck Schema angezeigt wird, und entfernen Sie dann alle vorhandenen Eigenschafts Instanzen, mit Ausnahme der möglichen Ausnahmen, die für Print Ticket wichtig sind. Behalten Sie alle ScoredProperty-Instanzen bei, und stellen Sie sicher, dass Sie Ihre Position beibehalten. Sie stellen einen intrinsischen Teil der Options Definition dar.

3.  Sie können auch Eigenschaften Instanzen zu beliebigen ScoredProperty-Objekten hinzufügen. Eigenschafts Elemente sind nur anwendbar, wenn der PrintTicket-Anbieter ihre Verwendung explizit unterstützt. Jeder Anbieter sollte den Zweck und die Verwendung aller unterstützten Eigenschaften Instanzen dokumentieren. Da Sie nicht wissen, welcher Anbieter das PrintTicket verarbeitet, möchten Sie möglicherweise nur die Eigenschaften Instanzen anfügen, die explizit vom System PrintTicket-Anbieter unterstützt werden.

4.  Wenn die Schlüsselwörter des Druck Schemas die SelectionType-Eigenschaft für eine bestimmte Funktion auf pickmany festlegen, können Sie mehrere Optionen für dieses Feature auswählen, vorausgesetzt, dass es sich bei der als identityoption bezeichneten Option nicht um eine der ausgewählten Optionen handelt. Die identityoption im Druck Schema hat dieselbe Auswirkung wie die Option None in den Dateien der PostScript PPD und Unidrv-GPD. Er dient als No-op.

5.  Überprüfen Sie die Druck Schema Schlüsselwörter für ParameterDef-Instanzen, die in Ihrem PrintTicket initialisiert werden sollen. Wählen Sie für jede solche ParameterDef-Instanz den Wert aus, der in der parameterinit-Instanz in PrintTicket verwendet werden soll. Dieser Wert muss den korrekten Datentyp aufweisen, muss innerhalb des Bereichs liegen, der in der ParameterDef-Instanz definiert ist, und muss alle anderen Anforderungen erfüllen, die in der ParameterDef-Instanz angegeben sind. Verwenden Sie eine parameterinit-Instanz, um den-Parameter für den von Ihnen ausgewählten Wert zu initialisieren.

    Wenn Sie eine Benutzeroberflächen Komponente entwickeln, entwerfen Sie Ihre PrintTicket-Generierungs Methoden, damit Benutzer den Wert für das parameterinit-Element eingeben können. Außerdem sollte die Methode für die Benutzeroberflächen Eingabe alle vom zugeordneten ParameterDef-Element angegebenen Eingabe Einschränkungen beobachten und einhalten.

6.  Überprüfen Sie den Inhalt der einzelnen Options Instanzen, die im PrintTicket für Vorkommen von ParameterRef angezeigt werden. Wenn eine entsprechende parameterinit-Instanz nicht bereits in PrintTicket angezeigt wird, befolgen Sie den vorherigen Schritt, um eine parameterinit-Instanz in PrintTicket zu erstellen. Der Zweck dieser parameterinit-Instanz ist die Initialisierung des Parameters, auf den von der ParameterRef-Instanz verwiesen wird.

7.  Beachten Sie, dass das Gerät, das den Auftrag verarbeitet, möglicherweise nicht alle Funktionen unterstützt, die in PrintTicket angegeben sind. Beachten Sie auch, dass eine benannte Funktion möglicherweise unterstützt wird, aber eine angegebene Option dieses Features ist möglicherweise nicht. Die gleichen Einschränkungen gelten für Parameter. Selbst wenn ein Gerät einen benannten Parameter unterstützt, liegt der in der parameterinit-Instanz angegebene Wert möglicherweise nicht innerhalb des gültigen Bereichs für das Gerät.

8.  Überprüfen Sie die Schlüsselwörter des Druck Schemas für Eigenschaften Instanzen, die in Ihrem PrintTicket vorhanden sein müssen. Fügen Sie Ihrer PrintTicket-Instanz eine Eigenschaften Instanz für diese hinzu, und geben Sie einen geeigneten Wert für diese an, indem Sie den Wert Elementtyp verwenden. Stellen Sie sicher, dass die Eigenschaften Instanzen innerhalb von PrintTicket ordnungsgemäß gefunden werden. Stellen Sie sicher, dass Sie das PrintTicket-Schema und nicht das printfunktionalitäten-Schema überprüfen.

9.  Überprüfen Sie die optionalen Eigenschaften Instanzen, die im PrintTicket-Schema definiert sind. Wenn solche Eigenschaften Instanzen in Ihrem PrintTicket vorhanden sein sollten, erstellen Sie diese in Ihrem PrintTicket.

10. Untergeordnete Elemente desselben Elementtyps dürfen nicht in einer Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Typ von Element, der definiert werden kann.

> [!Note]  
> Der XML-Inhalt von PrintTicket muss entweder mit UTF-8 oder UTF-16 codiert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



