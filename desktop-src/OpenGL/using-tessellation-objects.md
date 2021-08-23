---
title: Verwenden von Mosaikobjekten
description: Da ein komplexes Polygon beschrieben und mosaikiert wird, sind zugeordnete Daten erforderlich, z. B. scheiteltische Ränder und Rückruffunktionen.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- OpenGL-Hilfsprogramm (GLU), Mosaikobjekte
- GLU (OpenGL-Hilfsprogramm), Mosaikobjekte
- Mosaikobjekte OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc2ca11fd037f79a88fed1568c97a24692060d723327cde0c8e8842ed21d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011898"
---
# <a name="using-tessellation-objects"></a>Verwenden von Mosaikobjekten

Da ein komplexes Polygon beschrieben und mosaikiert wird, sind zugeordnete Daten erforderlich, z. B. scheiteltische Ränder und Rückruffunktionen. Alle diese Daten sind an ein einzelnes Mosaikobjekt gebunden. Um ein Polygon zu mosaiken, verwenden Sie zunächst die [**gluNewTess-Funktion,**](glunewtess.md) die ein neues Mosaikobjekt erstellt und einen Zeiger darauf zurückgibt. Ein NULL-Zeiger wird zurückgegeben, wenn die Funktion fehlschlägt.

Wenn Sie ein Mosaikobjekt nicht mehr benötigen, können Sie es löschen und den zugeordneten Arbeitsspeicher mit [**gluDeleteTess frei geben.**](gludeletetess.md)

Sie können ein einzelnes Mosaikobjekt für alle Mosaiken wiederverwenden. Dieses Objekt ist nur erforderlich, da Bibliotheksfunktionen möglicherweise ihre eigenen Mosaiken ausführen müssen, und sie sollten dies ohne Beeinträchtigung des Mosaiks des Programms tun können. Mehrere Mosaikobjekte sind auch nützlich, wenn Sie verschiedene Sätze von Rückrufen für verschiedene Mosaiken verwenden möchten. In der Regel ordnen Sie jedoch ein einzelnes Mosaikobjekt zu und verwenden es für alle Mosaike. Es ist nicht wirklich notwendig, es frei zu geben, da es eine kleine Menge an Arbeitsspeicher verwendet. Wenn Sie hingegen eine Bibliotheksfunktion schreiben, die das GLU-Mosaik verwendet, müssen Sie darauf achten, alle von Ihnen erstellten Mosaikobjekte frei zu geben.

 

 




