---
description: Einführung in die Verwendung von Steuerelementen ohne Beschriftungseigenschaften für den Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Steuerelemente ohne Beschriftungseigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5cd8eb0c87f946d8540fb63d75408dcf98a880cefcd1ba295ba2ba113e6828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774110"
---
# <a name="controls-without-caption-properties"></a>Steuerelemente ohne Beschriftungseigenschaften

Wenn ein Steuerelement nicht über eine eigene Beschriftungseigenschaft verfügt, führen Sie die folgenden Schritte aus, um sicherzustellen, dass die Steuerelemente durch Barrierefreiheitshilfen identifiziert werden können:

-   Erstellen Sie ein statisches Textsteuerelement mit einem aussagekräftigen und beschreibenden Namen.
-   Platzieren Sie die statische Bezeichnung so, dass sie unmittelbar vor dem Steuerelement, auf das verwiesen wird, in der Tabulatorreihenfolge angezeigt wird.
-   Stellen Sie sicher, dass der Bezeichnungstext mit einem Doppelpunkt endet, z.B. "Einstellungen:".
-   Positionieren Sie den Bezeichnungstext unmittelbar links oder vor dem Steuerelement, auf das verwiesen wird.
-   Machen Sie den statischen Text unsichtbar, wenn er nicht für die visuelle Anzeige geeignet ist. Weisen Sie hierzu das entsprechende Attribut im Ressourcenskript zu. Dies kann geeignet sein, wenn der Name oder die Funktion eines Steuerelements visuell mit anderen Mitteln als statischem Textsteuerelement bereitgestellt wird, z. B. einer Grafik oder einem zugehörigen Optionsfeld.

Die ordnungsgemäße Verwendung statischer Steuerelemente ist die einzige Möglichkeit, unterstrichene Zugriffsschlüssel für Steuerelemente ohne systeminterne Bezeichnungen ordnungsgemäß zu implementieren. Weitere Informationen zur Verwendung von Steuerelementen ohne Beschriftungseigenschaften finden Sie im Abschnitt [Barrierefreiheit.](/windows/desktop/accessibility)

 

 
