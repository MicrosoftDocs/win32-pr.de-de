---
title: OpenGL-Funktionsnamen
description: Viele OpenGL-Funktionen sind Variationen voneinander, die sich größtenteils in den Datentypen ihrer Argumente unterscheiden.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, Funktionsnamen
- Funktionsnamen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7729ca1f8a092c261a2ae87a835b51ea253ff2d09de710a830458c0825642bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936880"
---
# <a name="opengl-function-names"></a>OpenGL-Funktionsnamen

Viele OpenGL-Funktionen sind Variationen voneinander, die sich größtenteils in den Datentypen ihrer Argumente unterscheiden. Einige Funktionen unterscheiden sich in der Anzahl der verknüpften Argumente und darin, ob diese Argumente als Vektor angegeben werden können oder separat in einer Liste angegeben werden müssen. Wenn Sie beispielsweise die **glVertex2f-Funktion** verwenden, müssen Sie x- und y-Koordinaten als 32-Bit-Gleitkommazahlen angeben. mit **glVertex3sv** müssen Sie ein Array von drei kurzen (16-Bit)-Ganzzahlwerten für x, y und z angeben. In den folgenden Themen wird nur der Basisname der Funktion verwendet. Ein Sternchen gibt an, dass der tatsächliche Funktionsname möglicherweise mehr enthält, als angezeigt wird. Beispielsweise steht [glVertex \*](glvertex-functions.md) für alle Variationen der Funktion, die Sie zum Angeben von Scheitelpunkten verwenden: **glVertex2d,** **glVertex2f,** **glVertex2i** usw.

Die Auswirkung einer OpenGL-Funktion kann variieren, je nachdem, ob bestimmte Modi aktiviert sind. Beispielsweise müssen Sie die Beleuchtung aktivieren, wenn die beleuchtungsbezogenen Funktionen ein ordnungsgemäß helles Objekt erzeugen sollen. Verwenden Sie zum Aktivieren eines bestimmten Modus die [**GlEnable-Funktion,**](glenable.md) und geben Sie die entsprechende Konstante an, um den Modus zu identifizieren (z. B. GL \_ LIGHTING). Um einen Modus zu deaktivieren, verwenden [**Sie glDisable**](gldisable.md). Eine vollständige Liste der Modi, die aktiviert werden können, finden Sie unter **glEnable.**

 

 




