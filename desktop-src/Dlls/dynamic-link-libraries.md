---
description: Eine Dynamic Link Library (DLL) ist ein Modul, das Funktionen und Daten enthält, die von einem anderen Modul (Anwendung oder DLL) verwendet werden können.
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Dynamic-Link Bibliotheken (Dynamic Link Libraries)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369091464aad63ea78ea9f24a84fb4eb49eb810a1faff14571fc67e2e39bb0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815899"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Dynamic-Link Bibliotheken (Dynamic Link Libraries)

Eine *Dynamic Link Library* (DLL) ist ein Modul, das Funktionen und Daten enthält, die von einem anderen Modul (Anwendung oder DLL) verwendet werden können.

Eine DLL kann zwei Arten von Funktionen definieren: exportiert und intern. Die exportierten Funktionen sollen von anderen Modulen sowie innerhalb der DLL aufgerufen werden, in der sie definiert sind. Interne Funktionen sollen in der Regel nur innerhalb der DLL aufgerufen werden, in der sie definiert sind. Obwohl eine DLL Daten exportieren kann, werden ihre Daten in der Regel nur von ihren Funktionen verwendet. Es gibt jedoch nichts, das ein anderes Modul daran hindern kann, diese Adresse zu lesen oder zu schreiben.

DLLs bieten eine Möglichkeit, Anwendungen zu modularisieren, sodass ihre Funktionalität einfacher aktualisiert und wiederverwendet werden kann. DLLs tragen auch dazu bei, den Arbeitsspeicheraufwand zu reduzieren, wenn mehrere Anwendungen die gleiche Funktionalität gleichzeitig verwenden, da die Anwendungen den DLL-Code zwar erhalten, aber obwohl jede Anwendung eine eigene Kopie der DLL-Daten erhält.

Die Windows API (Application Programming Interface) wird als Satz von DLLs implementiert, sodass jeder Prozess, der die Windows-API verwendet, dynamische Verknüpfungen verwendet.

-   [Informationen Dynamic-Link Bibliotheken](about-dynamic-link-libraries.md)
-   [Verwenden Dynamic-Link Bibliotheken](using-dynamic-link-libraries.md)
-   [Dynamic Link Library Reference (Dynamic Link Library-Referenz)](dynamic-link-library-reference.md)

> [!Note]  
> Wenn sie probleme mit einer DLL auf Ihrem Computer haben, wenden Sie sich an den Kundensupport des Softwareanbieters, der die DLL veröffentlicht. Wenn Sie der Meinung sind, dass Sie Support für ein Microsoft-Produkt (einschließlich Windows) benötigen, besuchen Sie unsere Website für technischen Support [unter support.microsoft.com.](https://support.microsoft.com)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
