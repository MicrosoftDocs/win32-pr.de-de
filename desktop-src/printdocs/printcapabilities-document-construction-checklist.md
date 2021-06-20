---
description: Dieser Artikel enthält eine Prüfliste, die Autoren von PrintCapabilities-Dokumenten verwenden können, um ein PrintCapabilities-Dokument zu erstellen, das ein Gerät beschreibt.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Prüfliste für die Erstellung von PrintCapabilities-Dokumenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee309c96cf7b2d70cb78f125e7783668fb2298da
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407113"
---
# <a name="printcapabilities-document-construction-checklist"></a>Prüfliste für die Erstellung von PrintCapabilities-Dokumenten

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

[In der Zusammenfassung der Elementtypen](summary-of-element-types.md) werden die verschiedenen Elemente erläutert, aus denen ein PrintCapabilities-Dokument besteht. Dieser Abschnitt enthält eine Prüfliste, die Autoren von PrintCapabilities-Dokumenten verwenden können, um ein PrintCapabilities-Dokument zu erstellen, das ein Gerät beschreibt.

1.  Identifizieren Sie alle Geräteattribute, die zur Gerätekonfiguration beitragen. Bestimmen Sie für jedes geräteattribut, ob es als Feature-/Optionskonstrukt oder als Parameterkonstrukt dargestellt werden soll.

2.  Bestimmen Sie für jedes Gerätefeature, ob es durch ein Feature dargestellt werden kann, das in den Schlüsselwörtern für Das Druckschema definiert ist. Andernfalls müssen Sie ein neues privat definiertes Feature (und ein entsprechendes Namensattribut) einführen.

    -   Identifizieren Sie für mit Schlüsselwörtern für Druckschemas definierte Featureinstanzen jeden verfügbaren Status, auf den dieses Feature festgelegt werden kann. Jeder Zustand entspricht einer Option der Funktionsinstanz. Bestimmen Sie, welcher dieser Zustände den Mit diesem Feature verknüpften Vom Schema definierten Optionsinstanzen drucken entspricht und welche Zustände eine benutzerdefinierte Optionsinstanz erfordern. Das Thema [Optionsdefinitionen](option-definitions.md) enthält Informationen zum Erstellen neuer Optionsinstanzen und zum Ableiten neuer Optionsinstanzen von vorhandenen Optionsinstanzen.

    -   Identifizieren Sie bei nicht standardmäßigen Featureinstanzen die Merkmale, die verwendet werden können, um eine Option von einer anderen zu unterscheiden. Stellen Sie jedes dieser Merkmale durch ein ScoredProperty-Element dar, und weisen Sie jedem ScoredProperty-Element in jeder Option-Instanz einen Wert zu, der für diese Option spezifisch ist. Stellen Sie sicher, dass genügend ScoredProperty-Elemente vorhanden sind, sodass jede Option für ein bestimmtes Feature eindeutig ist. Nicht standardmäßige Feature- und Optionsinstanzen sind naturgemäß nicht portierbar. Das heißt, ein anderer Treiber kann keine entsprechende Funktion oder Option finden, die mit einer nicht dem Standard entsprechenden Funktion oder Option übereinstimmt, die im von Ihrem Treiber erstellten PrintTicket angegeben ist.

3.  Bestimmen Sie, ob eine Option ParameterRef-Elemente enthalten muss. Weitere Informationen finden Sie unter [Parameterkonstrukte](parameter-constructs.md) und [Parameterverweiselemente.](parameter-reference-elements.md)

4.  Bestimmen Sie für Parameter, ob eine der ParameterDef-Instanzen, die in den Schlüsselwörtern für Druckschemas definiert sind, eine angemessene Übereinstimmung ist. Wenn dies der Fall ist, kopieren Sie die ParameterDef-Instanz aus den Druckschemaschlüsselwörtern, und passen Sie den Wert jeder änderbaren Eigenschaftsinstanz an, um die beste Anpassung zu erhalten. Wenn keine der ParameterDef-Instanzen in den Schlüsselwörtern für Druckschemas eine angemessene Übereinstimmung ist, erstellen Sie Ihre eigene ParameterDef-Instanz. Weitere Informationen finden Sie unter [Parameter im PrintCapabilities-Dokument.](parameters-in-the-printcapabilities-document.md)

5.  Stellen Sie sicher, dass alle Property- und ScoredProperty-Instanzen, die für das Dokument Print Schema Keywords erforderlich sind, im PrintCapabilities-Dokument vorhanden sind und ordnungsgemäß initialisiert sind.

