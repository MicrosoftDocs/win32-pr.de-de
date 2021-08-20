---
title: Verwenden von Fensterstilen zum Ändern des MCIWnd-Fensters
description: Verwenden von Fensterstilen zum Ändern des MCIWnd-Fensters
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90212b43d6d51c82eb9b6e1a26bb06c7215c2568594e04980294b0d87bd53e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135608"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Verwenden von Fensterstilen zum Ändern des MCIWnd-Fensters

Wie bei jedem Fenster können Sie die Darstellung und das Verhalten eines MCIWnd-Fensters ändern, indem Sie aus den Standardfensterstilen auswählen, die mit der [CreateWindow-Funktion angegeben](/windows/win32/api/winuser/nf-winuser-createwindowa) werden. Darüber hinaus können Sie aus mehreren anderen Fensterstilen auswählen, die für MCIWnd-Fenster spezifisch sind. Mit diesen Stilen kann Ihre Anwendung diese MCIWnd-Fenster wie folgt ändern:

-   Ändern sie die Fenstergröße.
-   Ausblenden oder Anzeigen von Steuerelementen.
-   Geben Sie Benachrichtigungsmeldungen aus.
-   Zeigen Sie Informationen auf der Titelleiste an.

Sie können Fensterstile festlegen, indem Sie sie in der [**MCIWndCreate-Funktion**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) angeben, oder Sie können das [**MCIWndChangeStyles-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) verwenden, um den Stil eines vorhandenen MCIWnd-Fensters zu ändern. Sie können ein MCIWnd-Fenster auch mithilfe des [**MCIWndGetStyles-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) nach seinen aktuellen Stilen abfragen.

Eine Liste der MCIWnd-spezifischen Fensterstile finden Sie unter [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 