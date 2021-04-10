---
title: Erweitern von OpenGL-Funktionen
description: Die OpenGL-Bibliothek unterstützt mehrere Implementierungen ihrer Funktionen.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL unter Windows, Erweiterungsfunktionen
- Erweiterungsfunktionen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947978"
---
# <a name="extending-opengl-functions"></a>Erweitern von OpenGL-Funktionen

Die OpenGL-Bibliothek unterstützt mehrere Implementierungen ihrer Funktionen. In einem renderingkontext unterstützte Erweiterungsfunktionen werden nicht notwendigerweise in einem anderen renderingkontext unterstützt. Verwenden Sie für einen gegebenen renderingkontext in einer Anwendung, die Erweiterungsfunktionen verwendet, nur die von der [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) -Funktion zurückgegebenen Funktions Adressen.

 

 




