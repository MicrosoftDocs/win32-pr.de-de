---
title: OpenGL-Grafik Steuerelement
description: OpenGL-Grafik Steuerelement
ms.assetid: 327f2920-1bc9-4de7-aa12-3e9f74a94759
keywords:
- OpenGL, Grafik Steuerelement
- Grafik Steuerelement OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bb138a2d8c597fae2d92a1d1394c8ff05b03cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710601"
---
# <a name="opengl-graphic-control"></a><span data-ttu-id="dd6ce-105">OpenGL-Grafik Steuerelement</span><span class="sxs-lookup"><span data-stu-id="dd6ce-105">OpenGL Graphic Control</span></span>

<span data-ttu-id="dd6ce-106">OpenGL bietet Ihnen Recht direkte Kontrolle über die grundlegenden Vorgänge von zwei-und dreidimensionalen Grafiken.</span><span class="sxs-lookup"><span data-stu-id="dd6ce-106">OpenGL provides you with fairly direct control over the fundamental operations of two- and three-dimensional graphics.</span></span> <span data-ttu-id="dd6ce-107">Dies umfasst die Angabe solcher Parameter als Transformations Matrizen, Beleuchtungs Formel Koeffizienten, Antialiasing-Methoden und Pixel Aktualisierungs Operatoren.</span><span class="sxs-lookup"><span data-stu-id="dd6ce-107">This includes specification of such parameters as transformation matrices, lighting equation coefficients, antialiasing methods, and pixel-update operators.</span></span> <span data-ttu-id="dd6ce-108">Es bietet Ihnen jedoch keine Möglichkeit, komplexe geometrische Objekte zu beschreiben oder zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="dd6ce-108">However, it doesn't provide you with a means for describing or modeling complex geometric objects.</span></span> <span data-ttu-id="dd6ce-109">Daher geben die von Ihnen ausgelegten OpenGL-Befehle an, wie ein bestimmtes Ergebnis erstellt werden soll (die Prozedur, die befolgt werden soll), anstatt genau das Ergebnis zu sehen.</span><span class="sxs-lookup"><span data-stu-id="dd6ce-109">Thus, the OpenGL commands you issue specify how a certain result should be produced (what procedure should be followed) rather than what exactly that result should look like.</span></span> <span data-ttu-id="dd6ce-110">Das heißt, OpenGL ist grundlegend prozedural und nicht beschreibend.</span><span class="sxs-lookup"><span data-stu-id="dd6ce-110">That is, OpenGL is fundamentally procedural rather than descriptive.</span></span> <span data-ttu-id="dd6ce-111">Um die Verwendung von OpenGL vollständig zu verstehen, ist es hilfreich, die Reihenfolge zu kennen, in der die Vorgänge durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dd6ce-111">To fully understand how to use OpenGL, it helps to know the order in which it carries out its operations.</span></span>

 

 




