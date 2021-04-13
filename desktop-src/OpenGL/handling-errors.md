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
# <a name="handling-errors-opengl"></a><span data-ttu-id="121d9-105">Behandeln von Fehlern (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="121d9-105">Handling Errors (OpenGL)</span></span>

<span data-ttu-id="121d9-106">Die Funktion " **gluerrorstring** " ruft Fehler Zeichenfolgen ab, die den OpenGL-oder glu-Fehlercodes entsprechen.</span><span class="sxs-lookup"><span data-stu-id="121d9-106">The **gluErrorString** function retrieves error strings that correspond to OpenGL or GLU error codes.</span></span> <span data-ttu-id="121d9-107">Die aktuell definierten OpenGL-Fehlercodes werden in [**glgeterror**](glgeterror.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="121d9-107">The currently defined OpenGL error codes are described in [**glGetError**](glgeterror.md).</span></span> <span data-ttu-id="121d9-108">Die glu-Fehlercodes sind in " [**gluerrorstring**](gluerrorstring.md)", " [*glutesscallback*](glutess.md)", " [*gluvierccallback*](gluquadric.md)" und " [*glunurbscallback*](glunurbs.md)" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="121d9-108">The GLU error codes are listed in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md), and [*gluNurbsCallback*](glunurbs.md).</span></span>

<span data-ttu-id="121d9-109">Der Rückgabewert für " **gluerrorstring** " ist ein Zeiger auf eine beschreibende Zeichenfolge, die der im *errorCode* -Parameter übergebenen OpenGL-, Glu-oder glx-Fehlernummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="121d9-109">The return value for **gluErrorString** is a pointer to a descriptive string that corresponds to the OpenGL, GLU, or GLX error number passed in the *errorCode* parameter.</span></span> <span data-ttu-id="121d9-110">Die definierten Fehlercodes werden im OpenGL- *Referenzhandbuch* zusammen mit der Funktion oder Funktion beschrieben, die Sie generieren kann.</span><span class="sxs-lookup"><span data-stu-id="121d9-110">The defined error codes are described in the *OpenGL Reference Manual* along with the function or function that can generate them.</span></span>

 

 




