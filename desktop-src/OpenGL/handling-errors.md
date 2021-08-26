---
title: Behandeln von Fehlern (OpenGL)
description: Die funktion gluErrorString ruft Fehlerzeichenfolgen ab, die OpenGL- oder GLU-Fehlercodes entsprechen.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- OpenGL-Hilfsprogramm (GLU), Fehlercodes
- GLU (OpenGL Utility), Fehlercodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ac3fd9010862dd9c567cb7688f7f96286cae06f7e3b0e4ffe73d3b41ca9b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035190"
---
# <a name="handling-errors-opengl"></a>Behandeln von Fehlern (OpenGL)

Die **funktion gluErrorString** ruft Fehlerzeichenfolgen ab, die OpenGL- oder GLU-Fehlercodes entsprechen. Die derzeit definierten OpenGL-Fehlercodes werden unter [**glGetError**](glgeterror.md)beschrieben. Die GLU-Fehlercodes sind in [**gluErrorString,**](gluerrorstring.md) [*gluTessCallback,*](glutess.md) [*gluQuadricCallback*](gluquadric.md)und [*gluNurbsCallback*](glunurbs.md)aufgeführt.

Der Rückgabewert für **gluErrorString** ist ein Zeiger auf eine beschreibende Zeichenfolge, die der im *errorCode-Parameter* übergebenen OpenGL-, GLU- oder GLX-Fehlernummer entspricht. Die definierten Fehlercodes werden im *OpenGL-Referenzhandbuch* zusammen mit der Funktion oder Funktion beschrieben, die sie generieren kann.

 

 




