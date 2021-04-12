---
title: VML regroupid-Attribut
description: VML regroupid-Attribut
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390432"
---
# <a name="vml-regroupid-attribute"></a>VML regroupid-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine vorherige Gruppe für eine Form. Lese-/Schreibzugriff. **Vginteger**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:regroupid = " *Expression* " >

**Anmerkungen**

Eine ID-Nummer wird verwendet, um Gruppen von Formen zu identifizieren, die nicht mehr gruppiert sind. Ermöglicht das programmgesteuerte erneute Gruppieren von Formen.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form war Teil einer Gruppe, die durch die Gruppen-ID 040754 gekennzeichnet ist.


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 