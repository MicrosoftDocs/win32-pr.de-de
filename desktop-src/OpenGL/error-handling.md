---
title: Fehlerbehandlung (OpenGL)
description: Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode aufgezeichnet.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- Fehlerbehandlung für OpenGL
- OpenGL-Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064330859b4e6b6d2d0bb9985e9f24d968a7daa5062215c64e82f89563ae06ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361380"
---
# <a name="error-handling-opengl"></a>Fehlerbehandlung (OpenGL)

Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode aufgezeichnet. Die Funktion, die den Fehler verursacht hat, wird ignoriert, sodass sie keine Auswirkungen auf den OpenGL-Zustand oder den Framepufferinhalt hat. (Wenn der aufgezeichnete Fehler GL \_ war NICHT \_ GENÜGEND \_ ARBEITSSPEICHER, die Ergebnisse der Funktion sind jedoch nicht definiert.) Nach der Aufzeichnung wird der aktuelle Fehlercode erst gelöscht, wenn Sie die [**GlGetError-Abfragefunktion**](glgeterror.md) aufrufen, die den aktuellen Fehlercode zurückgibt.

Implementierungen von OpenGL geben möglicherweise mehrere aktuelle Fehlercodes zurück, von denen jeder bis zur Abfrage festgelegt bleibt. Die **glGetError-Funktion** gibt GL NO ERROR zurück, \_ nachdem Sie alle \_ aktuellen Fehlercodes abgefragt haben oder wenn kein Fehler vorliegt. Wenn Sie einen Fehlercode erhalten, rufen Sie **daher glGetError** auf, bis GL \_ NO ERROR zurückgegeben \_ wird, um sicherzustellen, dass Sie alle Fehler ermittelt haben. Eine Liste der Fehlercodes finden Sie unter [OpenGL-Fehlercodes.](opengl-error-codes.md)

Sie können die [**gluErrorString**](gluerrorstring.md) GLU-Funktion verwenden, um eine beschreibende Zeichenfolge zu erhalten, die dem übergebenen Fehlercode entspricht. Weitere Informationen zu **gluErrorString** finden Sie unter [Behandeln von Fehlern.](handling-errors.md)

> [!Note]  
> GLU-Funktionen geben häufig Fehlerwerte zurück, wenn ein Fehler erkannt wird. Außerdem definiert die OpenGL-Hilfsprogrammbibliothek die Fehlercodes GLU \_ INVALID \_ ENUM, GLU \_ INVALID VALUE und GLU OUT OF \_ \_ \_ \_ MEMORY, die die gleiche Bedeutung wie die zugehörigen OpenGL-Fehlercodes haben.

 

 

 




