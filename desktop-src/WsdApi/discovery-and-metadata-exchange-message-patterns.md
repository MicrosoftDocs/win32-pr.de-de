---
description: DpWS-Hosts (Device Profile for Web Services) kommunizieren über das Netzwerk mithilfe einer Reihe von SOAP-Nachrichten über UDP und HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Ermittlung und Metadaten Exchange Nachrichtenmustern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b41267e86358a9d6e263f4bc8971632f1061eb1c94d1e64cc76d65020ce255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856794"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Ermittlung und Metadaten Exchange Nachrichtenmustern

DpWS-Hosts (Device Profile for Web Services) kommunizieren über das Netzwerk mithilfe einer Reihe von SOAP-Nachrichten über UDP und HTTP.

Das folgende Diagramm zeigt eine Übersicht über den erwarteten UDP- und HTTP-Datenverkehr zwischen einem DPWS-Host und -Client.

![Diagramm: UDP- und HTTP-Datenverkehr zwischen einem DPWS-Host und -Client](images/ws-discovery-and-metadata-exchange-message-patterns.png)

[Hello-,](hello-message.md) [Bye-,](bye-message.md) [Probe-, Resolve-](resolve-message.md)und [Get-Nachrichten](get--metadata-exchange--http-request-and-message.md) werden alle ohne Netzwerkankündigung generiert. [](probe-message.md) diese Nachrichten werden verwendet, um den Gerätestatus ankündigen oder eine Suchanforderung aus zu stellen. [ProbeMatches-,](probematches-message.md) [ResolveMatches-](resolvematches-message.md)und [GetResponse-Meldungen](getresponse--metadata-exchange--message.md) werden als Reaktion auf Probe-, Resolve- und Get-Meldungen generiert.

[Hello-,](hello-message.md) [Bye-,](bye-message.md) [Resolve-](resolve-message.md)und [ResolveMatches-Meldungen](resolvematches-message.md) treten immer über UDP auf. Ebenso werden [Get-](get--metadata-exchange--http-request-and-message.md) und [GetResponse-Metadatenmeldungen](getresponse--metadata-exchange--message.md) immer über HTTP oder HTTPS gesendet. [Probe-](probe-message.md) [und ProbeMatches-Nachrichten](probematches-message.md) werden normalerweise über UDP übertragen, aber in einem szenariogesteuerten Ermittlung über eine HTTP- oder HTTPS-Verbindung. Weitere Informationen zu Mustern von gerichteten Ermittlungsnachrichten finden Sie unter [Problembehandlung bei Anwendungen mithilfe der gerichteten Ermittlung.](troubleshooting-applications-using-directed-discovery.md)

In der folgenden Liste ist die typische Sequenz von Nachrichten im Netzwerk aufgeführt. Nicht alle Nachrichten sind obligatorisch.

1.  [Hello](hello-message.md)
2.  [Test](probe-message.md)
3.  [ProbeMatches](probematches-message.md)
4.  [Beheben](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (Metadatenaustauschanforderung)
7.  [Getresponse](getresponse--metadata-exchange--message.md)
8.  [Auf Wiedersehen](bye-message.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Webdiensten auf Geräten](about-web-services-for-devices.md)
</dt> </dl>

 

 



