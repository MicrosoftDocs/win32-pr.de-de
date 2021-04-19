---
title: Externe Ereignisse
description: Externe Ereignisse
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player Skins, externe Ereignisse
- Skins, externe Ereignisse
- Ereignisse, extern
- Schreiben von Code für Skins, externe Ereignisse
- externe Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342299"
---
# <a name="external-events"></a>Externe Ereignisse

Wenn Benutzer auf eine Schaltfläche klicken oder eine Taste drücken, können Sie auf Ihre Eingabe mit Ereignis Handlern reagieren. Ein Ereignishandler ist ein Code Abschnitt, der immer dann ausgeführt wird, wenn das Ereignis ausgelöst wird.

Die folgenden Ereignisse werden von Skin-Elementen unterstützt:

-   **Laden**
-   **close**
-   **Größe**
-   **Messer**
-   **Sie**
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

Weitere Informationen zu bestimmten Ereignissen finden Sie in der Design- [Programmier Referenz](skin-programming-reference.md) .

Ein typischer externer Ereignishandler würde das Ereignis benennen und den Code definieren, der ausgeführt wird. Wenn Sie z. b. Code zum Starten von Windows Media Player erstellen möchten, wenn der Benutzer auf eine Schaltfläche klickt, würden Sie die folgende Zeile in den Schaltflächen Code einfügen.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Dadurch wird die Datei mit dem Namen "Laure. wma" wiedergegeben. Beachten Sie, dass Sie das Wort "on" bestimmten Ereignissen hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Ereignissen**](handling-events.md)
</dt> </dl>

 

 




