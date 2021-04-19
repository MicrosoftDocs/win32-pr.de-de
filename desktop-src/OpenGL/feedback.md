---
title: Feedback
description: Im Feedback Modus generiert jedes primitive, das rasterisiert werden soll, einen Block von Werten, die in das Feedback Array kopiert werden.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- Feedback Modus, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106373426"
---
# <a name="feedback-mode"></a>Feedback Modus

Im Feedback Modus generiert jedes primitive, das rasterisiert werden soll, einen Block von Werten, die in das Feedback Array kopiert werden. Geben Sie dieses Array mit [**glfeedbackbuffer**](glfeedbackbuffer.md)an, das aufgerufen werden muss, bevor OpenGL in den Feedback Modus versetzt wird. Jeder Block von Werten beginnt mit einem Code, der den primitiven Typ anzeigt, gefolgt von Werten, die die Scheitel Punkte und zugeordneten Daten des primitiven beschreiben. Einträge werden auch für Bitmaps und Pixel Rechtecke geschrieben. Es ist nicht garantiert, dass die Werte in das Feedback Array geschrieben werden, bis Sie " [**glrendermode**](glrendermode.md) " aufgerufen haben, um OpenGL aus dem Feedback Modus zu nehmen. Sie können mit [**glpassthrough**](glpassthrough.md) einen Marker angeben, der im Feedback Modus zurückgegeben wird, als ob es sich um einen primitiven handelt.

 

 




