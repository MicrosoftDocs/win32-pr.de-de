---
title: Implementieren von cpluginwindow
description: Implementieren von cpluginwindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Windows Media Player-Plug-ins, cpluginwindow-Klasse
- Plug-ins, cpluginwindow-Klasse
- Benutzeroberflächen-Plug-ins, cpluginwindow-Klasse
- UI-Plug-ins, cpluginwindow-Klasse
- Cpluginwindow-Klasse
- Programmier Handbuch, Benutzerschnittstellen-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709072"
---
# <a name="implementing-cpluginwindow"></a>Implementieren von cpluginwindow

Die cpluginwindow-Klasse stellt die Benutzeroberfläche für das Plug-in bereit. Im Fall des Such Benutzeroberflächen-Plug-Ins enthält diese Klasse den Code für die **Such** Schaltfläche und den Code, mit dem die Suchseite gestartet wird, wenn auf die Schaltfläche geklickt wird.

Der Assistent stellt eine grundlegende Implementierung von cpluginwindow in der Header Datei "cpluginwindow. h" bereit. Um dies zu gewährleisten, ändert das Such Benutzeroberflächen-Plug-in diese Datei direkt, obwohl umfassende Ergänzungen normalerweise in einer separaten cpluginwindow. cpp-Datei platziert werden.

In den folgenden Abschnitten wird beschrieben, was Sie tun müssen, um cpluginwindow zu implementieren:

-   [Die Meldungs Zuordnung](the-message-map.md)
-   [Der Konstruktor](the-constructor.md)
-   [Die OnPaint-Methode](the-onpaint-method.md)
-   [Die OnCreate-Methode](the-oncreate-method.md)
-   [Die onSearch-Methode](the-onsearch-method.md)
-   [Die LaunchPage-Methode](the-launchpage-method.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für Benutzeroberflächen-Plug-ins**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




