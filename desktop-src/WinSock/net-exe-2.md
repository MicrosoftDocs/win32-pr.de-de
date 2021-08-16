---
description: Net.exe können verwendet werden, um das IPv6-Protokoll zu beenden und zu starten.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ab08a69590d6cf53a42096bf12d2e8657c571fd27b637feca4c51c61354225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741077"
---
# <a name="netexe"></a>Net.exe

Net.exe können verwendet werden, um das IPv6-Protokoll zu beenden und zu starten. Durch den Neustart von IPv6 wird das Protokoll erneut initialisiert, als ob der Computer neu gestartet würde, was die Schnittstellennummern ändern kann. Net.exe verfügt über viele Unterkombinationen. Die folgenden Befehle sind für IPv6 relevant:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**
</dt> <dd>

Beendet das IPv6-Protokoll und entlädt es aus dem Arbeitsspeicher. Dieser Befehl schlägt fehl, wenn IPv6-Sockets geöffnet sind.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**
</dt> <dd>

Startet das IPv6-Protokoll, wenn es beendet wurde. Wenn eine neue Tcpip6.sys Treiberdatei im Verzeichnis %systemroot% \\ System32 Drivers vorhanden \\ ist, wird diese Treiberdatei geladen.

</dd> </dl>

 

 



