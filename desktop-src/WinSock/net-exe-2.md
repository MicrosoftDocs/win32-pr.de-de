---
description: Net.exe können zum Abbrechen und Starten des IPv6-Protokolls verwendet werden.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862552"
---
# <a name="netexe"></a>Net.exe

Net.exe können zum Abbrechen und Starten des IPv6-Protokolls verwendet werden. Durch einen Neustart von IPv6 wird das Protokoll neu initialisiert, als wenn der Computer neu gestartet wird, wodurch die Schnittstellen Nummern geändert werden können. Net.exe weist viele Unterbefehle auf. Die folgenden Befehle sind für IPv6 relevant:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**NET-tcpip6**
</dt> <dd>

Beendet das IPv6-Protokoll und entlädt es aus dem Arbeitsspeicher. Dieser Befehl schlägt fehl, wenn IPv6-Sockets geöffnet sind.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET Start tcpip6**
</dt> <dd>

Startet das IPv6-Protokoll, wenn es beendet wurde. Wenn eine neue Tcpip6.sys Treiberdatei im Verzeichnis "% SystemRoot% System32 Drivers" vorhanden ist \\ \\ , wird diese Treiberdatei geladen.

</dd> </dl>

 

 