6.  Fügen Sie nach Bedarf zusätzliche Eigenschaften- und Untereigenschafteninstanzen hinzu. Sie können privat definierte Eigenschafteninstanzen einführen, wenn Es Aspekte des Geräts gibt, die Sie charakterisieren müssen, die nicht von den Eigenschafteninstanzen abgedeckt werden, die in den Schlüsselwörtern des Druckschemas definiert sind.

7.  Beachten Sie die Namespacekonvention für Namensattribute. Dies gilt sowohl für privat definierte Namensattribute als auch für die attribute, die in den Schlüsselwörtern für Druckschemas definiert sind.

8.  Untergeordnete Elemente des gleichen Elementtyps dürfen nicht in eine Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Elementtyp, der definiert werden kann.

Beachten Sie, dass der XML-Inhalt von Druckfunktionen-Dokumenten entweder mit UTF-8 oder UTF-16 codiert werden muss.

Beachten Sie, dass sich die gemeldeten Funktions-, Options- und ParameterDef-Instanzen unabhängig von der Momentaufnahme nicht ändern dürfen. Die ScoredProperty-Instanzen, aus denen jede Option-Instanz und der jedem ScoredProperty-Element zugewiesene Wert gehören, dürfen sich ebenfalls nicht ändern. Dasselbe gilt für die Property-Instanzen, aus denen jede ParameterDef-Instanz bestehen.

Eine Liste zusätzlicher Eigenschafteninstanzen, die bereitgestellt werden müssen, um Funktions-/Optionskonstrukte und Parameter vollständig zu definieren, finden Sie unter [ParameterDef](parameterdef.md) und [ParameterInit.](parameterinit.md) Beispielsweise muss jedes Feature sein Benutzeroberflächenverhalten angeben, insbesondere ob genau eine oder mehrere Optionsinstanzen für jedes Feature gleichzeitig ausgewählt werden können. Das Dokument Druckschemaschlüsselwörter definiert diese Eigenschafteninstanzen, in denen sie im PrintCapabilities-Dokument angezeigt werden müssen und welche in den Schlüsselwörtern für Druckschemas definierten Wertinstanzen verfügbar sind.

Der PrintCapabilities-Anbieter ist für die Ausgabe des entsprechenden Werts für alle konfigurationsabhängigen Eigenschafteninstanzen verantwortlich. Wenn z. B. die Druckrate sowohl vom Farbmodus als auch von der verwendeten Auflösung abhängt, muss der PrintCapabilities-Anbieter den Farbmodus und die Auflösungseinstellungen beachten, die im vom Client bereitgestellten PrintTicket angegeben sind, und den richtigen Wert für die Druckrate melden. Beachten Sie, dass jede ScoredProperty-Instanz einwertig sein muss. die Value-Instanz kann nicht geändert werden, wenn sich die Gerätekonfiguration ändert.

Beachten Sie auch, dass Eigenschafteninstanzen, die in den Schlüsselwörtern für Druckschemas definiert sind, an der dort angegebenen Position angezeigt werden müssen. Sie können nicht an beliebigen Stellen innerhalb eines PrintCapabilities-Dokuments angezeigt werden. Privat definierte Eigenschafteninstanzen können überall angezeigt werden, auch als Untereigenschaften innerhalb von Schema-defined Property-Instanzen.

Beachten Sie, dass ein funktionaler Konflikt zwischen Einstellungen als zwei nicht in Konflikt stehende Druckschemaelemente definiert ist, die eine ähnliche Funktion aufweisen, aber unterschiedliche Features sind. Ein Beispiel wären JobDuplexAllDocumentsContiguously und DocumentDuplex. beide stellen die Duplexfunktion des Geräts dar, unterscheiden sich jedoch in der Anwendung der Funktion, eine anwendung auf den gesamten Auftrag zusammenhängend und eine für Dokumente. Wenn zwei solche Elemente angegeben werden, wird die Rangfolge durch den PrintCapabilities-Producer und den PrintTicket-Consumer bestimmt. Es liegt in der Verantwortung des PrintCapabilities-Producers, Einschränkungen zwischen konfliktverursachenden Elementen über das attribut "constrained" ordnungsgemäß anzugeben. Elemente im öffentlichen Druckschema, die diesen semantischen Konflikt aufweisen, werden in ihrer Definition identifiziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



