---
title: Ändern des mciwnd-Fensters mithilfe von Fenster Stilen
description: Ändern des mciwnd-Fensters mithilfe von Fenster Stilen
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Mciwndcreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337840"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Ändern des mciwnd-Fensters mithilfe von Fenster Stilen

Wie bei jedem beliebigen Fenster können Sie die Darstellung und das Verhalten eines mciwnd-Fensters ändern, indem Sie aus den Standardfenster Stilen auswählen, die mit der Funktion "up [Window](/windows/win32/api/winuser/nf-winuser-createwindowa) " angegeben werden. Darüber hinaus können Sie aus verschiedenen anderen Fenster Stilen auswählen, die für mciwnd-Fenster spezifisch sind. Diese Formate können von Ihrer Anwendung auf folgende Weise geändert werden:

-   Ändern Sie die Fenstergröße.
-   Ausblenden oder Anzeigen von Steuerelementen.
-   Ausgeben von Benachrichtigungs Meldungen.
-   Anzeigen von Informationen in der Titelleiste.

Sie können Fenster Stile festlegen, indem Sie Sie in der [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion angeben, oder Sie können das [**mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) -Makro verwenden, um den Stil eines vorhandenen mciwnd-Fensters zu ändern. Sie können auch ein mciwnd-Fenster für seine aktuellen Stile Abfragen, indem Sie das [**mciwndgetstyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) -Makro verwenden.

Eine Liste der mciwnd-spezifischen Fenster Stile finden Sie unter [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 