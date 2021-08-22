---
title: Erweitern von OpenGL-Funktionen
description: Die OpenGL-Bibliothek unterstützt mehrere Implementierungen ihrer Funktionen.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL auf Windows,Erweiterungsfunktionen
- Erweiterungsfunktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dce68498d5a3e672e63da1ae05d9bb513a4121d110237d90cdad75df0ff84d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361342"
---
# <a name="extending-opengl-functions"></a>Erweitern von OpenGL-Funktionen

Die OpenGL-Bibliothek unterstützt mehrere Implementierungen ihrer Funktionen. Erweiterungsfunktionen, die in einem Renderingkontext unterstützt werden, werden nicht unbedingt in einem anderen Renderingkontext unterstützt. Verwenden Sie für einen angegebenen Renderingkontext in einer Anwendung mitHilfe von Erweiterungsfunktionen nur die Funktionsadressen, die von der [**wglGetProcAddress-Funktion zurückgegeben**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) werden.

 

 




