---
description: Geräte Profile für Web Services (DPWS)-Hosts und-Clients kommunizieren über das Netzwerk, indem eine Reihe von SOAP-Nachrichten über UDP und HTTP verwendet wird.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Ermittlungs-und Metadatenaustausch-Nachrichten Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104218952"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Ermittlungs-und Metadatenaustausch-Nachrichten Muster

Geräte Profile für Web Services (DPWS)-Hosts und-Clients kommunizieren über das Netzwerk, indem eine Reihe von SOAP-Nachrichten über UDP und HTTP verwendet wird.

Das folgende Diagramm zeigt eine Übersicht über den erwarteten UDP-und HTTP-Datenverkehr zwischen einem DPWS-Host und-Client.

![Das Diagramm zeigt UDP-und HTTP-Datenverkehr zwischen einem DPWS-Host und-Client.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

[Hello](hello-message.md)- [](bye-message.md), bye [-, Test-,](probe-message.md) [Resolve](resolve-message.md)-und [Get](get--metadata-exchange--http-request-and-message.md) -Nachrichten werden ohne Netzwerkanfrage generiert. Diese Nachrichten werden verwendet, um den Gerätestatus anzukündigen oder eine Such Anforderung auszugeben. [Probe Matches](probematches-message.md), [resolvematches](resolvematches-message.md)und [GetResponse](getresponse--metadata-exchange--message.md) -Nachrichten werden als Antwort auf die Nachrichten "Probe", "auflösen" und "Get" generiert.

Die Nachrichten [Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md)und [resolvematches](resolvematches-message.md) werden immer über UDP ausgeführt. Ebenso erfolgen [Get](get--metadata-exchange--http-request-and-message.md) -und [GetResponse](getresponse--metadata-exchange--message.md) -metadatennachrichten immer über HTTP oder HTTPS. Test [-und](probe-message.md) [Probe Matches](probematches-message.md) -Nachrichten werden normalerweise über UDP übermittelt, aber über eine HTTP-oder HTTPS-Verbindung in einem gesteuerten Ermittlungs Szenario. Weitere Informationen zu gerichteten Ermittlungs Nachrichten Mustern finden Sie unter [Problembehandlung bei Anwendungen mithilfe der gesteuerten](troubleshooting-applications-using-directed-discovery.md)Ermittlung.

In der folgenden Liste wird die typische Nachrichten Sequenz angezeigt. Nicht alle Nachrichten sind obligatorisch.

1.  [Hello](hello-message.md) (Hallo)
2.  [Test](probe-message.md)
3.  [Probe Matches](probematches-message.md)
4.  [Beheben](resolve-message.md)
5.  [Resolvematches](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (metadatenaustauschanforderung)
7.  [GetResponse](getresponse--metadata-exchange--message.md)
8.  [Auf Wiedersehen](bye-message.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Webdiensten auf Geräten](about-web-services-for-devices.md)
</dt> </dl>

 

 



