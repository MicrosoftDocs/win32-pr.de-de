---
title: Externe Ereignisse
description: Externe Ereignisse
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player Skins, externe Ereignisse
- Skins, externe Ereignisse
- events,external
- Schreiben von Code für Skins, externe Ereignisse
- Externe Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91232447e37bc3970ea8dd0ec727fb9b5daae65e647809b129df3e0347c496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649190"
---
# <a name="external-events"></a>Externe Ereignisse

Wenn Benutzer auf eine Schaltfläche klicken oder eine Taste drücken, können Sie mit Ereignishandlern auf ihre Eingabe reagieren. Ein Ereignishandler ist ein Codeabschnitt, der immer dann ausgeführt wird, wenn das Ereignis ausgelöst wird.

Die folgenden Ereignisse werden von Skinelementen unterstützt:

-   **Laden**
-   **close**
-   **Größe**
-   **Timer**
-   **klicken**
-   **dblclick**
-   **error**
-   **mousedown**
-   **mouseup**
-   **mousemove**
-   **Mouseover**
-   **mouseout**
-   **keypress**
-   **keydown**
-   **keyup**

Weitere Informationen zu bestimmten Ereignissen finden Sie in der [Skin-Programmierreferenz.](skin-programming-reference.md)

Ein typischer externer Ereignishandler würde das Ereignis benennen und den code definieren, der ausgeführt wird. Wenn Sie z. B. Code erstellen möchten, um Windows Media Player zu starten, wenn der Benutzer auf eine Schaltfläche klickt, würden Sie die folgende Zeile in Ihren Schaltflächencode setzen.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Dadurch wird die Datei mit dem Namen laure.wma wiedergegeben. Beachten Sie, dass Sie das Wort "on" zu bestimmten Ereignissen hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Ereignissen**](handling-events.md)
</dt> </dl>

 

 




