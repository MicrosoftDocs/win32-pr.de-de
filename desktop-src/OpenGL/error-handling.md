---
title: Fehlerbehandlung (OpenGL)
description: Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode aufgezeichnet.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- Fehlerbehandlung bei OpenGL
- OpenGL-Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337699"
---
# <a name="error-handling-opengl"></a>Fehlerbehandlung (OpenGL)

Wenn OpenGL einen Fehler erkennt, wird ein aktueller Fehlercode aufgezeichnet. Die Funktion, die den Fehler verursacht hat, wird ignoriert und hat daher keine Auswirkung auf den OpenGL-Zustand oder den Frame Puffer-Inhalt. (Wenn der aufgezeichnete Fehler "GL \_ " war Nicht genügend Arbeits \_ \_ Speicher, die Ergebnisse der Funktion sind jedoch nicht definiert.) Nachdem Sie aufgezeichnet wurde, wird der aktuelle Fehlercode erst gelöscht, wenn Sie die Abfragefunktion " [**glgeterror**](glgeterror.md) " aufrufen, die den aktuellen Fehlercode zurückgibt.

Implementierungen von OpenGL können mehrere aktuelle Fehlercodes zurückgeben, die jeweils so lange festgelegt bleiben, bis Sie abgefragt werden. Die **glgeterror** -Funktion gibt den Fehler "GL No error" zurück, wenn \_ \_ Sie alle aktuellen Fehlercodes abgefragt haben oder wenn kein Fehler vorliegt. Wenn Sie also einen Fehlercode erhalten, rufen Sie **glgeterror** auf, bis GL \_ kein \_ Fehler zurückgegeben wird, um sicherzustellen, dass Sie alle Fehler ermittelt haben. Eine Liste der Fehlercodes finden Sie unter [OpenGL-Fehlercodes](opengl-error-codes.md).

Sie können die Funktion " [**gluerrorstring**](gluerrorstring.md) glu" verwenden, um eine beschreibende Zeichenfolge zu erhalten, die dem Fehlercode entspricht, der in der Übergabe Weitere Informationen zu " **gluerrorstring**" finden Sie unter [Behandeln von Fehlern](handling-errors.md).

> [!Note]  
> Die glu-Funktionen geben häufig Fehler Werte zurück, wenn ein Fehler erkannt wird. Die OpenGL Utility Library definiert außerdem die Fehlercodes glu \_ invalid \_ enum, Glu \_ invalid \_ Value und glu \_ out \_ of \_ Memory, die dieselbe Bedeutung wie die zugehörigen OpenGL-Fehlercodes haben.

 

 

 




