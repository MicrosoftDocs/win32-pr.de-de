---
title: Implementieren von CPluginWindow
description: Implementieren von CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Windows Media Player-Plug-Ins,CPluginWindow-Klasse
- Plug-Ins, CPluginWindow-Klasse
- Benutzeroberflächen-Plug-Ins,CPluginWindow-Klasse
- Benutzeroberflächen-Plug-Ins, CPluginWindow-Klasse
- CPluginWindow-Klasse
- Programmierhandbuch, Benutzeroberflächen-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6364d991fb219678d4f64b09ae4cd3df2526e77797093dcfff3a8dbce7f36101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748135"
---
# <a name="implementing-cpluginwindow"></a>Implementieren von CPluginWindow

Die CPluginWindow-Klasse stellt die Benutzeroberfläche für das Plug-In zur Verfügung. Im Fall des Suchbenutzeroberflächen-Plug-Ins enthält  diese Klasse den Code für die Schaltfläche Suchen und den Code, der die Suchseite startet, wenn auf die Schaltfläche geklickt wird.

Der Assistent bietet eine grundlegende Implementierung von CPluginWindow in der Headerdatei CPluginWindow.h. Um dies einfach zu halten, ändert das Plug-In für die Benutzeroberfläche für die Suche diese Datei direkt, obwohl umfangreiche Ergänzungen normalerweise in einer separaten CPluginWindow.cpp-Datei platziert würden.

In den folgenden Abschnitten wird beschrieben, was Sie zum Implementieren von CPluginWindow tun müssen:

-   [Die Meldungszuordnung](the-message-map.md)
-   [Der Konstruktor](the-constructor.md)
-   [Die OnPaint-Methode](the-onpaint-method.md)
-   [Die OnCreate-Methode](the-oncreate-method.md)
-   [Die OnSearch-Methode](the-onsearch-method.md)
-   [Die LaunchPage-Methode](the-launchpage-method.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Benutzeroberfläche Plug-Ins -Programmierhandbuch**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




