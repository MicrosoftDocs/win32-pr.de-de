---
title: VML ivganpassungen-Datentyp
description: VML ivganpassungen-Datentyp
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29f85f93218db098ca247fa66b1f493e9c622a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473436"
---
# <a name="vml-ivgadjustments-data-type"></a>VML ivganpassungen-Datentyp

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Sammlung von Anpassungen einer Form, die in Formeln verwendet werden kann. Anpassungen können als temporäre Platzhalter verwendet werden, oder Sie können aus irgendeinem Grund Variablen verwenden. Es gibt nur 8 Anpassungen in der Sammlung.



| Attribute | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Länge     | **Integer**. Anzahl der Anpassungen. Darf nicht größer als 8 sein.                                                                                                                                                                                                                                                                          |
| Element       | **Long**. Ein Array von Anpassungen, die von 0 bis 7 indiziert wurden. Beachten Sie, dass die Anpassungen möglicherweise sparsam angegeben werden. Das heißt, zwischen Array Werte können nicht immer ausgefüllt werden. Beispielsweise können Element 1, 3 und 5 Werte für eine Länge von 3 aufweisen, wobei Item (0), Item (2) und Item (4) angegeben sind. Um festzustellen, ob ein Element vorhanden ist, verwenden Sie das vorhanden sein-Attribut. |
| Exists     | **Ivgtrstate**. Bestimmt, ob eine angegebene Anpassung vorhanden ist. Beachten Sie, dass ein Index verwendet werden muss. Das heißt, "vorhanden" (Element) muss verwendet werden, um das vorhanden sein eines Elements abzurufen.                                                                                                                                                           |
| Wert      | **Zeichenfolge**. Text Darstellung numerischer Werte mit Kommas zwischen den einzelnen Zahlen.                                                                                                                                                                                                                                                    |



 

 

 