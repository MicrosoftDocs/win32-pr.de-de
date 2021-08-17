---
description: Die allgemeine Regel ist, dass eine Desktop-App eine winRT-API (Windows Runtime) aufrufen kann. Einige APIs, einschließlich der XAML-UI-APIs, erfordern jedoch, dass die aufrufende App über eine Paketidentität verfügt.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: WinRT-APIs, die von einer Desktop-App aus aufgerufen werden können
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bbfb2316a6fd4dd8d35d0744acc4ad301dba7f42aee36ee865d67bb2fff805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130302"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>WinRT-APIs, die von einer Desktop-App aus aufgerufen werden können

Die meisten [WinRT-APIs (Windows Runtime)](/uwp/api/) können von Desktop-Apps (.NET und native c++) verwendet werden. Einige WinRT-Klassen sind jedoch für konzipiert und werden nur für die Verwendung in UWP-Apps unterstützt. Dazu gehören [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)und einige verwandte Klassen. Andere WinRT-Klassen funktionieren in Desktop-Apps mit Ausnahme bestimmter Member.

Weitere Informationen finden Sie unter [In Desktop-Apps nicht unterstützte Windows-Runtime-APIs](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api). Falls verfügbar, schlägt dieser Artikel alternative APIs vor, um die gleiche Funktionalität wie durch die nicht unterstützten APIs zu erreichen.
