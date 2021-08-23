---
description: Dieser Abschnitt enthält die Kernfunktionen für Tablet PC.
ms.assetid: 8f94a82c-de93-4649-a9b5-0adcbe01333d
title: Pc-Kernfunktionen für Tablets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb9e58300321f2b483cc062472950f5d252a292dc1380b3e5c030993ddbe6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967543"
---
# <a name="core-tablet-pc-functions"></a>Pc-Kernfunktionen für Tablets

Dieser Abschnitt enthält die Kernfunktionen für Tablet PC.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                         | BESCHREIBUNG                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddOneStroke**](addonestroke.md)                             | Fügt dem [**übergebenen InkDivider-Objekt**](inkdivider-class.md) ein neues [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) hinzu.                                                                 |
| [**CallDivide**](calldivide.md)                                 | Ruft Analyseinformationen aus dem [**InkDivider-Objekt**](inkdivider-class.md) ab.                                                                                                              |
| [**CallDivideResults**](calldivideresults.md)                   | Gibt Analyseergebnisse aus dem [**InkDivider-Objekt**](inkdivider-class.md) zurück.                                                                                                                    |
| [**CallDivideResultsStrokeIds**](calldivideresultsstrokeids.md) | Ruft die [**Id-Eigenschaften**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) für die [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) des entsprechenden Worts, der Zeile, des Absatzes oder der Zeichnung ab, die von der Freihandanalyse bestimmt werden. |
| [**CreateInkDivider**](createinkdivider.md)                     | Instanziiert eine Implementierung der [**InkDivider-Schnittstelle**](inkdivider-class.md) und gibt ihr Handle zurück.                                                                                      |
| [**DeleteInkDivider**](deleteinkdivider.md)                     | Löscht ein [**InkDivider-Objekt**](inkdivider-class.md) und gibt zugeordnete Ressourcen frei.                                                                                                         |
| [**InvokeIDispatch**](invokeidispatch.md)                       | Ruft die Hilfsfunktionen für die IDispatch-Schnittstelle auf.                                                                                                                                           |
| [**RecognizerContextSet**](recognizercontextset.md)             | Testet, ob das [**InkDivider-Objekt**](inkdivider-class.md) die [**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md) zum Analysieren von Wörtern verwenden kann.                                      |
| [**RemoveStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-removestrokes)                | Entfernt [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aus [**inkDivider**](inkdivider-class.md).                                                                                           |
| [**SetLineHeight**](setlineheight.md)                           | Legt die [**LineHeight-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) für das [**InkDivider-Objekt**](inkdivider-class.md) fest.                                                                                 |
| [**SetLineRecoCallback**](setlinerecocallback.md)               | Legt eine Rückruffunktion fest, die während der Zeilenerkennung verwendet werden soll.                                                                                                                                        |



 

 

 
