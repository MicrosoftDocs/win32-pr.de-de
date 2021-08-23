---
title: Die Meldungszuordnung
description: Die Meldungszuordnung
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Windows Media Player-Plug-Ins,Meldungszuordnung
- Plug-Ins, Meldungszuordnung
- Benutzeroberflächen-Plug-Ins, Meldungszuordnung
- Benutzeroberflächen-Plug-Ins, Meldungszuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec00689257ee60ada8f9bdf027b1cd34e43d243492e8d8ce5b5b38d2d89044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831573"
---
# <a name="the-message-map"></a>Die Meldungszuordnung

Das Plug-In-Fenster reagiert auf verschiedene Ereignisse durch Aufrufen von Methoden, die entsprechenden Ereignismeldungen zugeordnet sind. Der Assistent bietet eine Zuordnung, sodass OnPaint und OnEraseBackground zu den entsprechenden Zeiten aufgerufen werden. Um die Schaltfläche **Suchen zu** erstellen und darauf zu reagieren, wird der Meldungszuordnungsabschnitt wie folgt geändert:


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

[**Implementieren von CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




