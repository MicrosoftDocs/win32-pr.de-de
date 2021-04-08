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
# <a name="the-message-map"></a>Die Meldungs Zuordnung

Das Plug-in-Fenster antwortet auf verschiedene Ereignisse, indem Methoden aufgerufen werden, die entsprechenden Ereignismeldungen zugeordnet sind. Der Assistent stellt eine Zuordnung bereit, sodass OnPaint und onerasebackground zu den entsprechenden Zeitpunkten aufgerufen werden. Um die **Such** Schaltfläche zu erstellen und darauf zu reagieren, wird der Nachrichten Zuordnungs Abschnitt wie folgt geändert:


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von cpluginwindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




