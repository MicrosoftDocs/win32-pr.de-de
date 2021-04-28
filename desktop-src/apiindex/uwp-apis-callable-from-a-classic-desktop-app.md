---
description: Die allgemeine Regel ist, dass eine Desktop-App eine winRT-API (Windows-Runtime) aufrufen kann. Einige APIs, einschließlich der XAML-UI-APIs, erfordern jedoch, dass die aufrufende App über eine Paketidentität verfügt.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: WinRT-APIs, die über eine Desktop-App aufgerufen werden können
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f99cca14c066f372ad7fd417e04137a62ae628
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172482"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a><span data-ttu-id="f3e5c-104">WinRT-APIs, die über eine Desktop-App aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="f3e5c-104">WinRT APIs callable from a desktop app</span></span>

<span data-ttu-id="f3e5c-105">Die meisten [winRT-APIs (Windows-Runtime)](/uwp/api/) können von Desktop-Apps (.NET und native c++) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3e5c-105">Most [Windows Runtime (WinRT) APIs](/uwp/api/) can be used by desktop (.NET and native C++) apps.</span></span> <span data-ttu-id="f3e5c-106">Einige WinRT-Klassen sind jedoch für konzipiert und werden nur für die Verwendung in UWP-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3e5c-106">However, some WinRT classes are designed for and are only supported for use in UWP apps.</span></span> <span data-ttu-id="f3e5c-107">Dazu gehören [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)und einige verwandte Klassen.</span><span class="sxs-lookup"><span data-stu-id="f3e5c-107">This includes [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview), and some related classes.</span></span> <span data-ttu-id="f3e5c-108">Andere WinRT-Klassen funktionieren in Desktop-Apps mit Ausnahme bestimmter Member.</span><span class="sxs-lookup"><span data-stu-id="f3e5c-108">Other WinRT classes work in desktop apps except for specific members.</span></span>

<span data-ttu-id="f3e5c-109">Weitere Informationen finden Sie unter [Windows-Runtime-APIs, die in Desktop-Apps nicht unterstützt werden.](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api)</span><span class="sxs-lookup"><span data-stu-id="f3e5c-109">For more information, see [Windows Runtime APIs not supported in desktop apps](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api).</span></span> <span data-ttu-id="f3e5c-110">Sofern verfügbar, werden in diesem Artikel alternative APIs vorgeschlagen, um die gleiche Funktionalität wie die nicht unterstützten APIs zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="f3e5c-110">Where available, this article suggests alternative APIs to achieve the same functionality as the unsupported APIs.</span></span>
