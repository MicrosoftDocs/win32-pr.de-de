---
description: Erkennungen, die für die Verwendung mit Windows Vista und Windows XP Tablet PC Edition erstellt wurden, verwenden eine Reihe von Strukturen, die jeweils als Lattice bezeichnet werden, um Erkennungsergebnisse an Tablet PC-Plattformbibliotheken zurückzugeben.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Recognizer Lattice-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5610d60428bd3259672f43e45efa59c25f78b7ddc5909c363610eaf08520e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716018"
---
# <a name="recognizer-lattice-structure"></a>Recognizer Lattice-Struktur

Erkennungen, die für die Verwendung mit Windows Vista und Windows XP Tablet PC Edition erstellt wurden, verwenden eine Reihe von Strukturen, die jeweils als Lattice bezeichnet werden, um Erkennungsergebnisse an Tablet PC-Plattformbibliotheken zurückzugeben. Die Tablet PC-Plattform kopiert dann die Informationen in diesen Strukturen in das [**IInkRecognitionResult-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) die [**IInkRecognitionAlternates-Auflistung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) und das [**IInkRecognitionAlternate-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)

Ein Zeiger auf das Lattice sollte von der Erkennung zurückgegeben werden, wenn die Plattform die [**GetLatticePtr-Funktion**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) im [HRECOCONTEXT-Handle](hrecocontext-handle.md) aufruft.

In diesem Abschnitt wird die Lattice-Struktur ausführlich beschrieben. Eine Übersicht über Erkennungen und verwandte Konzepte finden Sie unter Informationen zur [Handschrifterkennung.](about-handwriting-recognition.md)

## <a name="the-need-for-a-lattice"></a>Die Notwendigkeit eines Lattice

Eine Erkennung kann mehrere Möglichkeiten finden, einen Satz von Ink-Strichen in Erkennungssegmente aufzuteilen. Was die Erkennung als Erkennungssegment verwendet, hängt vom Typ der Erkennung ab. Spracherkennungen in Englisch verwenden in der Regel Wörter als Erkennungssegment. Andere Erkennungen können Zeichen, Formen oder Gesten als Erkennungssegment verwenden. Die Flexibilität der Lattice-Strukturen ermöglicht die logische Verwaltung der großen Anzahl von Erkennungsergebnissen, die in komplexen Beziehungen kombiniert werden können.

Intern verwenden Erkennungen ein Gitter, um grundlegende Erkennungseinheiten für ein bestimmtes Stück Ink zu speichern. Das Lattice enthält auch die Bewertung oder den Konfidenzgrad des kombinierten Ergebnisses. Darüber hinaus speichert das Lattice die Zuordnung von Segmenten zu den ursprünglichen Ink-Strichen.

Die Lattice-Strukturen werden in der RecTypes.h-Headerdatei definiert. Die Lattice-Strukturen umfassen die folgenden Strukturen:

-   [**RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**RECO \_ \_ LATTICE-SPALTE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**RECO \_ \_ LATTICE-ELEMENT**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**RECO \_ \_ LATTICE-EIGENSCHAFTEN**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**RECO \_ \_ LATTICE-EIGENSCHAFT**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Lattice-Komponenten

In den folgenden Beispielen werden die Striche für das Wort "zusammen" verwendet, wie in der folgenden Abbildung dargestellt. In den Beispielen werden die Segmente als ein oder mehrere Wörter ausgewertet. Die Zahlen stellen die einzelnen Striche im segment dar, das ausgewertet wird. Beachten Sie, dass jedes der "t"-Zeichen zwei Striche enthält.

![Striche für das Wort "zusammen"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Ein Lattice besteht aus einer oder mehreren Spalten, einer für jedes Segment. Jede Spalte enthält wiederum mindestens ein -Element. Ein Element enthält eine diskrete Erkennungs-Alternative. Weitere Informationen zu Spalten finden Sie in der [**RECO \_ LATTICE \_ COLUMN-Struktur.**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) Weitere Informationen zu Elementen finden Sie in der [**RECO \_ LATTICE-ELEMENTstruktur. \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)

Die Erkennung gibt möglicherweise ein einzelnes Segment zurück, wenn das im vorherigen Beispiel gezeigte Ink-Beispiel ausgewertet wird. In diesem Fall enthält das Lattice eine einzelne Spalte mit einem einzelnen Element.

Ein komplexeres Beispiel zeigt sich, wenn die Erkennung die Ink-Stichprobe auswertet und mehrere Segmente und mehrere Alternative für jedes Segment enthält.

Die Anzahl von Erkennungswechseln kann sogar für eine kleine Ink-Stichprobe staffelnd sein. "t o g e t h e r" kann beispielsweise die folgenden Ergebnisse liefern:

-   "to get her" (plus Alternative für jedes Wort)
-   "to gather" (plus Alternative für jedes Wort)
-   "to got her" (plus Alternative für jedes Wort)
-   "together" (plus Alternative für das Wort)

In diesem Fall kann eine Erkennung die folgende Lattice-Struktur erstellen.

![Lattice-Struktur für das Wort "zusammen"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Jede Spalte hat die gleiche Strichreihenfolge, da sie alle auf die gleiche [InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) verweisen.

 

 

 
