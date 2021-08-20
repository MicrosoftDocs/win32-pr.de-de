---
description: Dieser Artikel enthält eine Prüfliste, mit der Autoren von PrintCapabilities-Dokumenten ein PrintCapabilities-Dokument erstellen können, das ein Gerät beschreibt.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Prüfliste für die Dokumentkonstruktion "PrintCapabilities"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5284a480f73151750926d975535ea799457a1ce2cd4c14f197a4fc6519b646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867962"
---
# <a name="printcapabilities-document-construction-checklist"></a>Prüfliste für die Dokumentkonstruktion "PrintCapabilities"

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Unter [Zusammenfassung der Elementtypen werden](summary-of-element-types.md) die verschiedenen Elemente erläutert, aus denen ein PrintCapabilities-Dokument zusammenhing. Dieser Abschnitt enthält eine Prüfliste, mit der Autoren von PrintCapabilities-Dokumenten ein PrintCapabilities-Dokument erstellen können, das ein Gerät beschreibt.

1.  Identifizieren Sie alle Geräteattribute, die zur Gerätekonfiguration beitragen. Bestimmen Sie für jedes solche Geräteattribut, ob es als Feature-/Optionskonstrukt oder als Parameterkonstrukt dargestellt werden soll.

2.  Bestimmen Sie für jedes Gerätefeature, ob es durch ein Feature dargestellt werden kann, das in den Schlüsselwörtern für Druckschemas definiert ist. Falls nicht, müssen Sie ein neues privat definiertes Feature (und ein entsprechendes Namensattribut) einführen.

    -   Identifizieren Sie für durch Druckschemaschlüsselwörter definierte Featureinstanzen jeden der verfügbaren Zustände, auf die dieses Feature festgelegt werden kann. Jeder Zustand entspricht einer Option der Featureinstanz. Bestimmen Sie, welcher dieser Zustände den druckschemadefinierten Optionsinstanzen entspricht, die diesem Feature zugeordnet sind, und welche Zustände eine benutzerdefinierte Optionsinstanz erfordern. Das [Thema Optionsdefinitionen](option-definitions.md) enthält Informationen zum Erstellen neuer Optionsinstanzen und zum Ableiten neuer Optionsinstanzen von vorhandenen Optionsinstanzen.

    -   Identifizieren Sie für nicht standardmäßige Featureinstanzen die Merkmale, die verwendet werden können, um eine Option von einer anderen zu unterscheiden. Stellen Sie jedes dieser Merkmale durch ein ScoredProperty-Element dar, und weisen Sie jeder ScoredProperty-Instanz einen Wert zu, der für diese Option spezifisch ist. Stellen Sie sicher, dass genügend ScoredProperty-Elemente vorhanden sind, damit jede Option für ein bestimmtes Feature eindeutig ist. Nicht standardmäßige Feature- und Optionsinstanzen sind naturgemäß nicht portierbar. Das heißt, dass ein anderer Treiber keine gleichwertige Funktion oder Option finden kann, die mit einem nicht standardmäßigen Feature oder einer Option übereinstimmen, das im printTicket angegeben ist, das ihr Treiber erstellt.

3.  Bestimmen Sie, ob eine Option ParameterRef-Elemente enthalten muss. Weitere Informationen finden Sie unter [Parameterkonstrukte und](parameter-constructs.md) [Parameterverweiselemente.](parameter-reference-elements.md)

4.  Bestimmen Sie bei Parametern, ob eine der ParameterDef-Instanzen, die in den Schlüsselwörtern für Druckschemas definiert sind, eine geeignete Übereinstimmung ist. Wenn dies der Fall ist, kopieren Sie die ParameterDef-Instanz aus den Druckschemaschlüsselwörtern, und passen Sie den Wert jeder veränderlichen Property-Instanz an, damit er am besten passt. Wenn keine der ParameterDef-Instanzen in den Druckschemaschlüsselwörtern eine geeignete Übereinstimmung ist, erstellen Sie eine eigene ParameterDef-Instanz. Weitere Informationen finden Sie unter [Parameter im PrintCapabilities-Dokument.](parameters-in-the-printcapabilities-document.md)

5.  Stellen Sie sicher, dass alle Property- und ScoredProperty-Instanzen, die für das Dokument Print Schema Keywords erforderlich sind, in Ihrem PrintCapabilities-Dokument vorhanden sind und ordnungsgemäß initialisiert sind.

