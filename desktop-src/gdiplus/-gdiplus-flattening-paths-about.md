---
description: Ein GraphicsPath-Objekt speichert eine Sequenz von Linien und B&\# 233; Zier-Splines.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Vereinfachen von Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987901"
---
# <a name="flattening-paths"></a>Vereinfachen von Pfaden

Ein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt speichert eine Sequenz von Linien und Bézier-Splines. Sie können einem Pfad mehrere Arten von Kurven (Ellipsen, Arcs, kardinale Splines) hinzufügen, aber jede Kurve wird in eine Bézier-Spline konvertiert, bevor Sie im Pfad gespeichert wird. Das Vereinfachen eines Pfads besteht darin, jede Bézier-Spline im Pfad in eine Sequenz von geraden Zeilen umzuwandeln.

Um einen Pfad zu vereinfachen, nennen Sie die [**GraphicsPath:: vereinfachen**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) -Methode eines [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekts. Die **GraphicsPath:: Flatten** -Methode empfängt ein flatdo-Argument, das den maximalen Abstand zwischen dem vereinfachten Pfad und dem ursprünglichen Pfad angibt. Die folgende Abbildung zeigt einen Pfad vor und nach der Vereinfachung.

![Abbildung, die eine Sequenz von verbundenen Bézier-Splines in blau und den entsprechenden roten Zeilen anzeigt](images/aboutgdip02-art32a.png)

 

 



