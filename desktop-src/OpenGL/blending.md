---
title: Bänder
description: Beim Mischen werden die R-, G-, B-und a-Werte eines Fragments mit den Werten kombiniert, die im Frame Puffer am entsprechenden Speicherort gespeichert sind.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- OpenGL-Verarbeitungs Pipeline, Blending
- Mischen von OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310011"
---
# <a name="blending"></a><span data-ttu-id="90772-105">Bänder</span><span class="sxs-lookup"><span data-stu-id="90772-105">Blending</span></span>

<span data-ttu-id="90772-106">Beim Mischen werden die R-, G-, B-und a-Werte eines Fragments mit den Werten kombiniert, die im Frame Puffer am entsprechenden Speicherort gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="90772-106">Blending combines a fragment's R, G, B, and A values with those stored in the framebuffer at the corresponding location.</span></span> <span data-ttu-id="90772-107">Der Mischungs Wert, der nur im RGBA-Modus ausgeführt wird, hängt vom Alphawert des Fragments und vom entsprechenden aktuell gespeicherten Pixel ab. Dies kann auch von den RGB-Werten abhängen.</span><span class="sxs-lookup"><span data-stu-id="90772-107">The blending, which is performed only in RGBA mode, depends on the alpha value of the fragment and that of the corresponding currently stored pixel; it may also depend on the RGB values.</span></span> <span data-ttu-id="90772-108">Sie steuern das Mischen mit [**glblendfunc**](glblendfunc.md), mit dem Sie die Quell-und zielmischungs Faktoren angeben.</span><span class="sxs-lookup"><span data-stu-id="90772-108">You control blending with [**glBlendFunc**](glblendfunc.md), with which you indicate the source and destination blending factors.</span></span>

 

 




