---
description: Wenn client und host sich im Netzwerk nicht sehen können, können der benutzerdefinierte Host und der Client durch einen generischen Host und client ersetzt werden, um das Problem zu beheben.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6af77529116e21848e22812e04322273e08f1f0cf4d107787b4039b2442b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991490"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery

Wenn client und host sich im Netzwerk nicht sehen können, können der benutzerdefinierte Host und der Client durch einen generischen Host und client ersetzt werden, um das Problem zu beheben. Wenn die Geräteadresse nicht in der Ausgabe des WSD-Debugclients angezeigt wird, verursacht die Netzwerkumgebung wahrscheinlich den Fehler. Weitere Informationen zum generischen Host und Client finden Sie unter [Debugtools.](debugging-tools.md)

Wenn der Host oder Client eine Anwendung ist, die auf einem PC ausgeführt wird, sollte der generische Host oder Client im gleichen Sicherheitskontext wie der tatsächliche Host oder Client ausgeführt werden. Wenn der tatsächliche Host oder Client beispielsweise als Administrator ausgeführt wird, muss der generische Host oder Client als Administrator ausgeführt werden. Wenn es sich bei dem Host oder Client um ein eigenständiges Gerät handelt, sollte es vollständig durch einen PC ersetzt werden, auf dem ein generischer Host oder Client ausgeführt wird.

**So verwenden Sie einen generischen Host und Client zur Problembehandlung bei der UDP-WS-Ermittlung**

1.  Öffnen Sie ein Eingabeaufforderungsfenster.
2.  Führen Sie den folgenden Befehl aus: **WSDDebug \_host.exe /mode metadata /start**

    > [!Note]  
    > Möglicherweise wird **ein Windows-Sicherheit** Dialogfeld Warnung angezeigt. Klicken Sie in diesem Falle auf **Blockierung aufheben,** um die Ausführung des WSD-Debughosts zuzulassen.

     

    Dieser Befehl generiert eine Ausgabe ähnlich der folgenden. Notieren Sie sich die Geräte-ID.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Führen Sie den folgenden Befehl aus: **WSDDebug \_client.exe /mode metadata /hello off /resolve** *<id>* . Ersetzen Sie durch *<id>* die in Schritt 2 identifizierte Geräte-ID.
    > [!Note]  
    > Möglicherweise wird **ein Windows-Sicherheit** Dialogfeld Warnung angezeigt. Wenn ja, klicken Sie auf **Blockierung aufheben,** um die Ausführung des WSD-Debugclients zuzulassen.

     

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

Der WSD-Debugclient generiert möglicherweise viele Ausgaben in einem Netzwerk mit vielen DPWS-Geräten. Die Ausgabe kann zur einfacheren Analyse an eine Datei umgeleitet werden. Geben Sie **log tee** an *<filename>* der WSD-Debugclientaufforderung ein, um die Ausgabe an eine Datei umzuleiten. Die Ausgabeumleitung kann beendet werden, indem Sie an der Eingabeaufforderung des WSD-Debugclients log **tee stop** eingeben.

Notieren Sie sich die Adresse des Endpunktverweis (EPR). Diese EPR-Adresse sollte mit der in Schritt 2 oben angegebenen Geräte-ID übereinstimmen. Wenn dies der Fall ist, hängt der Anwendungsfehler wahrscheinlich nicht mit dem Betriebssystem oder der Netzwerkumgebung zusammen. Ersetzen Sie den generischen Host und Client durch den benutzerdefinierten Host und Client, und setzen Sie die Problembehandlung fort, indem Sie die Schritte unter Verwenden des [WSD-Debugclients zum Überprüfen von Multicastdatenverkehr](using-wsddebug-client-to-verify-multicast-traffic.md)befolgen.

Wenn die Geräte-ID nicht mit der EPR-Adresse übereinstimmt, hängt der Anwendungsfehler wahrscheinlich mit dem Betriebssystem oder der Netzwerkumgebung zusammen. Der Fehler kann eine oder mehrere der folgenden Ursachen haben:

-   Die Anwendung wird im falschen Sicherheitskontext ausgeführt. Stellen Sie sicher, dass die Anwendung die richtigen Anmeldeinformationen verwendet und der Client und der Host über ausreichende Berechtigungen für den Zugriff auf das Netzwerk verfügen.
-   Die Firewallkonfiguration ist falsch. Befolgen Sie die Anweisungen unter [Überprüfen des Adapters und der Firewall Einstellungen,](inspecting-adapter-and-firewall-settings.md) um zu überprüfen, ob die Windows Firewalleinstellungen korrekt sind und dass keine anderen Regeln zum Löschen der Pakete vorhanden sind. Der Client und der Host können auch auf einen "klammer" Computer kopiert werden (einen Computer mit einer Standardbetriebssysteminstallation, die noch nie in eine Domäne eingebunden wurde), um zu versuchen, den Fehler zu reproduzieren.
-   Eine IPSec-Richtlinie blockiert die Anwendung. Kopieren Sie den Client und den Host auf einen Computer, der nicht den IPSec-Richtlinien unterliegt, und versuchen Sie, den Fehler zu reproduzieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI–Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



