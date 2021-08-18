---
description: Das Divider-Objekt bietet Zugriff auf die Layoutanalysefeatures für Tablet-PCs.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Arbeiten mit dem Divider-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a31c7ab0c99c0ac4007abe164a887694c8e41fb8c8892dfe2637efaf25b10f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966569"
---
# <a name="working-with-the-divider-object"></a>Arbeiten mit dem Divider-Objekt

Das [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) bietet Zugriff auf die Layoutanalysefeatures für Tablet-PCs.

In verwaltetem Code kann das [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) instanziiert werden, indem einer der [Divider-Konstruktoren](/previous-versions/ms839465(v=msdn.10)) aufgerufen wird. In Automation wird dies als [**InkDivider-Objekt**](inkdivider-class.md) bezeichnet und kann instanziiert werden, indem die [**CoCreateInstance-Methode**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ aufgerufen wird.

Sie können eine Momentaufnahme des aktuellen Analyseergebnisses abrufen, indem Sie die [Divide-Methode](/previous-versions/ms839461(v=msdn.10)) des [Divider-Objekts](/previous-versions/ms583616(v=vs.100)) aufrufen. Das Analyseergebnis wird in einem [DivisionResult-Objekt](/previous-versions/ms839371(v=msdn.10)) zurückgegeben. Jedes Mal, wenn Sie die Divide-Methode aufrufen, erstellt das Divider-Objekt ein DivisionResult-Objekt. Weitere Informationen zum DivisionResult-Objekt finden Sie unter [Arbeiten mit dem DivisionResult-Objekt.](working-with-the-divisionresult-object.md)

Die Vom [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) [analysierte Strokes-Auflistung](/previous-versions/ms552701(v=vs.100)) ist in der [Strokes-Eigenschaft](/previous-versions/ms839422(v=msdn.10)) des Divider-Objekts enthalten. Das Divider-Objekt analysiert die Strokes-Auflistung dynamisch, wenn Sie der Auflistung hinzufügen oder diese löschen. Weitere Informationen zur Strokes-Eigenschaft des Divider-Objekts finden Sie unter [Working with a Strokes Collection](working-with-a-strokes-collection.md).

Das [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) verwendet einen Erkennungskontext, um die Analyse von Erkennungssegmenten zu verbessern und Erkennungstext für Handschriftelemente zu generieren. Sie können den Erkennungskontext mithilfe der [RecognizerContext-Eigenschaft](/previous-versions/ms839415(v=msdn.10)) des Divider-Objekts festlegen. Die RecognizerContext-Eigenschaft kann nicht mehr geändert werden, nachdem dem Divider-Objekt Striche zugewiesen wurden. Weitere Informationen zur RecognizerContext-Eigenschaft des Divider-Objekts finden Sie unter [Working with a Recognizer Context](working-with-a-recognizer-context.md).

> [!Caution]  
> In verwaltetem Code müssen Sie die [Dispose-Methode](/previous-versions/ms839450(v=msdn.10)) für dieses Objekt aufrufen, bevor es den Gültigkeitsbereich übergibt. Dieses Objekt verwaltet nicht verwaltete Ressourcen. Die Verwendung der Finalisierung für dieses Objekt kann zu Speicherverlusten und Ausnahmen in Ihrer Anwendung führen.

 

 

 
