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
# <a name="adding-user-controlled-playback"></a><span data-ttu-id="43e38-104">Hinzufügen User-Controlled Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="43e38-104">Adding User-Controlled Playback</span></span>

<span data-ttu-id="43e38-105">Sie können eine benutzergesteuerte Wiedergabe zu einer vorhandenen Anwendung hinzufügen, indem Sie die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion wie folgt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="43e38-105">You can add user-controlled playback to an existing application by calling the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function as follows:</span></span>


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



<span data-ttu-id="43e38-106">Mit den [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Parametern werden Handles für das übergeordnete Fenster und die Modul Instanz identifiziert, die dem mciwnd-Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="43e38-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) parameters identify handles to the parent window and to the module instance associated with the MCIWnd window.</span></span> <span data-ttu-id="43e38-107">Sie geben auch Fenster Stile und den Dateinamen (bzw. den Gerätenamen) an, die dem mciwnd-Fenster zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43e38-107">They also specify window styles and the filename (or device name) to associate with the MCIWnd window.</span></span>

<span data-ttu-id="43e38-108">**Mciwndcreate** führt automatisch die folgenden Schritte aus, die für andere Fenster Klassen selbst in Ihrem Code implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="43e38-108">**MCIWndCreate** automatically performs the following steps that, for other window classes, you would implement in your code yourself:</span></span>

1.  <span data-ttu-id="43e38-109">Registrieren Sie die mciwnd-Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="43e38-109">Register the MCIWnd window class.</span></span>
2.  <span data-ttu-id="43e38-110">Erstellen Sie das Fenster mciwnd.</span><span class="sxs-lookup"><span data-stu-id="43e38-110">Create the MCIWnd window.</span></span>
3.  <span data-ttu-id="43e38-111">Lädt den angegebenen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="43e38-111">Load the specified content.</span></span>
4.  <span data-ttu-id="43e38-112">Legen Sie die aktuelle Wiedergabe Position am Anfang des Inhalts fest.</span><span class="sxs-lookup"><span data-stu-id="43e38-112">Establish the current playback position at the beginning of the content.</span></span>
5.  <span data-ttu-id="43e38-113">Zeigen Sie das Geräte Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="43e38-113">Display the device control.</span></span>
6.  <span data-ttu-id="43e38-114">Zeigen Sie bei Bedarf den Wiedergabe Bereich des Fensters an.</span><span class="sxs-lookup"><span data-stu-id="43e38-114">Display the playback area of the window, if needed.</span></span>

 

 




