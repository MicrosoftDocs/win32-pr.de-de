---
description: Erfahren Sie mehr über das Erstellen eines gerätespezifischen PrintTickets, das auf ein bestimmtes Gerät ausgerichtet ist und auf mehrere Geräte portierbar ist.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Erstellen eines Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b825bd875ada534c8c467cd18d90f2db9a2a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409545"
---
# <a name="creating-a-device-specific-printticket"></a>Erstellen eines Device-Specific PrintTicket

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein gerätespezifisches PrintTicket ist auf ein bestimmtes Gerät ausgerichtet und daher in der Regel nicht auf mehrere Geräte übertragbar.

Die in der folgenden Liste aufgeführten Schritte sollten verwendet werden, wenn Sie ein gerätespezifisches PrintTicket erstellen.

1.  Rufen Sie ein PrintCapabilities-Dokument ab, das nur die relevanten Funktionsinstanzen für das Gerät enthält. Fordern Sie ein PrintCapabilities-Standarddokument an. Hierfür müssen Sie kein PrintTicket-Eingabeelement angeben, da die Geräteattribute (Funktions- und Optionsinstanzen und Parameter), die zum Erstellen des PrintTicket verwendet werden, unabhängig von der Konfiguration sind.

2.  Erstellen Sie ein leeres XML-Dokument, das den PrintTicket-Stamm enthält. Weisen Sie dem Print Schema-Namespace ein Namespacepräfix zu, und weisen Sie Präfixe für alle anderen Namespaces zu, die vom PrintTicket verwendet werden. Geben Sie die PrintTicket-Schemaversion an.

3.  Sie können Einstellungen im PrintTicket für jede Feature- und ParameterDef-Instanz definieren, die im PrintCapabilities-Dokument gemeldet wird, oder nur für diejenigen, die für Sie von Interesse sind. Wenn der PrintTicket-Schnittstelle ein partielles PrintTicket angezeigt wird, werden während der PrintTicket-Überprüfung automatisch Standardwerte für ausgelassene Feature- und ParameterDef-Instanzen bereitgestellt.

4.  Überprüfen Sie das Dokument PrintCapabilities auf Funktionsinstanzen, und bestimmen Sie, welche dieser Instanzen in Ihrem PrintTicket definiert werden sollen. Fügen Sie diese Featureinstanzen dem PrintTicket hinzu, übertragen Sie jedoch nicht den Inhalt der Featureinstanzen an Ihr PrintTicket. Wenn Sie ein Untergeordnetes Feature übertragen, muss auch das übergeordnete Feature übertragen werden, und die Beziehung zwischen über- und untergeordnetem Element muss im PrintTicket beibehalten werden.

    Legen Sie für jedes übertragene Feature fest, welche Optionsinstanzen auf Ihr PrintTicket anwendbar sind. Übertragen Sie die gesamte Option wie im PrintCapabilities-Dokument definiert, und entfernen Sie dann alle vorhandenen Eigenschafteninstanzen. Die Eigenschafteninstanzen werden in PrintCapabilities-Dokumenten verwendet, erfüllen aber keinen Zweck im PrintTicket. Behalten Sie alle ScoredProperty-Instanzen bei, und stellen Sie sicher, dass Sie deren Speicherort beibehalten. sie sind ein systeminterner Teil der Option-Definition.

5.  Sie können eigenschafteninstanzen auch jeder ScoredProperty-Instanz hinzufügen. Eigenschafteninstanzen werden nur verwendet, wenn der PrintTicket-Anbieter ihre Verwendung explizit unterstützt. Jeder Anbieter sollte den Zweck und die Verwendung aller unterstützten Eigenschafteninstanzen dokumentieren. Beachten Sie, dass während der Überprüfung alle In einer Option-Instanz enthaltenen Eigenschafteninstanzen entfernt werden, es sei denn, der Namespace der Eigenschaft wird vom PrintCapabilities- oder PrintTicket-Zielanbieter erkannt, und im PrintCapabilities-Dokument befindet sich eine mögliche Option, deren ScoredProperty-Instanzen den in der Referenzoption definierten Instanzen perfekt entsprechen.

