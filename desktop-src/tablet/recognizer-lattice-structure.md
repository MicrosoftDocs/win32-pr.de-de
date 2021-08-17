---
description: Erkennungen, die für die Verwendung mit Windows Vista und Windows XP Tablet PC Edition erstellt wurden, verwenden eine Reihe von Strukturen, von denen jede als Lattice bezeichnet wird, um Erkennungsergebnisse an Die Tablet PC-Plattformbibliotheken zurück zu übergeben.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Lattice-Struktur der Recognizer-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5610d60428bd3259672f43e45efa59c25f78b7ddc5909c363610eaf08520e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716018"
---
# <a name="recognizer-lattice-structure"></a>Lattice-Struktur der Recognizer-Struktur

Erkennungen, die für die Verwendung mit Windows Vista und Windows XP Tablet PC Edition erstellt wurden, verwenden eine Reihe von Strukturen, von denen jede als Lattice bezeichnet wird, um Erkennungsergebnisse an Die Tablet PC-Plattformbibliotheken zurück zu übergeben. Die Tablet PC-Plattform kopiert dann die Informationen in diesen Strukturen in das [**IInkRecognitionResult-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) die [**IInkRecognitionAlternates-Sammlung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) und das [**IInkRecognitionAlternate-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)

Ein Zeiger auf den Lattice sollte von der -Erkennen zurückgegeben werden, wenn die Plattform die [**GetLatticePtr-Funktion**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) für das [HRECOCONTEXT-Handle](hrecocontext-handle.md) aufruft.

In diesem Abschnitt wird die Latticestruktur ausführlich beschrieben. Eine Übersicht über Erkennungen und verwandte Konzepte finden Sie unter [Informationen zur Handschrifterkennung.](about-handwriting-recognition.md)

## <a name="the-need-for-a-lattice"></a>Die Notwendigkeit eines Lattices

Eine Erkennung kann mehrere Möglichkeiten finden, einen Satz von Ink-Strichen in Erkennungssegmente zu unterteilen. Was die Erkennung als Erkennungssegment verwendet, hängt vom Typ der Erkennung ab. Erkennungen in englischer Sprache verwenden in der Regel Wörter als Erkennungssegment. Andere Erkennungen verwenden möglicherweise Zeichen, Formen oder Gesten als Erkennungssegment. Die Flexibilität der Latticestrukturen ermöglicht die logische Verwaltung der großen Anzahl von Erkennungsergebnissen, die in komplexen Beziehungen kombiniert werden können.

Intern verwenden Erkennungen ein Lattice, um grundlegende Erkennungseinheiten für ein bestimmtes Stück Ink zu halten. Das Lattice enthält auch die Bewertung oder konfidenzstufe des kombinierten Ergebnisses. Darüber hinaus speichert das Lattice die Zuordnung von Segmenten zu den ursprünglichen Ink-Strichen.

Die Latticestrukturen werden in der Headerdatei RecTypes.h definiert. Die Lattice-Strukturen umfassen die folgenden Strukturen:

-   [**\_RECO-LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**\_RECO-LATTICE-SPALTE \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**RECO \_ LATTICE-ELEMENT \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**\_RECO-LATTICE-EIGENSCHAFTEN \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**\_RECO-LATTICE-EIGENSCHAFT \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Lattice-Komponenten

In den folgenden Beispielen werden die Striche für das Wort "together" verwendet, wie in der folgenden Abbildung dargestellt. In den Beispielen werden die Segmente als ein oder mehrere Wörter ausgewertet. Die Zahlen stellen die einzelnen Striche in dem Segment dar, das ausgewertet wird. Beachten Sie, dass jedes der "t"-Zeichen zwei Striche enthält.

![Striche für das Wort "zusammen"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Ein Lattice besteht aus einer oder mehreren Spalten, eine für jedes Segment. Jede Spalte enthält wiederum ein oder mehrere Elemente. Ein Element enthält eine diskrete Erkennungs alternative. Weitere Informationen zu Spalten finden Sie in der [**RECO \_ LATTICE \_ COLUMN-Struktur.**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) Weitere Informationen zu Elementen finden Sie in der [**RECO \_ LATTICE-ELEMENT-Struktur. \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)

Bei der Auswertung des im vorherigen Beispiel gezeigten Ink-Beispiels gibt die Recognizer möglicherweise ein einzelnes Segment zurück. In diesem Fall enthält das Lattice eine einzelne Spalte mit einem einzelnen Element.

Ein komplexeres Beispiel zeigt sich, wenn die Recognizer das Ink-Beispiel auswertet und mehrere Segmente und mehrere Alternativen für jedes Segment enthält.

Die Anzahl der Erkennungswechsel kann sich auch bei einer kleinen Ink-Stichprobe staffeln. Beispielsweise kann "t o g e t h e r" die folgenden Ergebnisse liefern:

-   "to get her" (plus Alternativen für jedes Wort)
-   "to gather" (plus Alternativen für jedes Wort)
-   "to got her" (plus Alternativen für jedes Wort)
-   "together" (plus Alternativen für das Wort)

In diesem Fall kann eine -Erkannte die folgende Latticestruktur erstellen.

![Lattice-Struktur für das Wort "together"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Jede Spalte hat die gleiche Strich reihenfolge, da sie alle auf dieselbe [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) verweisen.

 

 

 
