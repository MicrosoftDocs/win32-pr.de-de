---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Prüfliste zur Erstellung von printfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f730a426bb787104e08f879ecccd357fd3102b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353267"
---
# <a name="printcapabilities-document-construction-checklist"></a>Prüfliste zur Erstellung von printfunktionen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Die [Zusammenfassung der Element Typen](summary-of-element-types.md) erläutert die verschiedenen Elemente, aus denen ein printfunktionen-Dokument besteht. Dieser Abschnitt enthält eine Prüfliste, die Autoren von Printworks-Dokumenten zum Erstellen eines printfunktionalitäten-Dokuments verwenden können, das ein Gerät beschreibt.

1.  Identifizieren Sie alle Geräte Attribute, die zur Gerätekonfiguration beitragen. Legen Sie für jedes derartige Geräte Attribut fest, ob es als Funktions-/optionskonstrukt oder als Parameter Konstrukt dargestellt werden soll.

2.  Bestimmen Sie für jedes Geräte Feature, ob es durch eine Funktion dargestellt werden kann, die in den Schlüsselwörtern für den Druck Schema definiert ist. Wenn dies nicht der Fall ist, müssen Sie eine neue privat definierte Funktion (und ein entsprechendes Namensattribut) einführen.

    -   Identifizieren Sie für Schlüsselwörter von Druck Schema-Schlüsselwörtern definierte Funktions Instanzen jeden der verfügbaren Zustände, auf die diese Funktion festgelegt werden kann. Jeder Zustand entspricht einer Option der Funktions Instanz. Legen Sie fest, welche dieser Zustände den von diesem Feature zugeordneten Druck Schema definierten Options Instanzen entsprechen und welche Zustände eine angepasste Options Instanz erfordern. Das Thema " [options Definitionen](option-definitions.md) " enthält Informationen zum Erstellen neuer Options Instanzen und zum Ableiten neuer Options Instanzen aus vorhandenen Options Instanzen.

    -   Identifizieren Sie bei nicht standardmäßigen Funktions Instanzen die Merkmale, die verwendet werden können, um eine Option von einer anderen zu unterscheiden. Stellen Sie jedes dieser Merkmale durch ein ScoredProperty-Element dar, und weisen Sie jeder ScoredProperty in jeder Options Instanz einen Wert zu, der für diese Option spezifisch ist. Stellen Sie sicher, dass genügend ScoredProperty-Elemente vorhanden sind, sodass jede Option für eine bestimmte Funktion eindeutig ist. Nicht dem Standard entsprechende Funktions-und Options Instanzen sind naturgemäß nicht portabel. Das heißt, dass ein anderer Treiber keine äquivalente Funktion oder Option finden kann, um eine Übereinstimmung mit einer nicht dem Standard entsprechenden Funktion oder Option zu finden, die in dem von Ihrem Treiber erstellten PrintTicket angegeben ist.

3.  Bestimmen Sie, ob eine Option ParameterRef-Elemente enthalten muss. Weitere Informationen finden Sie unter [Parameterkonstrukte](parameter-constructs.md) und [Parameter Verweis Elemente](parameter-reference-elements.md).

