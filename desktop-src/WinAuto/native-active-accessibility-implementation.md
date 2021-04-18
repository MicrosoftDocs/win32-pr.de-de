---
title: Native Active Accessibility-Implementierung
description: Benutzeroberflächen Elemente, die die IAccessible-Schnittstelle implementieren, stellen eine native Implementierung dar.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339415"
---
# <a name="native-active-accessibility-implementation"></a><span data-ttu-id="8ecc8-103">Native Active Accessibility-Implementierung</span><span class="sxs-lookup"><span data-stu-id="8ecc8-103">Native Active Accessibility Implementation</span></span>

<span data-ttu-id="8ecc8-104">Benutzeroberflächen Elemente, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren, stellen eine *native Implementierung* dar.</span><span class="sxs-lookup"><span data-stu-id="8ecc8-104">User interface elements that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface are said to provide a *native implementation*.</span></span> <span data-ttu-id="8ecc8-105">Obwohl die Entwicklungskosten für die Implementierung von **IAccessible** (oder einer beliebigen anderen Component Object Model (com)-Schnittstelle) hoch sein können, ist der Vorteil die umfassende Kontrolle über die Informationen, die Clients zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8ecc8-105">Although the development cost for implementing **IAccessible** (or any other Component Object Model (COM) interface) can be high, the benefit is complete control over the information exposed to clients.</span></span>

<span data-ttu-id="8ecc8-106">Wenn Ihre Anwendung benutzerdefinierte Steuerelemente oder andere Steuerelemente verwendet, die nicht von Oleacc.dll bereitgestellt werden können, müssen Sie eine systemeigene Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8ecc8-106">If your application uses custom controls or other controls that cannot be proxied by Oleacc.dll, you will need to provide a native implementation.</span></span>

 

 




