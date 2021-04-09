---
title: Duale Schnittstellen (com)
description: Duale Schnittstellen
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039718"
---
# <a name="dual-interfaces"></a><span data-ttu-id="5d444-103">Duale Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5d444-103">Dual Interfaces</span></span>

<span data-ttu-id="5d444-104">OLE-Automatisierung ermöglicht einem Objekt, eine Reihe von Methoden auf zwei Arten verfügbar zu machen: über die **IDispatch** -Schnittstelle und durch direkte OLE-Vtable-Bindungen.</span><span class="sxs-lookup"><span data-stu-id="5d444-104">OLE Automation enables an object to expose a set of methods in two ways: via the **IDispatch** interface, and through direct OLE VTable binding.</span></span> <span data-ttu-id="5d444-105">**IDispatch** wird von den meisten Tools verwendet, die heute verfügbar sind, und bietet Unterstützung für das späte Binden an Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="5d444-105">**IDispatch** is used by most tools available today, and offers support for late binding to properties and methods.</span></span>

<span data-ttu-id="5d444-106">Die Vtable-Bindung bietet eine wesentlich höhere Leistung, da diese Methode direkt anstelle von **IDispatch:: Aufrufen** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5d444-106">VTable binding offers much higher performance because this method is called directly instead of through **IDispatch::Invoke**.</span></span> <span data-ttu-id="5d444-107">**IDispatch** bietet eine spät gebundene Unterstützung, bei der die direkte Vtable-Bindung einen erheblichen Leistungsgewinn bietet. Beide Techniken sind wertvoll und in verschiedenen Szenarien wichtig.</span><span class="sxs-lookup"><span data-stu-id="5d444-107">**IDispatch** offers late bound support, where direct VTable binding offers a significant performance gain; both techniques are valuable and important in different scenarios.</span></span> <span data-ttu-id="5d444-108">Durch das bezeichnen einer Schnittstelle als \[ [**Dual**](/windows/desktop/Midl/dual) \] in der Typbibliothek kann eine OLE-Automatisierungsschnittstelle entweder über **IDispatch** oder direkt an gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="5d444-108">By labeling an interface as \[[**dual**](/windows/desktop/Midl/dual)\] in the type library, an OLE Automation interface can be used either via **IDispatch**, or it can be bound to directly.</span></span> <span data-ttu-id="5d444-109">Container können daher die am besten geeignete Methode auswählen.</span><span class="sxs-lookup"><span data-stu-id="5d444-109">Containers can thus choose the most appropriate technique.</span></span> <span data-ttu-id="5d444-110">Die Unterstützung für duale Schnittstellen wird für Steuerelemente und Container dringend empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5d444-110">Support for dual interfaces is strongly recommended for both controls and containers.</span></span>

 

 