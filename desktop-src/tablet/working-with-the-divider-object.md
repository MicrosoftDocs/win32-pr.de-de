---
description: Das Divider-Objekt ermöglicht den Zugriff auf die Features der Tablet PC-Layoutanalyse.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Arbeiten mit dem Divider-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd158f85d368d764bce17e8b481ebe625a4d6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356741"
---
# <a name="working-with-the-divider-object"></a>Arbeiten mit dem Divider-Objekt

Das [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt ermöglicht den Zugriff auf die Features der Tablet PC-Layoutanalyse.

In verwaltetem Code kann das [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt instanziiert werden, indem einer der [Divider](/previous-versions/ms839465(v=msdn.10)) -Konstruktoren aufgerufen wird. In Automation wird dies als [**InkDivider**](inkdivider-class.md) -Objekt bezeichnet und kann durch Aufrufen der [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Sie können eine Momentaufnahme des aktuellen Analyse Ergebnisses abrufen, indem Sie die [Divide](/previous-versions/ms839461(v=msdn.10)) -Methode des [Divider](/previous-versions/ms583616(v=vs.100)) -Objekts aufrufen. Das Analyseergebnis wird in einem [DivisionResult](/previous-versions/ms839371(v=msdn.10)) -Objekt zurückgegeben. Jedes Mal, wenn Sie die Divide-Methode aufrufen, erstellt das Divider-Objekt ein DivisionResult-Objekt. Weitere Informationen zum DivisionResult-Objekt finden Sie unter [Arbeiten mit dem DivisionResult-Objekt](working-with-the-divisionresult-object.md).

Die [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung, die das [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt analysiert, ist in der [Striche](/previous-versions/ms839422(v=msdn.10)) -Eigenschaft des Divider-Objekts enthalten. Das untergeordnete Objekt analysiert die Striche-Auflistung dynamisch, wenn Sie Sie der Auflistung hinzufügen oder daraus löschen. Weitere Informationen über die Strokes-Eigenschaft des Divider-Objekts finden Sie unter [Working with a Striche Collection](working-with-a-strokes-collection.md).

Das [Divider](/previous-versions/ms583616(v=vs.100)) -Objekt verwendet einen Erkennungs Kontext, um die Analyse der Erkennungs Segmente zu verbessern und Erkennungs Text für Handschrift Elemente zu generieren. Sie können den Erkennungs Kontext mithilfe der [erkennzercontext](/previous-versions/ms839415(v=msdn.10)) -Eigenschaft des Divider-Objekts festlegen. Die erkenzercontext-Eigenschaft kann nicht geändert werden, nachdem dem Divider-Objekt Striche zugewiesen wurden. Weitere Informationen zur erkenzercontext-Eigenschaft des Divider-Objekts finden Sie unter [Working with a erkenzer Context](working-with-a-recognizer-context.md).

> [!Caution]  
> In verwaltetem Code [muss die verwerfen](/previous-versions/ms839450(v=msdn.10)) -Methode für dieses Objekt aufgerufen werden, bevor es den Gültigkeitsbereich verlässt. Dieses Objekt verwaltet nicht verwaltete Ressourcen. Die Verwendung des Abschluss für dieses Objekt kann zu Speicher Verlusten und Ausnahmen in der Anwendung führen.

 

 

 