4.  Legen Sie für Parameter fest, ob eine der ParameterDef-Instanzen, die in den Schlüsselwörtern für den Druck Schema definiert sind, eine angemessene Entsprechung ist Wenn dies der Fall ist, kopieren Sie die ParameterDef-Instanz aus den Schlüsselwörtern des Druck Schemas, und passen Sie den Wert der einzelnen änderbaren Eigenschaften Instanzen an Wenn keine der ParameterDef-Instanzen in den Print Schema-Schlüsselwörtern eine angemessene Entsprechung ist, erstellen Sie eine eigene ParameterDef-Instanz. Weitere Informationen finden Sie unter [Parameter im Dokument "printfunktionalitäten](parameters-in-the-printcapabilities-document.md)".

5.  Stellen Sie sicher, dass alle Eigenschaften-und ScoredProperty-Instanzen, die für das Schlüsselwort "Print Schema Keywords" erforderlich sind, in Ihrem Printworks-Dokument vorhanden sind und ordnungsgemäß initialisiert sind.

6.  Fügen Sie zusätzliche Eigenschafts-und unter Eigenschaften Instanzen wie gewünscht hinzu. Sie können privat definierte Eigenschaften Instanzen einführen, wenn es Aspekte des Geräts gibt, die Sie charakterisieren müssen, die nicht von den in den Schlüsselwörtern des Print-Schemas definierten Eigenschaften Instanzen abgedeckt werden.

7.  Beachten Sie die Namespace Konvention für namens Attribute. Dies gilt für Privat definierte namens Attribute sowie für diejenigen, die in den Schlüsselwörtern des Print-Schemas definiert sind.

8.  Untergeordnete Elemente desselben Elementtyps dürfen nicht in einer Tiefe von mehr als 10 Elementen geschachtelt werden. Diese Regel gilt unabhängig für jeden Typ von Element, der definiert werden kann.

Beachten Sie, dass der XML-Inhalt von Druckfunktionen mit UTF-8 oder UTF-16 codiert werden muss.

Beachten Sie, dass der Satz von Funktions-, Options-und ParameterDef-Instanzen unabhängig von der Momentaufnahme nicht geändert werden darf. Die ScoredProperty-Instanzen, die die einzelnen Options Instanzen bilden, sowie der Wert, der den einzelnen ScoredProperty-Elementen zugewiesen ist, dürfen sich ebenfalls nicht ändern. Das gleiche gilt für die Eigenschaften Instanzen, aus denen sich die einzelnen ParameterDef-Instanzen bilden.

Eine Liste zusätzlicher Eigenschaften Instanzen, die bereitgestellt werden müssen, um Funktions-/optionskonstrukte und-Parameter vollständig zu definieren, finden Sie unter [ParameterDef](parameterdef.md) und [parameterinit](parameterinit.md). Beispielsweise muss jede Funktion das Verhalten der Benutzeroberfläche angeben, insbesondere, ob genau eine oder mehrere Options Instanzen gleichzeitig für jede Funktion ausgewählt werden können. Das Dokument mit dem Schlüsselwort "Print Schema" definiert diese Eigenschafts Instanzen, in denen Sie innerhalb des Printworks-Dokuments angezeigt werden müssen und die in den Schlüsselwörtern des Druck Schemas definierten Wert Instanzen verfügbar sind.

Der Printworks-Anbieter ist dafür verantwortlich, den entsprechenden Wert für alle Konfigurations abhängigen Eigenschaften Instanzen auszuwerten. Wenn die Druck Rate z. b. sowohl vom Farbmodus als auch von der verwendeten Auflösung abhängt, muss der Printworks-Anbieter die im vom Client bereitgestellten PrintTicket angegebenen Farb Modus-und Auflösungseinstellungen notieren und den richtigen Wert für die Druck Rate melden. Beachten Sie, dass jede ScoredProperty-Instanz einwertig sein muss. die Wert Instanz kann sich nicht ändern, wenn die Gerätekonfiguration geändert wird.

Beachten Sie auch, dass die in den Schlüsselwörtern des Druck Schemas definierten Eigenschaften Instanzen an der dort angegebenen Position angezeigt werden müssen. Sie können in einem Printworks-Dokument nicht an beliebigen Orten angezeigt werden. Privat definierte Eigenschaften Instanzen können überall angezeigt werden, auch als untergeordnete Eigenschaften innerhalb von Schema definierten Eigenschaften Instanzen.

Beachten Sie, dass ein funktionaler Konflikt zwischen Einstellungen als zwei nicht in Konflikt stehende Druck Schema Elemente definiert ist, die über eine ähnliche Funktion verfügen, aber unterschiedliche Funktionen aufweisen. Ein Beispiel wäre jobduplexalldocumentscontiguron und DocumentDuplex. Beide stellen die Duplex Funktion des Geräts dar, unterscheiden sich jedoch in der Anwendung der Funktion, eine, die auf den gesamten Auftrag angewendet wird, und eine auf Dokumente. Wenn zwei solche Elemente angegeben werden, wird die Rangfolge durch den Printworks Producer und den PrintTicket-Consumer bestimmt. Der Printworks Producer ist dafür verantwortlich, Einschränkungen zwischen widersprüchlichen Elementen durch das "eingeschränkte" Attribut anzugeben. Elemente im öffentlichen Druck Schema, die diesen semantischen Konflikt aufweisen, werden in ihrer Definition identifiziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



