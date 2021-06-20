---
description: Erfahren Sie, wie Sie ein generisches PrintTicket erstellen, falls das PrintCapabilities-Dokument für das Gerät nicht verfügbar ist.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Erstellen eines generischen PrintTickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e611205663138b9cc3c0d3cd315c2c19d2d7e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409523"
---
# <a name="creating-a-generic-printticket"></a>Erstellen eines generischen PrintTickets

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Wenn das PrintCapabilities-Dokument für das Gerät nicht verfügbar ist oder das Zielgerät unbekannt ist, sollten Sie ein generisches PrintTicket erstellen. Da es kein PrintCapabilities-Dokument gibt, das einen Satz von Feature- und Optionselementen oder Parametern enthält, müssen die unterstützten Instanzen dieser Elementtypen direkt aus den Druckschemaschlüsselwörtern erhalten werden.

Die in der folgenden Liste gezeigten Schritte sollten verwendet werden, wenn Sie ein generisches PrintTicket erstellen.

1.  Erstellen Sie ein leeres XML-Dokument, das den PrintTicket-Stamm enthält. Weisen Sie dem Druckschemanamespace ein Namespacepräfix zu. Geben Sie die Schemaversion an.

2.  Untersuchen Sie die Featureinstanzen in den Druckschemaschlüsselwörtern, und bestimmen Sie, welche dieser Instanzen in Ihrem PrintTicket definiert werden soll. Fügen Sie diese Featureinstanzen Ihrem PrintTicket hinzu. Wenn Sie ein Unterfeature übertragen, müssen Sie das übergeordnete Feature übertragen und die Über-/Unterfunktionsbeziehung zwischen dem Feature und dem Unterfeature im PrintTicket beibehalten.

    Bestimmen Sie für jede Featureinstanz, die Sie übertragen, welche Optionsinstanzen auf Ihr PrintTicket anwendbar sind. Übertragen Sie aus diesem Satz von Optionsinstanzen jede gesamte Option-Instanz so, wie sie im Druckschema angezeigt wird, und entfernen Sie dann alle property -Instanzen, die vorhanden sind, mit ausnahme derer, die für Ihr PrintTicket von Bedeutung sind. Behalten Sie alle ScoredProperty-Instanzen bei, und stellen Sie sicher, dass sie ihren Speicherort beibehalten. sie sind ein intrinsischer Bestandteil der Option-Definition.

3.  Sie können jeder ScoredProperty auch Eigenschaftsinstanzen hinzufügen. Eigenschaftselemente sind nur anwendbar, wenn der PrintTicket-Anbieter deren Verwendung explizit unterstützt. Jeder Anbieter sollte den Zweck und die Verwendung aller unterstützten Eigenschafteninstanzen dokumentieren. Da Sie nicht wissen, welcher Anbieter printTicket verarbeiten wird, sollten Sie nur die Property-Instanzen anfügen, die explizit vom PrintTicket-Systemanbieter unterstützt werden.

4.  Wenn die SelectionType-Eigenschaft für ein bestimmtes Feature von den Druckschemaschlüsselwörtern auf PickMany festgelegt wird, können Sie mehrere Optionen für dieses Feature auswählen, vorausgesetzt, dass es sich bei der option, die als IdentityOption festgelegt ist, nicht um eine der ausgewählten Optionen handelt. IdentityOption im Druckschema hat die gleiche Wirkung wie die Option Keine in Postscript-PPD-Dateien und Unidrv-GPD-Dateien. sie dient als No-Op.

5.  Untersuchen Sie die Print Schema Keywords für ParameterDef-Instanzen, die in Ihrem PrintTicket initialisiert werden sollen. Wählen Sie für jede dieser ParameterDef-Instanzen den Wert aus, der in der ParameterInit-Instanz in PrintTicket verwendet werden soll. Dieser Wert muss vom richtigen Datentyp sein, muss innerhalb des bereichs liegen, der in der ParameterDef-Instanz definiert ist, und muss alle anderen Anforderungen erfüllen, die in der ParameterDef-Instanz angegeben sind. Verwenden Sie eine ParameterInit-Instanz, um den Parameter mit dem von Ihnen ausgewählten Wert zu initialisieren.

    Wenn Sie eine Benutzeroberflächenkomponente entwickeln, entwerfen Sie die PrintTicket-Generierungsmethoden, damit Benutzer den Wert für das ParameterInit-Element eingeben können. Darüber hinaus sollte die Eingabemethode der Benutzeroberfläche alle Eingabeeinschränkungen beachten und einhalten, die vom zugeordneten ParameterDef-Element angegeben werden.

6.  Überprüfen Sie den Inhalt jeder Option-Instanz, die im PrintTicket angezeigt wird, auf Vorkommen von ParameterRef. Wenn im PrintTicket noch keine entsprechende ParameterInit-Instanz angezeigt wird, führen Sie den vorherigen Schritt aus, um eine ParameterInit-Instanz im PrintTicket zu erstellen. Der Zweck dieser ParameterInit-Instanz besteht im Initialisieren des Parameters, auf den von der ParameterRef-Instanz verwiesen wird.

7.  Beachten Sie, dass das Gerät, das den Auftrag verarbeitet, möglicherweise nicht jedes im PrintTicket angegebene Feature unterstützt. Beachten Sie auch, dass ein benanntes Feature unterstützt werden kann, aber eine angegebene Option dieses Features möglicherweise nicht ist. Die gleichen Einschränkungen gelten für Parameter. Auch wenn ein Gerät einen benannten Parameter unterstützt, liegt der in der ParameterInit-Instanz angegebene Wert möglicherweise nicht innerhalb des gültigen Bereichs für das Gerät.

8.  Überprüfen Sie die Druckschemaschlüsselwörter für Eigenschafteninstanzen, die in Ihrem PrintTicket vorhanden sein müssen. Fügen Sie Ihrem PrintTicket jeweils eine Property-Instanz hinzu, und geben Sie mithilfe des Value-Elementtyps einen geeigneten Wert dafür an. Stellen Sie sicher, dass sich Eigenschafteninstanzen ordnungsgemäß innerhalb von PrintTicket befinden. Stellen Sie sicher, dass Sie das PrintTicket-Schema anstelle des PrintCapabilities-Schemas verwenden.

9.  Untersuchen Sie die optionalen Eigenschafteninstanzen, die im PrintTicket-Schema definiert sind. Wenn es solche Property-Instanzen gibt, die sich in Ihrem PrintTicket befinden sollten, erstellen Sie sie in Ihrem PrintTicket.

10. Unterelemente desselben Elementtyps dürfen nicht bis zu einer Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Elementtyp, der definiert werden kann.

> [!Note]  
> PrintTicket XML-Inhalt MUSS entweder mit UTF-8 oder UTF-16 codiert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



