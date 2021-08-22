---
title: VML ConnectType-Attribut
description: VML ConnectType-Attribut
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76910977c0673500be2e91d9f387b1e61782a1460e5de0d513784caa6f0f1633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999260"
---
# <a name="vml-connecttype-attribute"></a>VML ConnectType-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Typ der Verbindungspunkte, die zum Anfügen von Formen an andere Formen verwendet werden. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *element* o:connecttype=" *ausdruck* ">

**Anmerkungen**

Mögliche Werte:



| Wert    | Beschreibung                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| Keine     | Keine Verbindungsstandorte. Standard.                                                                                                         |
| rect     | Vier Standardverbindungspunkte an den Mittelpunkten der oberen, unteren, linken und rechten Seite.                                                   |
| Segmente | Die Bearbeitungspunkte der Form werden verwendet. Bearbeitungspunkte sind die schwarzen Punkte in einem grafischen Editor, die zum Auswählen von Teilen einer Form verwendet werden. |
| custom   | Ein benutzerdefiniertes Array von Verbindungsspeicherorten.                                                                                               |



 

*Microsoft Office Extensions-Attribut*

 

 