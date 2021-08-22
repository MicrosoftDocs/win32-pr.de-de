---
title: VML ShapeType-Element
description: VML ShapeType-Element
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0632919a141ae04f80b0b6cd6782ea907aa8cfe1d720e599964110c038f3998e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099090"
---
# <a name="vml-shapetype-element"></a>VML ShapeType-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Form, die zum Erstellen anderer Formen verwendet werden kann.

Das folgende Attribut ändert einen **ShapeType.**



| attribute                                      | BESCHREIBUNG                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Master](msdn-online-vml-master-attribute.md) | Bestimmt, ob ein **ShapeType** ein Masterelement ist. |



 

**Anmerkungen**

**ShapeType** ist mit dem **Shape-Element** identisch, es sei denn, es kann nicht auf ein anderes **ShapeType-Element** verwiesen werden.

Wenn ein **Shape-Element** auf einen **ShapeType** verweist, dupliziert die **Form** möglicherweise einige der Eigenschaften, die bereits im **ShapeType** angegeben wurden. In diesen Fällen überschreiben die Attribute in der **Form** die Attribute des **ShapeType**.

Das **Type-Attribut** darf nicht mit **ShapeType** verwendet werden.

CSS-Positionierungsattribute (z.B. **Top,** **Left** usw.) werden nicht von einem **ShapeType** an eine **Form** übergeben.

Um dieses Element zu verwenden, erstellen Sie einen **ShapeType** mit einem bestimmten [ID-Attribut.](id-attribute--vml.md) Erstellen Sie dann eine **Form,** und verweisen Sie mit dem **Type-Attribut** auf **shapeType.** Weitere Informationen finden Sie unter [Type-Attribut.](type-attribute--shape--vml.md)

 

 