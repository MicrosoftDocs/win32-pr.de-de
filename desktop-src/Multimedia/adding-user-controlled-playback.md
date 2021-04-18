---
title: Hinzufügen User-Controlled Wiedergabe
description: Hinzufügen User-Controlled Wiedergabe
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- Mciwndcreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338188"
---
# <a name="adding-user-controlled-playback"></a>Hinzufügen User-Controlled Wiedergabe

Sie können eine benutzergesteuerte Wiedergabe zu einer vorhandenen Anwendung hinzufügen, indem Sie die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion wie folgt aufrufen:


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Mit den [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Parametern werden Handles für das übergeordnete Fenster und die Modul Instanz identifiziert, die dem mciwnd-Fenster zugeordnet ist. Sie geben auch Fenster Stile und den Dateinamen (bzw. den Gerätenamen) an, die dem mciwnd-Fenster zugeordnet werden sollen.

**Mciwndcreate** führt automatisch die folgenden Schritte aus, die für andere Fenster Klassen selbst in Ihrem Code implementiert werden:

1.  Registrieren Sie die mciwnd-Fenster Klasse.
2.  Erstellen Sie das Fenster mciwnd.
3.  Lädt den angegebenen Inhalt.
4.  Legen Sie die aktuelle Wiedergabe Position am Anfang des Inhalts fest.
5.  Zeigen Sie das Geräte Steuerelement an.
6.  Zeigen Sie bei Bedarf den Wiedergabe Bereich des Fensters an.

 

 




