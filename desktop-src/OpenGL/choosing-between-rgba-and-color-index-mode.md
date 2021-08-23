---
title: Auswählen zwischen RGBA und Color-Index Modus
description: Verwenden Sie im Allgemeinen den RGBA-Modus für Ihre OpenGL-Anwendungen. Sie bietet mehr Flexibilität als der Farbindexmodus für Effekte wie Schattierung, Beleuchtung, Farbzuordnung, Blending, Antialiasing und Blending.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL im Windows,RGBA-Modus
- OpenGL im Windows,Farbindexmodus
- RGBA-Modus OpenGL
- Farbindexmodus OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa78096369ec9ba01d6e0dcd3d67535a0d368ef7a5018d3679f9f64dcdf74d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554630"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Auswählen zwischen RGBA und Color-Index Modus

Verwenden Sie im Allgemeinen den RGBA-Modus für Ihre OpenGL-Anwendungen. Sie bietet mehr Flexibilität als der Farbindexmodus für Effekte wie Schattierung, Beleuchtung, Farbzuordnung, Blending, Antialiasing und Blending.

Verwenden Sie in den folgenden Fällen den Farbindexmodus:

-   Wenn Eine begrenzte Anzahl von Bitebenen verfügbar ist, der Farbindexmodus kann eine weniger grobe Schattierung als der RGBA-Modus erzeugen.
-   Wenn Sie keine Bedenken hinsichtlich der Verwendung von "echten" Farben haben, Verwenden Sie beispielsweise mehrere Farben in einer topografischen Karte, um relative Erhöhungen festzulegen.
-   Wenn Sie eine vorhandene Anwendung portieren, die den Farbindexmodus umfassend verwendet.
-   Wenn Sie Farbzuordnungsanimation und Effekte in Ihrer Anwendung verwenden möchten. (Dies ist auf Geräten mit echter Farbe nicht möglich.)

 

 




