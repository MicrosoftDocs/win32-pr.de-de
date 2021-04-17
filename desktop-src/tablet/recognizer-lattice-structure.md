---
description: Erkennungs Tools, die für die Verwendung mit Windows Vista und Windows XP Tablet PC Edition erstellt wurden, verwenden eine Reihe von Strukturen, die jeweils als Gitter bezeichnet werden, um Erkennungsergebnisse zurück an Tablet PC Platform-Bibliotheken zu übergeben.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Gitterstruktur der Erkennungsfunktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bbfe71674571ae0554509dfa8477569ef8b44d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557325"
---
# <a name="recognizer-lattice-structure"></a>Gitterstruktur der Erkennungsfunktion

Erkennungs Tools, die für die Verwendung mit Windows Vista und Windows XP Tablet PC Edition erstellt wurden, verwenden eine Reihe von Strukturen, die jeweils als Gitter bezeichnet werden, um Erkennungsergebnisse zurück an Tablet PC Platform-Bibliotheken zu übergeben. Die Tablet PC-Plattform kopiert dann die Informationen in diesen Strukturen in das [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt, die [**iinkrecognitionalternate es**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) -Auflistung und das [**iinkrecognitionalternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) -Objekt.

Ein Zeiger auf das Gitter soll von der Erkennung zurückgegeben werden, wenn die Plattform die [**getlatticeptr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) -Funktion für das [hrecocontext](hrecocontext-handle.md) -Handle aufruft.

In diesem Abschnitt wird die Gitterstruktur ausführlich beschrieben. Eine Übersicht über Erkennungs Tools und verwandte Konzepte finden Sie unter [Informationen zur Handschrifterkennung](about-handwriting-recognition.md).

## <a name="the-need-for-a-lattice"></a>Der Bedarf an einem Gitter

Eine Erkennung kann verschiedene Möglichkeiten finden, eine Menge von Hand Strichen in Erkennungs Segmente zu unterteilen. Was die Erkennung als Erkennungs Segment verwendet, hängt vom Typ des Erkennungs Moduls ab. Englische Spracherkennung verwenden in der Regel Wörter als Erkennungs Segment. Andere Erkennungs Tools verwenden möglicherweise Zeichen, Formen oder Gesten als Erkennungs Segment. Die Flexibilität der Gitterstrukturen ermöglicht die logische Verwaltung der großen Anzahl von Erkennungs Ergebnissen, die in komplexen Beziehungen kombiniert werden können.

Intern verwenden erkenzer ein Gitter, um grundlegende Erkennungs Einheiten für eine bestimmte frei Hand Eingabe zu halten. Das Gitter enthält auch das Ergebnis oder den Vertrauensgrad des kombinierten Ergebnisses. Außerdem speichert das Gitter die Zuordnung von Segmenten zu den ursprünglichen Hand Strich Eingaben.

Die Gitterstrukturen sind in der Header Datei "rectypes. h" definiert. Die Gitterstrukturen enthalten die folgenden Strukturen:

-   [**Reco- \_ Gitter**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**Reco- \_ Gitter \_ Spalte**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**Reco- \_ Gitter \_ Element**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**Eigenschaften von "Reco" \_ \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**Reco- \_ Gitter \_ Eigenschaft**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Gitter Komponenten

In den folgenden Beispielen werden die Striche für das Wort "parallel" verwendet, wie in der folgenden Abbildung dargestellt. In den Beispielen werden die Segmente als ein oder mehrere Wörter ausgewertet. Die Zahlen stellen die einzelnen Striche im auszuwertenden Segment dar. Beachten Sie, dass jedes der "t"-Zeichen zwei Striche enthält.

![Striche für das Wort "Zusammenfassung"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Ein Gitter setzt sich aus einer oder mehreren Spalten zusammen, eine für jedes Segment. Jede Spalte enthält wiederum ein oder mehrere-Elemente. Ein Element enthält eine diskrete Erkennungs Alternative. Weitere Informationen zu Spalten finden Sie in der Struktur der [**Reco- \_ Gitter \_ Spalten**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) . Weitere Informationen zu Elementen finden Sie in der Struktur von " [**Reco \_ Gitter \_ Element**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) ".

Die Erkennung gibt möglicherweise ein einzelnes Segment zurück, wenn Sie das im vorherigen Beispiel gezeigte Ink-Beispiel auswerten. In diesem Fall enthält das Gitter eine einzelne Spalte mit einem einzelnen Element.

Ein komplexeres Beispiel zeigt sich, wenn die Erkennung das Ink-Beispiel auswertet und mehrere Segmente und mehrere Alternativen für jedes Segment enthält.

Die Anzahl der Erkennungs Alternativen kann auch für ein kleines frei Hand Beispiel sehr erstaunlich sein. Beispielsweise kann "t o g e t h e r" die folgenden Ergebnisse liefern:

-   "um Sie zu erhalten" (plus Alternativen für jedes Wort)
-   "to Gather" (plus-Alternativen für jedes Wort)
-   "um Sie zu erhalten" (plus Alternativen für jedes Wort)
-   "zusammen" (plus Alternativen für das Wort)

In diesem Fall kann eine Erkennung die folgende Gitterstruktur erstellen.

![Gitterstruktur für das Wort "Zusammenfassung"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Jede Spalte hat dieselbe hubreihenfolge, da Sie alle auf dieselbe Auflistung von [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) verweisen.

 

 

 
