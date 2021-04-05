---
title: Typen von IAccessible-Unterstützung
description: Typen von IAccessible-Unterstützung
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710686"
---
# <a name="types-of-iaccessible-support"></a><span data-ttu-id="c4231-103">Typen von IAccessible-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c4231-103">Types of IAccessible Support</span></span>

<span data-ttu-id="c4231-104">Für Microsoft Active Accessibility-Server gibt es zwei Typen von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Unterstützung: Native und Proxy.</span><span class="sxs-lookup"><span data-stu-id="c4231-104">Microsoft Active Accessibility servers have two types of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support: native and proxied.</span></span> <span data-ttu-id="c4231-105">Die Benutzeroberflächen Elemente, die in einer Anwendung verwendet werden, bestimmen, welche Art von Unterstützung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c4231-105">The UI elements used in an application determine which type of support is appropriate.</span></span> <span data-ttu-id="c4231-106">Viele Server, die heute geschrieben werden, profitieren von der Verwendung von **IAccessible** -Proxys und implementieren nur **IAccessible** für Steuerelemente, die nicht durch Oleacc.dll über einen Proxy verfügen, z. b. fensterlose Steuerelemente oder Steuerelemente mit einem benutzerdefinierten Fenster Klassennamen</span><span class="sxs-lookup"><span data-stu-id="c4231-106">Many servers being written today take full advantage of **IAccessible** proxies and only implement **IAccessible** for those controls that are not proxied by Oleacc.dll, such as windowless controls or controls with a custom window class name.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4231-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c4231-107">In this section</span></span>

-   [<span data-ttu-id="c4231-108">Native Active Accessibility-Implementierung</span><span class="sxs-lookup"><span data-stu-id="c4231-108">Native Active Accessibility Implementation</span></span>](native-active-accessibility-implementation.md)
-   [<span data-ttu-id="c4231-109">Ibarrierefreie Proxys</span><span class="sxs-lookup"><span data-stu-id="c4231-109">IAccessible Proxies</span></span>](iaccessible-proxies.md)

 

 




