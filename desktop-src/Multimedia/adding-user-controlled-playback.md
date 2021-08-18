---
title: Hinzufügen User-Controlled Wiedergabe
description: Hinzufügen User-Controlled Wiedergabe
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62d4e4af43be9877ec5bf3fae452e44ae415bc47047448cb65b64ad3446e0b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941818"
---
# <a name="adding-user-controlled-playback"></a>Hinzufügen User-Controlled Wiedergabe

Sie können einer vorhandenen Anwendung eine benutzergesteuerte Wiedergabe hinzufügen, indem Sie die [**MCIWndCreate-Funktion**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) wie folgt aufrufen:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Die [**MCIWndCreate-Parameter**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identifizieren Handles für das übergeordnete Fenster und die Modulinstanz, die dem MCIWnd-Fenster zugeordnet ist. Sie geben auch Fensterstile und den Dateinamen (oder Gerätenamen) an, die dem MCIWnd-Fenster zugeordnet werden sollen.

**MCIWndCreate** führt automatisch die folgenden Schritte aus, die Sie für andere Fensterklassen selbst in Ihren Code implementieren würden:

1.  Registrieren Sie die MCIWnd-Fensterklasse.
2.  Erstellen Sie das MCIWnd-Fenster.
3.  Laden Sie den angegebenen Inhalt.
4.  Legen Sie die aktuelle Wiedergabeposition am Anfang des Inhalts fest.
5.  Zeigt das Gerätesteuerelement an.
6.  Zeigen Sie bei Bedarf den Wiedergabebereich des Fensters an.

 

 




