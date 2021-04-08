---
title: Die Meldungs Zuordnung
description: Die Meldungs Zuordnung
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Windows Media Player-Plug-ins, Meldungs Zuordnung
- Plug-ins, Meldungs Zuordnung
- Benutzerschnittstellen-Plug-ins, Meldungs Zuordnung
- UI-Plug-ins, Meldungs Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037072"
---
# <a name="the-message-map"></a><span data-ttu-id="55caf-107">Die Meldungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="55caf-107">The Message Map</span></span>

<span data-ttu-id="55caf-108">Das Plug-in-Fenster antwortet auf verschiedene Ereignisse, indem Methoden aufgerufen werden, die entsprechenden Ereignismeldungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55caf-108">The plug-in window responds to various events by calling methods that are mapped to corresponding event messages.</span></span> <span data-ttu-id="55caf-109">Der Assistent stellt eine Zuordnung bereit, sodass OnPaint und onerasebackground zu den entsprechenden Zeitpunkten aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="55caf-109">The wizard provides a mapping so that OnPaint and OnEraseBackground will be called at the appropriate times.</span></span> <span data-ttu-id="55caf-110">Um die **Such** Schaltfläche zu erstellen und darauf zu reagieren, wird der Nachrichten Zuordnungs Abschnitt wie folgt geändert:</span><span class="sxs-lookup"><span data-stu-id="55caf-110">To create the **Search** button and to respond to clicks from it, the message map section is modified as follows:</span></span>


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a><span data-ttu-id="55caf-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55caf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55caf-112">**Implementieren von cpluginwindow**</span><span class="sxs-lookup"><span data-stu-id="55caf-112">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




