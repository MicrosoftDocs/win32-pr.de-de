---
title: Behandeln von Fehlern (OpenGL)
description: Die Funktion "gluerrorstring" ruft Fehler Zeichenfolgen ab, die den OpenGL-oder glu-Fehlercodes entsprechen.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- OpenGL-Hilfsprogramm (GLU), Fehlercodes
- GLU (OpenGL-Hilfsprogramm), Fehlercodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340018"
---
# <a name="handling-errors-opengl"></a>Behandeln von Fehlern (OpenGL)

Die Funktion " **gluerrorstring** " ruft Fehler Zeichenfolgen ab, die den OpenGL-oder glu-Fehlercodes entsprechen. Die aktuell definierten OpenGL-Fehlercodes werden in [**glgeterror**](glgeterror.md)beschrieben. Die glu-Fehlercodes sind in " [**gluerrorstring**](gluerrorstring.md)", " [*glutesscallback*](glutess.md)", " [*gluvierccallback*](gluquadric.md)" und " [*glunurbscallback*](glunurbs.md)" aufgeführt.

Der Rückgabewert für " **gluerrorstring** " ist ein Zeiger auf eine beschreibende Zeichenfolge, die der im *errorCode* -Parameter übergebenen OpenGL-, Glu-oder glx-Fehlernummer entspricht. Die definierten Fehlercodes werden im OpenGL- *Referenzhandbuch* zusammen mit der Funktion oder Funktion beschrieben, die Sie generieren kann.

 

 




