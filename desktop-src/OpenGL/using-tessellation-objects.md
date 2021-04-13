---
title: Verwenden von Mosaik Objekten
description: Wenn ein komplexes Polygon beschrieben und im Mosaik Prozess verwendet wird, werden zugeordnete Daten, wie z. b. die Scheitel Punkte, Kanten und Rückruf Funktionen, benötigt.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- OpenGL-Hilfsprogramm (GLU), Mosaik Objekte
- GLU (OpenGL-Hilfsprogramm), Mosaik Objekte
- Mosaik Objekte OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309639"
---
# <a name="using-tessellation-objects"></a>Verwenden von Mosaik Objekten

Wenn ein komplexes Polygon beschrieben und im Mosaik Prozess verwendet wird, werden zugeordnete Daten, wie z. b. die Scheitel Punkte, Kanten und Rückruf Funktionen, benötigt. Alle diese Daten sind an ein einzelnes Mosaik Objekt gebunden. Zum Mosaik eines Polygons verwenden Sie zunächst die [**glunewtess**](glunewtess.md) -Funktion, die ein neues Mosaik Objekt erstellt und einen Zeiger darauf zurückgibt. Wenn die Funktion fehlschlägt, wird ein NULL-Zeiger zurückgegeben.

Wenn Sie kein Mosaik Objekt mehr benötigen, können Sie es löschen und den gesamten zugeordneten Arbeitsspeicher mit " [**gludeletetess**](gludeletetess.md)" freigeben.

Sie können ein einzelnes Mosaik Objekt für alle Mosaik Vorgänge wieder verwenden. Dieses Objekt ist nur erforderlich, da Bibliotheksfunktionen möglicherweise eigene Mosaik Vorgänge durchführen müssen, und Sie sollten dies tun können, ohne dass sich dies auf das von Ihrem Programm durch zuführte Mosaik beeinträchtigt. Mehrere Mosaik Objekte sind ebenfalls nützlich, wenn Sie unterschiedliche Sätze von Rückrufen für verschiedene Mosaik Vorgänge verwenden möchten. In der Regel weisen Sie jedoch ein einzelnes Mosaik Objekt zu und verwenden es für alle Mosaik Vorgänge. Es ist nicht erforderlich, es freizugeben, da es eine kleine Menge an Arbeitsspeicher verwendet. Wenn Sie dagegen eine Bibliotheksfunktion schreiben, die das-Mosaik verwendet, achten Sie darauf, dass Sie alle erstellten Mosaik Objekte freigeben.

 

 




