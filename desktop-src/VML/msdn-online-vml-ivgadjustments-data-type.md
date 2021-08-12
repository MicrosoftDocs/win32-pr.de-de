---
title: VML IVgAdjustments-Datentyp
description: VML IVgAdjustments-Datentyp
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed6512e36e9621d010e8875eec3190fa81524b4947a30f14364199341d18c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599678"
---
# <a name="vml-ivgadjustments-data-type"></a>VML IVgAdjustments-Datentyp

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Auflistung von Anpassungen an einer Form, die in Formeln verwendet werden kann. Anpassungen können als temporäre Platzhalter oder aus einem beliebigen Grund verwendet werden, aus dem Sie Variablen verwenden würden. Es gibt nur 8 Anpassungen in der Auflistung.



| Attribute | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Länge     | **Integer**. Anzahl der Anpassungen. Darf nicht größer als 8 sein.                                                                                                                                                                                                                                                                          |
| Element       | **Long**. Array von Anpassungen, indiziert von 0 bis 7. Beachten Sie, dass Anpassungen möglicherweise nur selten angegeben werden. Das heißt, zwischengeschaltete Arraywerte werden möglicherweise nicht immer ausgefüllt. Beispielsweise können die Elemente 1, 3 und 5 Werte für die Länge 3 aufweisen, wobei item(0), item(2) und item(4) angegeben sind. Um festzustellen, ob ein Element vorhanden ist, verwenden Sie das Exists-Attribut. |
| Exists     | **IVgTriState**. Bestimmt, ob eine angegebene Anpassung vorhanden ist. Beachten Sie, dass ein Index verwendet werden muss. das heißt, exists(item) muss verwendet werden, um das Vorhandensein eines Elements abzurufen.                                                                                                                                                           |
| Wert      | **Zeichenfolge**. Textdarstellung numerischer Werte mit Kommas zwischen den einzelnen Zahlen.                                                                                                                                                                                                                                                    |



 

 

 