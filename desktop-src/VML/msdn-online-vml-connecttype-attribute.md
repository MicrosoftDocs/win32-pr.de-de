---
title: VML connecttype-Attribut
description: VML connecttype-Attribut
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101663"
---
# <a name="vml-connecttype-attribute"></a>VML connecttype-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Typ der Verbindungspunkte, die zum Anfügen von Formen an andere Formen verwendet werden. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* o:connecttype = " *Ausdruck* " >

**Anmerkungen**

Mögliche Werte:



| Wert    | BESCHREIBUNG                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| none     | Keine Verbindungs Standorte. Standard.                                                                                                         |
| rect     | Standard vier Verbindungspunkte in Mittelpunkten von oben, unten, Links und rechts.                                                   |
| Segmente | Die Bearbeitungspunkte der Form werden verwendet. Bearbeitungspunkte sind die schwarzen Punkte in einem grafischen Editor, die verwendet werden, um Teile einer Form auszuwählen. |
| custom   | Ein benutzerdefiniertes Array von Verbindungs Standorten.                                                                                               |



 

*Microsoft Office Extensions-Attribut*

 

 