6.  Fügen Sie nach Wunsch zusätzliche Eigenschaften- und Untereigenschafteninstanzen hinzu. Sie können privat definierte Eigenschafteninstanzen einführen, wenn es Aspekte des Geräts gibt, die Sie charakterisieren müssen, die nicht von den Eigenschafteninstanzen abgedeckt werden, die in den Schlüsselwörtern für Druckschemas definiert sind.

7.  Beachten Sie die Namespacekonvention für Namensattribute. Dies gilt sowohl für privat definierte Namensattribute als auch für diejenigen, die in den Schlüsselwörtern für Druckschemas definiert sind.

8.  Unterelemente desselben Elementtyps dürfen nicht bis zu einer Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Elementtyp, der definiert werden kann.

Beachten Sie, dass Dokument-XML-Inhalt von Druckfunktionen entweder mit UTF-8 oder UTF-16 codiert werden muss.

Beachten Sie, dass sich die gemeldeten Instanzen Feature, Option und ParameterDef unabhängig von der Momentaufnahme nicht ändern dürfen. Die ScoredProperty-Instanzen, aus denen jede Option-Instanz besteht, und der Wert, der jedem ScoredProperty-Element zugewiesen ist, dürfen sich ebenfalls nicht ändern. Dasselbe gilt für die Property-Instanzen, aus denen die einzelnen ParameterDef-Instanzen sind.

Eine Liste der zusätzlichen Eigenschafteninstanzen, die bereitgestellt werden müssen, um Funktions-/Optionskonstrukte und Parameter vollständig zu definieren, finden Sie unter [ParameterDef](parameterdef.md) und [ParameterInit](parameterinit.md). Beispielsweise muss jedes Feature sein Verhalten der Benutzeroberfläche (UI) angeben, insbesondere, ob genau eine oder mehrere Optionsinstanzen für jedes Feature gleichzeitig ausgewählt werden können. Das Dokument Print Schema Keywords definiert diese Eigenschafteninstanzen, in denen sie im PrintCapabilities-Dokument angezeigt werden müssen und welche Value-Instanzen, die in den Druckschemaschlüsselwörtern definiert sind, verfügbar sind.

Der PrintCapabilities-Anbieter ist für die Ausgabe des entsprechenden Werts für alle konfigurationsabhängigen Eigenschafteninstanzen verantwortlich. Wenn die Druckrate beispielsweise sowohl vom Farbmodus als auch von der verwendeten Auflösung abhängt, muss der PrintCapabilities-Anbieter den Farbmodus und die Auflösungseinstellungen notieren, die im vom Client bereitgestellten PrintTicket angegeben sind, und den richtigen Wert für die Druckrate melden. Beachten Sie, dass jede ScoredProperty-Instanz einwertig sein muss. Die Value-Instanz kann sich nicht ändern, wenn sich die Gerätekonfiguration ändert.

Beachten Sie auch, dass Eigenschafteninstanzen, die in den Druckschemaschlüsselwörtern definiert sind, an der angegebenen Position angezeigt werden müssen. Sie können nicht an beliebigen Stellen in einem PrintCapabilities-Dokument angezeigt werden. Privat definierte Eigenschafteninstanzen können überall angezeigt werden, auch als Untereigenschaften in schemadefinierten Eigenschafteninstanzen.

Beachten Sie, dass ein funktionaler Konflikt zwischen Einstellungen als zwei nicht in Konflikt stehende Druckschemaelemente definiert ist, die eine ähnliche Funktion haben, aber unterschiedliche Funktionen sind. Ein Beispiel wären JobDuplexAllDocumentsContiguously und DocumentDuplex. beide stellen die Duplexfunktion des Geräts dar, unterscheiden sich jedoch in der Anwendung der Funktion, eine, die zusammenhängend auf den gesamten Auftrag und eine für Dokumente anwendung. Wenn zwei solche Elemente angegeben werden, wird die Rangfolge durch den PrintCapabilities-Producer und den PrintTicket-Consumer bestimmt. Es liegt in der Verantwortung des PrintCapabilities-Producers, Einschränkungen zwischen in Konflikt stehenden Elementen über das Attribut "constrained" richtig anzugeben. Elemente im öffentlichen Druckschema, die diesen semantischen Konflikt zeigen, werden in ihrer Definition identifiziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



