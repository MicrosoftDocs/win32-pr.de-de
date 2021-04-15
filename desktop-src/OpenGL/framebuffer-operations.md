---
title: Framebuffer-Vorgänge
description: Verwenden Sie zum Auswählen des Puffers, in den Farbwerte geschrieben werden, gldrawbuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- OpenGL-Verarbeitungs Pipeline, Framebuffer-Vorgänge
- Framebuffers, Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515597"
---
# <a name="framebuffer-operations"></a>Framebuffer-Vorgänge

Verwenden Sie zum Auswählen des Puffers, in den Farbwerte geschrieben werden, [**gldrawbuffer**](gldrawbuffer.md). Sie verwenden vier verschiedene Funktionen, um das Schreiben von Bits für jeden logischen Framebuffer zu maskieren, nachdem alle Vorgänge pro Fragment ausgeführt wurden:

-   [**glindexmask**](glindexmask.md)
-   [**glcolormask**](glcolormask.md)
-   [**gldepthmask**](gldepthmask.md)
-   [**glstencilmask**](glstencilmask.md)

Die Funktion " [**glaccum**](glaccum.md) " steuert den Vorgang des Akkumulations Puffers. Schließlich legt [**glClear**](glclear.md) jedes Pixel in einer angegebenen Teilmenge der Puffer auf den Wert fest, der mit " [**glclearcolor**](glclearcolor.md)", " [**glclearindex**](glclearindex.md)", " [**glcleartiefe**](glcleardepth.md)", " [**glclearstencil**](glclearstencil.md)" oder " [**glclearaccum**](glclearaccum.md)" angegeben wird.

 

 




