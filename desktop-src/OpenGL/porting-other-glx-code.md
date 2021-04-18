---
title: Portieren von anderem glx-Code
description: Portieren von anderem glx-Code
ms.assetid: 3a67a206-d249-493c-a774-c3bbaa933611
keywords:
- Portieren auf OpenGL, glx-Code
- OpenGL-Portierung, glx-Code
- X-Fenster System, Portieren von glx-Code
- Glx-Funktionen, portieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c2f9430fbef8bef7c41a2d6c6f86bf6e9f3e7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337799"
---
# <a name="porting-other-glx-code"></a><span data-ttu-id="2c2c1-107">Portieren von anderem glx-Code</span><span class="sxs-lookup"><span data-stu-id="2c2c1-107">Porting Other GLX Code</span></span>

<span data-ttu-id="2c2c1-108">Zusätzlich zu den in den vorherigen Abschnitten beschriebenen Xlib-und glx-Funktionen enthält Ihr Programm wahrscheinlich einige der anderen in der über [setzung der glx-Bibliothek](translating-the-glx-library.md)aufgeführten Funktionen von glx oder xlib.</span><span class="sxs-lookup"><span data-stu-id="2c2c1-108">In addition to the Xlib and GLX functions described in the preceding sections, your program probably contains some of the other GLX or Xlib functions listed in [Translating the GLX Library](translating-the-glx-library.md).</span></span> <span data-ttu-id="2c2c1-109">Schreiben Sie Ihren X-Fenster System Code in Windows um, und ersetzen Sie dabei die entsprechenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2c2c1-109">Rewrite your X Window System code to Windows, substituting the appropriate functions.</span></span>

 

 




