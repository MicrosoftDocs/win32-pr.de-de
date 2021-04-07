---
title: VML-Attribut "invx"
description: VML-Attribut "invx"
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728073"
---
# <a name="vml-invx-attribute"></a>VML-Attribut "invx"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die x-Position des Handles invertiert ist. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))

**Tagsyntax**

<v: *Element* invx = " *Expression* " >

**Anmerkungen**

**True** gibt an, dass die x-Position des Handles invertiert wird, indem der x-Wert vom x-Wert von **coordorigin** subtrahieren wird, der dem x-Wert von **coordsize** hinzugefügt wird. Der Standardwert ist **False**.

Dieses Attribut entspricht

coordorigin. x + coordsize. x-h. Position. x

*VML-Standard Attribut*

 

 