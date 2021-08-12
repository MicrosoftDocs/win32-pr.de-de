---
title: VML-InvX-Attribut
description: VML-InvX-Attribut
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e040c4ff013ec9c2a606e1034458f9149d666813dd42341d9ec68a39901094b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600126"
---
# <a name="vml-invx-attribute"></a>VML-InvX-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die x-Position des Handles invertiert wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))

**Tagsyntax**

<v: *element* invx=" *ausdruck* ">

**Anmerkungen**

**True** gibt an, dass die x Position des Handles umgekehrt wird, indem der x-Wert vom x-Wert von **CoordOrigin** subtrahiert wird, der dem x-Wert von **CoordSize** hinzugefügt wurde. Der Standardwert ist **False**.

Dieses Attribut entspricht

coordorigin.x + coordsize.x – h.position.x

*VML-Standardattribut*

 

 