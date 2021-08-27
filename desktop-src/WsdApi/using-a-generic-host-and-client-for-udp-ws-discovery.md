---
description: Wenn sich Client und Host im Netzwerk nicht gegenseitig sehen können, können ein generischer Host und ein generischer Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b9f42cd76e54c3ee04a3299e9f23eecbfdd73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883078"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery

Wenn sich Client und Host im Netzwerk nicht gegenseitig sehen können, können ein generischer Host und ein generischer Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben. Wenn die Geräteadresse nicht in der Ausgabe des WSD-Debugclients angezeigt wird, verursacht die Netzwerkumgebung wahrscheinlich den Fehler. Weitere Informationen zum generischen Host und Client finden Sie unter [Debugtools](debugging-tools.md).

Wenn es sich bei dem Host oder Client um eine Anwendung handelt, die auf einem PC ausgeführt wird, sollte der generische Host oder Client im gleichen Sicherheitskontext wie der tatsächliche Host oder Client ausgeführt werden. Wenn der tatsächliche Host oder Client beispielsweise als Administrator ausgeführt wird, muss der generische Host oder Client als Administrator ausgeführt werden. Wenn es sich bei dem Host oder Client um ein eigenständiges Gerät handelt, sollte es vollständig durch einen PC ersetzt werden, auf dem ein generischer Host oder Client ausgeführt wird.

**So verwenden Sie einen generischen Host und Client für die Problembehandlung bei der UDP-WS-Ermittlung**

1.  Öffnen Sie ein Eingabeaufforderungsfenster.
2.  Führen Sie den folgenden Befehl aus: **WSDDebug \_host.exe /mode metadata /start**

    > [!Note]  
    > Möglicherweise **wird Windows-Sicherheit Dialogfeld** Warnung angezeigt. Wenn ja, klicken Sie **auf Blockierung** entsperren, um die Ausführung des WSD-Debughosts zu ermöglichen.

     

    Dieser Befehl generiert eine Ausgabe ähnlich der folgenden. Notieren Sie sich die Geräte-ID.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Führen Sie den folgenden Befehl aus: **WSDDebug \_client.exe /mode metadata /hello off /resolve** *&lt; id &gt;*. Ersetzen *&lt; Sie id &gt;* durch die in Schritt 2 identifizierte Geräte-ID.
    > [!Note]  
    > Möglicherweise **wird Windows-Sicherheit Dialogfeld** Warnung angezeigt. Wenn ja, klicken Sie **auf Blockierung** entsperren, um die Ausführung des WSD-Debugclients zu ermöglichen.

     

Der WSD-Debugclient generiert eine Ausgabe ähnlich der folgenden.

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
```

Der WSD-Debugclient generiert möglicherweise viele Ausgaben in einem Netzwerk mit vielen DPWS-Geräten. Die Ausgabe kann zur einfacheren Analyse an eine Datei umgeleitet werden. Geben **Sie an der WSD-Debugclient-Eingabeaufforderung** log tee *&lt; filename &gt;* ein, um die Ausgabe an eine Datei umzuleiten. Die Ausgabeumleitung kann beendet werden, indem Sie **log tee stop an** der WSD Debug Client-Eingabeaufforderung eingeben.

Notieren Sie sich die Adresse des Endpunktverweises (Endpoint Reference, EPR). Diese EPR-Adresse sollte mit der geräte-ID übereinstimmen, die in Schritt 2 oben identifiziert wurde. Wenn dies der Fall ist, bezieht sich der Anwendungsfehler wahrscheinlich nicht auf das Betriebssystem oder die Netzwerkumgebung. Ersetzen Sie den generischen Host und Client durch den benutzerdefinierten Host und Client, und fahren Sie mit der Problembehandlung fort, indem Sie die Schritte unter Verwenden des WSD-Debugclients zum Überprüfen des [Multicastdatenverkehrs durchführen.](using-wsddebug-client-to-verify-multicast-traffic.md)

Wenn die Geräte-ID nicht mit der EPR-Adresse übereinstimmen, bezieht sich der Anwendungsfehler wahrscheinlich auf das Betriebssystem oder die Netzwerkumgebung. Der Fehler kann eine oder mehrere der folgenden Ursachen haben:

-   Die Anwendung wird im falschen Sicherheitskontext ausgeführt. Stellen Sie sicher, dass die Anwendung die richtigen Anmeldeinformationen verwendet und dass client und host über ausreichende Berechtigungen für den Zugriff auf das Netzwerk verfügen.
-   Die Firewallkonfiguration ist falsch. Befolgen Sie die Anweisungen unter Überprüfen von Adapter- und [Firewall-Einstellungen,](inspecting-adapter-and-firewall-settings.md) um sicherzustellen, dass die Windows Firewall-Einstellungen richtig sind und keine anderen Regeln zum Löschen der Pakete gelten. Client und Host können auch auf einen "ursprünglichen" Computer kopiert werden (einer mit einer Standardinstallation des Betriebssystems, die nie einer Domäne beigetreten ist), um zu versuchen, den Fehler zu reproduzieren.
-   Eine IPSec-Richtlinie blockiert die Anwendung. Kopieren Sie den Client und den Host auf einen Computer, der nicht IPSec-Richtlinien unterliegt, und versuchen Sie, den Fehler zu reproduzieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI – Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



