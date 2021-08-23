---
description: Erfahren Sie, wie Sie ein generisches PrintTicket erstellen, falls das PrintCapabilities-Dokument für das Gerät nicht verfügbar ist.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Erstellen eines generischen PrintTickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f660b2f1c015e0d32f5bfd80d58cae96cf3450dfafb13a7758c644ad0a7576b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719730"
---
# <a name="creating-a-generic-printticket"></a>Erstellen eines generischen PrintTickets

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Wenn das PrintCapabilities-Dokument für das Gerät nicht verfügbar ist oder das Zielgerät unbekannt ist, sollten Sie ein generisches PrintTicket erstellen. Da es kein PrintCapabilities-Dokument gibt, das eine Reihe von Feature- und Optionselementen oder Parametern bereitstellt, müssen die unterstützten Instanzen dieser Elementtypen direkt aus den Schlüsselwörtern für Das Druckschema abgerufen werden.

Die in der folgenden Liste aufgeführten Schritte sollten verwendet werden, wenn Sie ein generisches PrintTicket erstellen.

1.  Erstellen Sie ein leeres XML-Dokument, das den PrintTicket-Stamm enthält. Weisen Sie dem Namespace Print Schema ein Namespacepräfix zu. Geben Sie die Schemaversion an.

2.  Untersuchen Sie die Featureinstanzen in den Schlüsselwörtern für Das Druckschema, und bestimmen Sie, welche dieser Instanzen in Ihrem PrintTicket definiert werden sollen. Fügen Sie diese Featureinstanzen ihrem PrintTicket hinzu. Wenn Sie ein Untergeordnetes Feature übertragen, müssen Sie das übergeordnete Feature übertragen und die Über-/Unterfeaturebeziehung zwischen dem Feature und dem Untergeordneten Feature im PrintTicket beibehalten.

    Legen Sie für jede übertragene Funktionsinstanz fest, welche Optionsinstanzen auf Ihr PrintTicket anwendbar sind. Übertragen Sie aus diesem Satz von Optionsinstanzen jede gesamte Option-Instanz, wie sie im Druckschema angezeigt wird, und entfernen Sie dann alle vorhandenen Eigenschafteninstanzen, mit Ausnahme derjenigen, die für Ihr PrintTicket von Bedeutung sind. Behalten Sie alle ScoredProperty-Instanzen bei, und stellen Sie sicher, dass Sie deren Speicherort beibehalten. sie sind ein systeminterner Teil der Option-Definition.

3.  Sie können auch Jeder ScoredProperty Eigenschafteninstanzen hinzufügen. Eigenschaftselemente sind nur anwendbar, wenn der PrintTicket-Anbieter deren Verwendung explizit unterstützt. Jeder Anbieter sollte den Zweck und die Verwendung aller unterstützten Eigenschafteninstanzen dokumentieren. Da Sie nicht wissen, welcher Anbieter das PrintTicket verarbeitet, möchten Sie möglicherweise nur die Eigenschafteninstanzen anfügen, die explizit vom PrintTicket-Systemanbieter unterstützt werden.

4.  Wenn die Schlüsselwörter des Druckschemas die SelectionType-Eigenschaft für ein bestimmtes Feature auf PickMany festlegen, können Sie mehrere Optionen für dieses Feature auswählen, vorausgesetzt, dass die als IdentityOption festgelegte Option nicht eine der ausgewählten Optionen ist. IdentityOption im Druckschema hat die gleiche Auswirkung wie die Option None in Postscript PPD-Dateien und Unidrv-GPD-Dateien. sie dient als No-Op.

5.  Untersuchen Sie die Druckschemaschlüsselwörter für ParameterDef-Instanzen, die in Ihrem PrintTicket initialisiert werden sollen. Wählen Sie für jede solche ParameterDef-Instanz den Wert aus, der in der ParameterInit-Instanz im PrintTicket verwendet werden soll. Dieser Wert muss den richtigen Datentyp aufweisen, innerhalb des in der ParameterDef-Instanz definierten Bereichs liegen und alle anderen Anforderungen erfüllen, die in der ParameterDef-Instanz angegeben sind. Verwenden Sie eine ParameterInit-Instanz, um den Parameter mit dem ausgewählten Wert zu initialisieren.

    Wenn Sie eine Benutzeroberflächenkomponente entwickeln, entwerfen Sie die PrintTicket-Generierungsmethoden so, dass Benutzer den Wert für das ParameterInit-Element eingeben können. Darüber hinaus sollte die Eingabemethode der Benutzeroberfläche alle Eingabeeinschränkungen beachten und einhalten, die durch das zugeordnete ParameterDef-Element angegeben werden.

6.  Überprüfen Sie den Inhalt jeder Option-Instanz, die im PrintTicket angezeigt wird, auf Vorkommen von ParameterRef. Wenn eine entsprechende ParameterInit-Instanz nicht bereits im PrintTicket angezeigt wird, führen Sie den vorherigen Schritt aus, um eine ParameterInit-Instanz im PrintTicket zu erstellen. Der Zweck dieser ParameterInit-Instanz besteht darin, den Parameter zu initialisieren, auf den von der ParameterRef-Instanz verwiesen wird.

7.  Beachten Sie, dass das Gerät, das den Auftrag verarbeitet, möglicherweise nicht jedes im PrintTicket angegebene Feature unterstützt. Beachten Sie auch, dass ein benanntes Feature unterstützt werden kann, aber eine angegebene Option dieses Features möglicherweise nicht ist. Die gleichen Einschränkungen gelten für Parameter. Selbst wenn ein Gerät einen benannten Parameter unterstützt, liegt der in der ParameterInit-Instanz angegebene Wert möglicherweise nicht innerhalb des gültigen Bereichs für das Gerät.

8.  Untersuchen Sie die Druckschemaschlüsselwörter für Eigenschafteninstanzen, die in Ihrem PrintTicket vorhanden sein müssen. Fügen Sie ihrer PrintTicket-Instanz jeweils eine Property-Instanz hinzu, und geben Sie mithilfe des Value-Elementtyps einen geeigneten Wert dafür an. Stellen Sie sicher, dass sich Eigenschafteninstanzen ordnungsgemäß im PrintTicket befinden. Stellen Sie sicher, dass Sie das PrintTicket-Schema anstelle des PrintCapabilities-Schemas lesen.

9.  Untersuchen Sie die optionalen Eigenschafteninstanzen, die im PrintTicket-Schema definiert sind. Wenn solche Eigenschafteninstanzen in Ihrem PrintTicket vorhanden sein sollten, erstellen Sie sie in Ihrem PrintTicket.

10. Untergeordnete Elemente des gleichen Elementtyps dürfen nicht in eine Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Elementtyp, der definiert werden kann.

> [!Note]  
> PrintTicket-XML-Inhalt MUSS entweder mit UTF-8 oder UTF-16 codiert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



