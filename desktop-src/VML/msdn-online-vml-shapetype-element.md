---
title: VML ShapeType-Element
description: VML ShapeType-Element
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209254"
---
# <a name="vml-shapetype-element"></a>VML ShapeType-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine Form, die zum Erstellen anderer Formen verwendet werden kann.

Das folgende Attribut ändert einen **ShapeType**.



| Attribut                                      | BESCHREIBUNG                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Master](msdn-online-vml-master-attribute.md) | Bestimmt, ob ein **ShapeType** ein Master Element ist. |



 

**Anmerkungen**

**ShapeType** ist mit dem **Shape** -Element identisch, außer es kann nicht auf ein anderes **ShapeType** -Element verweisen.

Wenn ein **Shape** -Element auf einen **ShapeType** verweist, kann die **Form** einige der Eigenschaften duplizieren, die bereits im **ShapeType** angegeben wurden. In diesen Fällen überschreiben die Attribute in der **Form** die Attribute des **ShapeType**.

Das **Type** -Attribut darf nicht mit **ShapeType** verwendet werden.

CSS-Positionierungs Attribute (z. b. " **Top**", " **left**" usw.) werden nicht aus einem **ShapeType** an eine **Form** weitergegeben.

Um dieses Element zu verwenden, erstellen Sie einen **ShapeType** mit einem bestimmten [ID](id-attribute--vml.md) -Attribut. Erstellen Sie dann eine **Form** , und verweisen Sie auf den **ShapeType** mit dem **Type** -Attribut. Weitere Informationen finden Sie unter dem [Type](type-attribute--shape--vml.md) -Attribut.

 

 