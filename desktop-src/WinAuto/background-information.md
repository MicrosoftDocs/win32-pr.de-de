---
title: Hintergrundinformationen
description: Die Microsoft Active Accessibility-Komponente, oleacc.dll, erstellt Proxy Objekte, die im Namen von standardmäßigen Windows-Steuerelementen IAccessible implementieren.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100650"
---
# <a name="background-information"></a><span data-ttu-id="146ae-103">Hintergrundinformationen</span><span class="sxs-lookup"><span data-stu-id="146ae-103">Background Information</span></span>

<span data-ttu-id="146ae-104">Die Microsoft Active Accessibility-Komponente, oleacc.dll, erstellt Proxy Objekte, die im Namen von standardmäßigen Windows-Steuerelementen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren.</span><span class="sxs-lookup"><span data-stu-id="146ae-104">The Microsoft Active Accessibility component, oleacc.dll, creates proxy objects that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) on behalf of standard Windows controls.</span></span> <span data-ttu-id="146ae-105">Da diese Proxys standardmäßige Windows-Meldungen und Steuerelement spezifische APIs verwenden, um Informationen zu jedem Steuerelement zu sammeln, gibt es keinen direkten Mechanismus zum Anpassen der Informationen, die diese Proxys über **iaccess verfügbar** machen.</span><span class="sxs-lookup"><span data-stu-id="146ae-105">Because these proxies use standard Windows messages and control-specific APIs to collect information about each control, there has been no direct mechanism for customizing the information these proxies expose through **IAccessible**.</span></span>

<span data-ttu-id="146ae-106">Derzeit können Sie eine vorhandene [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung mithilfe von Unterklassen und Umbrüchen anpassen.</span><span class="sxs-lookup"><span data-stu-id="146ae-106">Currently, you can customize an existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation using subclassing and wrapping techniques.</span></span> <span data-ttu-id="146ae-107">Diese Techniken sind jedoch mühsam und fehleranfällig.</span><span class="sxs-lookup"><span data-stu-id="146ae-107">However, these techniques are tedious and error-prone.</span></span> <span data-ttu-id="146ae-108">Tatsächlich ist der Großteil des Codes, der zum Überschreiben von einer oder zwei Eigenschaften geschrieben wird, mit der Implementierung von Unterklassen und Wrapping verbunden. nur ein kleiner Bruchteil führt die eigentliche Aufgabe der Überschreibung von Informationen aus.</span><span class="sxs-lookup"><span data-stu-id="146ae-108">In fact, the majority of the code written to override one or two properties is concerned with implementing subclassing and wrapping; only a small fraction carries out the real task of overriding information.</span></span> <span data-ttu-id="146ae-109">Durch die dynamische Anmerkung wird die Situation verbessert, indem ähnliche Funktionen bereitgestellt werden, ohne dass Sie eine Unterklassen-oder Wrapping Code schreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="146ae-109">Dynamic Annotation improves the situation by providing similar capabilities without requiring you to write subclassing or wrapping code.</span></span> <span data-ttu-id="146ae-110">Stattdessen können Sie sich auf die Bereitstellung von Code konzentrieren, der die richtigen Informationen liefert.</span><span class="sxs-lookup"><span data-stu-id="146ae-110">Instead, you can focus on providing code that supplies the correct information.</span></span> <span data-ttu-id="146ae-111">Die dynamische Anmerkung ermöglicht Entwicklern, Hinweise und andere nützliche Informationen an oleacc zu übergeben, um die Informationen anzupassen, die Sie verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="146ae-111">Dynamic Annotation allows developers to pass hints and other useful information to OLEACC to customize the information it exposes.</span></span> <span data-ttu-id="146ae-112">Diese Funktion allein reduziert die Kosten für die Unterstützung von Microsoft Active Accessibility und ermöglicht Entwicklern, den Zugriff auf die Benutzeroberflächen erheblich zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="146ae-112">This capability alone will reduce the cost of supporting Microsoft Active Accessibility and allow developers to greatly improve the accessibility of their user interfaces.</span></span>

 

 




