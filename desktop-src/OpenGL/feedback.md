---
title: Feedback
description: Im Feedbackmodus generiert jeder Primitive, der gerast werden soll, einen Block von Werten, der in das Feedbackarray kopiert wird.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- Feedbackmodus,OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5d307b9033a60a03b585cb4df6109293d3b9b0b276bde822ca595eb37fcd19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082450"
---
# <a name="feedback-mode"></a>Feedbackmodus

Im Feedbackmodus generiert jeder Primitive, der gerast werden soll, einen Block von Werten, der in das Feedbackarray kopiert wird. Stellen Sie für dieses Array [**glFeedbackBuffer**](glfeedbackbuffer.md)zur Verfügung, das Sie aufrufen müssen, bevor Sie OpenGL in den Feedbackmodus versetzen. Jeder Werteblock beginnt mit einem Code, der den primitiven Typ angibt, gefolgt von Werten, die die Scheitelpunkte des Primitivs und die zugehörigen Daten beschreiben. Einträge werden auch für Bitmaps und Pixelrechtecke geschrieben. Es ist nicht garantiert, dass Werte in das Feedbackarray geschrieben werden, bis Sie [**glRenderMode**](glrendermode.md) aufrufen, um OpenGL aus dem Feedbackmodus zu nehmen. Mit [**glPassThrough**](glpassthrough.md) können Sie einen Marker bereitstellen, der im Feedbackmodus zurückgegeben wird, als wäre es ein Primitiver.

 

 




