---
title: VML AutoRotationCenter-Attribut
description: VML AutoRotationCenter-Attribut
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54b363b34a6b2f943be45d457e252eebcf597afd7f82b7992cf151b0c2eda4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347102"
---
# <a name="vml-autorotationcenter-attribute"></a>VML AutoRotationCenter-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob der Mittelpunkt der Drehung der geometrische Mittelpunkt derExtrusion ist. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *element* autorotationcenter=" *expression* ">

**Skriptsyntax**

*element* .autorotationcenter="*expression*"

*expression* = *Element*.autorotationcenter

**Anmerkungen**

Der geometrische Mittelpunkt einer polygonierten Form ist 0,0,0. Wenn der Wert dieses Attributs **False ist,** wird der Mittelpunkt der Drehung durch das [RotationCenter-Attribut](msdn-online-vml-rotationcenter-attribute.md) bestimmt. Der Standardwert ist **False**.

*Microsoft Office Extensions-Attribut*

 

 