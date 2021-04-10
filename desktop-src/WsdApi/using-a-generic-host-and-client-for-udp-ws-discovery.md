---
description: Wenn der Client und der Host sich nicht im Netzwerk befinden, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214978"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery

Wenn der Client und der Host sich nicht im Netzwerk befinden, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben. Wenn die Geräteadresse nicht in der WSD-debugclientausgabe angezeigt wird, verursacht die Netzwerkumgebung wahrscheinlich den Fehler. Weitere Informationen zum generischen Host und Client finden Sie unter [Debugtools](debugging-tools.md).

Wenn entweder der Host oder der Client eine Anwendung ist, die auf einem PC ausgeführt wird, sollte der generische Host oder Client im gleichen Sicherheitskontext wie der tatsächliche Host oder Client ausgeführt werden. Wenn der tatsächliche Host oder Client beispielsweise als Administrator ausgeführt wird, muss der generische Host oder Client als Administrator ausgeführt werden. Auch wenn der Host oder der Client ein eigenständiges Gerät ist, sollte es vollständig durch einen PC ersetzt werden, auf dem ein generischer Host oder Client ausgeführt wird.

**So verwenden Sie einen generischen Host und Client für die Problembehandlung von UDP-WS-Discovery**

1.  Öffnen Sie ein Eingabeaufforderungsfenster.
2.  Führen Sie den folgenden Befehl aus: **wsddebug \_host.exe/Mode Metadata/Start**

    > [!Note]  
    > Möglicherweise wird ein Dialogfeld mit der **Windows-Sicherheitswarnung** angezeigt. Wenn dies der Fall ist **, klicken Sie auf Entsperren** , um das Ausführen des WSD-debughosts zuzulassen.

     

    Dieser Befehl generiert eine Ausgabe ähnlich der folgenden. Notieren Sie sich die Geräte-ID.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Führen Sie den folgenden Befehl **aus: wsddebug \_client.exe/Mode Metadata/Hello off/Resolve** *<id>* . Ersetzen Sie *<id>* durch die in Schritt 2 identifizierte Geräte-ID.
    > [!Note]  
    > Möglicherweise wird ein Dialogfeld mit der **Windows-Sicherheitswarnung** angezeigt. Wenn dies der Fall ist **, klicken Sie auf Entsperren** , um das Ausführen des WSD-Debugclients zuzulassen.

     

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

Der WSD-Debugclient generiert möglicherweise eine Menge Ausgabe in einem Netzwerk mit vielen DPWS-Geräten. Die Ausgabe kann zur einfacheren Analyse an eine Datei umgeleitet werden. Geben Sie **Log Tee** *<filename>* an der WSD Debug Client-Eingabeaufforderung ein, um die Ausgabe an eine Datei umzuleiten. Die Ausgabe Umleitung kann beendet werden, indem Sie an der WSD-Debug-Client-Eingabeaufforderung " **Log Tee-Stopp**

Notieren Sie sich die Endpunkt Verweisadresse (EPR). Diese EPR-Adresse sollte mit der in Schritt 2 oben identifizierten Geräte-ID identisch sein. Wenn dies der Fall ist, ist der Anwendungsfehler wahrscheinlich nicht mit dem Betriebssystem oder der Netzwerkumgebung verknüpft. Ersetzen Sie den generischen Host und den generischen Client durch den benutzerdefinierten Host und Client, und setzen Sie die Problembehandlung fort, indem Sie die Schritte unter [Verwenden des WSD-Debugclients zum Überprüfen](using-wsddebug-client-to-verify-multicast-traffic.md)

Wenn die Geräte-ID nicht mit der EPR-Adresse identisch ist, ist der Anwendungsfehler wahrscheinlich mit dem Betriebssystem oder der Netzwerkumgebung verknüpft. Der Fehler kann eine oder mehrere der folgenden Gründe haben:

-   Die Anwendung wird im falschen Sicherheitskontext ausgeführt. Vergewissern Sie sich, dass die Anwendung die richtigen Anmelde Informationen verwendet und dass der Client und der Host über ausreichende Zugriffsberechtigungen für das Netzwerk verfügen.
-   Die Firewallkonfiguration ist falsch. Befolgen Sie die Anweisungen unter Überprüfen der [Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md) , um sicherzustellen, dass die Windows-Firewall-Einstellungen korrekt sind und keine anderen Regeln zum Löschen der Pakete vorhanden sind. Der Client und der Host können auch auf einen "unverfälschten" Computer kopiert werden (einer mit einer Standardinstallation des Betriebssystems, der noch nie einer Domäne hinzugefügt wurde), um den Fehler zu reproduzieren.
-   Eine IPSec-Richtlinie blockiert die Anwendung. Kopieren Sie Client und Host auf einen Computer, der nicht den IPSec-Richtlinien unterliegt, und versuchen Sie, den Fehler zu reproduzieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



