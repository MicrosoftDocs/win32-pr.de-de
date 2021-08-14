---
title: Fehlerbehandlung (OpenGL)
description: Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode erfasst.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- Fehlerbehandlung bei OpenGL
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

Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode erfasst. Die Funktion, die den Fehler verursacht hat, wird ignoriert, sodass sie keine Auswirkungen auf den OpenGL-Zustand oder den Framebuffer-Inhalt hat. (Wenn der aufgezeichnete Fehler GL war \_ OUT \_ OF MEMORY sind die Ergebnisse der Funktion jedoch nicht \_ definiert.) Nach der Aufzeichnung wird der aktuelle Fehlercode erst dann wiedergerufen, wenn Sie die [**abfragefunktion glGetError**](glgeterror.md) aufrufen, die den aktuellen Fehlercode zurückgibt.

Implementierungen von OpenGL geben möglicherweise mehrere aktuelle Fehlercodes zurück, die jeweils bis zur Abfrage festgelegt bleiben. Die **glGetError-Funktion** gibt GL NO ERROR zurück, nachdem Sie alle aktuellen Fehlercodes abgefragt haben oder \_ kein Fehler aufgetreten \_ ist. Wenn Sie einen Fehlercode erhalten, rufen Sie **daher glGetError** auf, bis GL NO ERROR zurückgegeben wird, um sicherzustellen, dass Sie alle \_ Fehler gefunden \_ haben. Eine Liste der Fehlercodes finden Sie unter [OpenGL-Fehlercodes.](opengl-error-codes.md)

Sie können die [**GLU-Funktion gluErrorString**](gluerrorstring.md) verwenden, um eine beschreibende Zeichenfolge zu erhalten, die dem übergebenen Fehlercode entspricht. Weitere Informationen zu **gluErrorString finden Sie** unter [Behandeln von Fehlern.](handling-errors.md)

> [!Note]  
> GLU-Funktionen geben häufig Fehlerwerte zurück, wenn ein Fehler erkannt wird. Außerdem definiert die OpenGL-Hilfsprogrammbibliothek die Fehlercodes GLU INVALID ENUM, GLU INVALID VALUE und GLU OUT OF MEMORY, die dieselbe Bedeutung wie die zugehörigen \_ \_ \_ \_ \_ \_ \_ OpenGL-Fehlercodes haben.

 

 

 




