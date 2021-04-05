---
title: OpenGL-Funktionsnamen
description: Viele OpenGL-Funktionen sind Variationen voneinander und unterscheiden sich hauptsächlich von den Datentypen ihrer Argumente.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, Funktionsnamen
- Funktionsnamen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710607"
---
# <a name="opengl-function-names"></a>OpenGL-Funktionsnamen

Viele OpenGL-Funktionen sind Variationen voneinander und unterscheiden sich hauptsächlich von den Datentypen ihrer Argumente. Einige Funktionen unterscheiden sich in der Anzahl der verknüpften Argumente und ob diese Argumente als Vektor oder separat in einer Liste angegeben werden können. Wenn Sie z. b. die **glVertex2f** -Funktion verwenden, müssen Sie x-und y-Koordinaten als 32-Bit-Gleit Komma Zahlen angeben. mit **glVertex3sv** müssen Sie ein Array von drei kurzen (16-Bit-) ganzzahligen Werten für x, y und z angeben. In den folgenden Themen wird nur der Basisname der Funktion verwendet. Ein Sternchen gibt an, dass möglicherweise mehr für den eigentlichen Funktionsnamen vorhanden ist, als angezeigt wird. Beispielsweise steht ["glVertex \*](glvertex-functions.md) " für alle Variationen der Funktion, mit der Vertices angegeben werden: **glVertex2d**, **glVertex2f**, **glVertex2i** usw.

Die Auswirkung einer OpenGL-Funktion kann variieren, je nachdem, ob bestimmte Modi aktiviert sind. Beispielsweise müssen Sie die Beleuchtung aktivieren, wenn die Beleuchtungs bezogenen Funktionen ein ordnungsgemäß beleuchtetes Objekt bilden. Um einen bestimmten Modus zu aktivieren, verwenden Sie die Funktion [**glEnable**](glenable.md) , und geben Sie die entsprechende Konstante an, um den Modus zu identifizieren (z. b. gl- \_ Beleuchtung). Um einen Modus zu deaktivieren, verwenden Sie [**gldeaktiviert**](gldisable.md). Eine komplette Liste der Modi, die aktiviert werden können, finden Sie unter **glEnable** .

 

 