6.  Wenn die Schlüsselwörter des Druckschemas die SelectionType-Eigenschaft für ein bestimmtes Feature auf PickMany festlegen, können Sie mehrere Optionen für dieses Feature auswählen, vorausgesetzt, dass die als IdentityOption festgelegte Option nicht eine der ausgewählten Optionen ist. IdentityOption im Druckschema hat die gleiche Auswirkung wie die Option None in Postscript PPD-Dateien und Unidrv-GPD-Dateien. sie dient als No-Op.

7.  Überprüfen Sie das PrintCapabilities-Dokument auf ParameterDef-Instanzen, die in Ihrem PrintTicket festgelegt werden sollen. Wählen Sie für jede solche ParameterDef-Instanz einen Wert aus, der in der ParameterInit-Instanz im PrintTicket verwendet werden soll. Dieser Wert muss den richtigen Datentyp aufweisen und innerhalb des in der ParameterDef-Instanz definierten Bereichs liegen und alle anderen Anforderungen erfüllen, die in der ParameterDef-Instanz angegeben sind. Verwenden Sie eine ParameterInit-Instanz, um den Parameter mit dem ausgewählten Wert zu initialisieren.

8.  Überprüfen Sie den Inhalt jeder Option-Instanz, die im PrintTicket angezeigt wird, auf Vorkommen von ParameterRef-Instanzen. Wenn eine entsprechende ParameterInit-Instanz nicht bereits im PrintTicket angezeigt wird, führen Sie den vorherigen Schritt aus, um eine ParameterInit-Instanz im PrintTicket zu erstellen. Der Zweck dieser ParameterInit-Instanz besteht darin, den Parameter zu initialisieren, auf den von der ParameterRef-Instanz verwiesen wird.

9.  Beachten Sie, dass Einschränkungskonflikte das Gerät möglicherweise daran hindern, die konfiguration anzuwenden, die Sie im PrintTicket angegeben haben. Bei Bedarf ändert der Überprüfungsprozess die im PrintTicket definierte Konfiguration in eine Konfiguration, die keine Konflikte enthält.

10. Untersuchen Sie die Druckschemaschlüsselwörter für Eigenschafteninstanzen, die in Ihrem PrintTicket vorhanden sein müssen. Fügen Sie ihrem PrintTicket für jede erforderliche Instanz eine Property-Instanz hinzu, und geben Sie mithilfe des Value-Elementtyps einen geeigneten Wert dafür an. Stellen Sie sicher, dass sich Eigenschafteninstanzen ordnungsgemäß im PrintTicket befinden.

11. Untersuchen Sie die optionalen Eigenschafteninstanzen im PrintTicket-Schema. Wenn solche Eigenschafteninstanzen in Ihrem PrintTicket vorhanden sein sollten, erstellen Sie sie in Ihrem PrintTicket.

12. Sie können auch privat definierte Eigenschafteninstanzen auf Stammebene oder einer beliebigen Funktions-, Options- oder Eigenschafteninstanz hinzufügen. Beachten Sie jedoch, dass diese privat definierten Eigenschafteninstanzen während der Überprüfung entfernt werden, es sei denn, der Namespace, zu dem sie gehören, wird vom PrintCapabilities- oder PrintTicket-Zielanbieter erkannt. Darüber hinaus werden Eigenschaftsinstanzen, die an einer beliebigen Stelle innerhalb einer Option-Instanz angezeigt werden, während der Überprüfung entfernt, es sei denn, das PrintCapabilities-Dokument enthält eine Option, die eine perfekte Übereinstimmung ist. Zwei Optionsinstanzen sind eine perfekte Übereinstimmung, wenn jede ScoredProperty in einer Option-Instanz über eine entsprechende ScoredProperty in der anderen verfügt und die Werte der ScoredProperty-Instanzen identisch sind. Eine Liste der erkannten privaten Eigenschafteninstanzen und deren Verwendung finden Sie im privaten Schema des PrintTicket-Anbieters.

13. Untergeordnete Elemente desselben Elementtyps dürfen nicht in eine Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Elementtyp, der definiert werden kann.

> [!Note]  
> PrintTicket-XML-Inhalt MUSS entweder mit UTF-8 oder UTF-16 codiert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



