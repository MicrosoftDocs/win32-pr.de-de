---
description: Wenn der Client und der Host keine Metadaten austauschen können, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345804"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch

Wenn der Client und der Host keine Metadaten austauschen können, können ein generischer Host und Client durch den benutzerdefinierten Host und Client ersetzt werden, um das Problem zu beheben. Wenn die Geräteadresse oder die Geräte Metadaten nicht in der WSD-debugclientausgabe angezeigt werden, kann der Fehler von den angegebenen Transport Adressen oder der Netzwerkumgebung verursacht werden. Weitere Informationen zum generischen Host und Client finden Sie unter [Debugtools](debugging-tools.md).

Wenn überprüft wurde, ob ein generischer Host und ein Client sowohl WS-Discovery als auch http-Metadatenaustausch durchführen können, kann diese Diagnose Prozedur übersprungen und die Problembehandlung fortgesetzt werden, indem die Verfahren unter [Verwenden der WinHTTP-Protokollierung zum Überprüfen von Datenverkehr](using-winhttp-logging-to-verify-get-traffic.md)durchgeführt werden.

Wenn entweder der Host oder der Client eine Anwendung ist, die auf einem PC ausgeführt wird, sollte der generische Host oder Client im gleichen Sicherheitskontext wie der tatsächliche Host oder Client ausgeführt werden. Wenn der tatsächliche Host oder Client beispielsweise als Administrator ausgeführt wird, muss der generische Host oder Client als Administrator ausgeführt werden. Auch wenn der Host oder der Client ein eigenständiges Gerät ist, sollte es vollständig durch einen PC ersetzt werden, auf dem ein generischer Host oder Client in einem Sicherheitskontext ausgeführt wird, der unbegrenzten Netzwerk Zugriff garantiert (z. b. als Administrator).

**So verwenden Sie einen generischen Host und Client für die Problembehandlung von http-Metadatenaustausch**

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
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

Der WSD-Debugclient generiert möglicherweise eine Menge Ausgabe in einem Netzwerk mit vielen DPWS-Geräten. Die Ausgabe kann zur einfacheren Analyse an eine Datei umgeleitet werden. Geben Sie **Log Tee** *<filename>* an der WSD Debug Client-Eingabeaufforderung ein, um die Ausgabe an eine Datei umzuleiten. Die Ausgabe Umleitung kann beendet werden, indem Sie an der WSD-Debug-Client-Eingabeaufforderung " **Log Tee-Stopp**

Notieren Sie sich die Endpunkt Verweisadresse (EPR). Diese EPR-Adresse sollte mit der in Schritt 2 oben identifizierten Geräte-ID identisch sein. Vergewissern Sie sich außerdem, dass der WSD-Debugclient die Metadaten für das Gerät vollständig gedruckt hat. Die Geräte Metadaten beginnen mit `Metadata for host` und enden mit `End of metadata` .

Wenn die Geräte-ID und die Geräte Metadaten in der WSD-debugclientausgabe ordnungsgemäß angezeigt werden, ist der Anwendungsfehler wahrscheinlich nicht mit den angegebenen Transport Adressen, dem Betriebssystem oder der Netzwerkumgebung verknüpft. Ersetzen Sie den generischen Host und Client durch den benutzerdefinierten Host und Client, und setzen Sie die Problembehandlung fort, indem Sie die Schritte unter [Verwenden von WinHTTP-Protokollierung zum Überprüfen](using-winhttp-logging-to-verify-get-traffic.md)von

Wenn die Geräteadresse und die Geräte Metadaten nicht in der WSD-debugclientausgabe angezeigt werden, kann der Fehler eine oder mehrere der folgenden Gründe haben:

-   Die vom Host angekündigte Transport Adresse ist falsch oder falsch formatiert. Der WSD-Debugclient versucht, die Geräte Metadaten aus der URL zu erhalten, die im **xaddrs** -Element einer [Probe Matches](probematches-message.md) -oder [resolvematches](resolvematches-message.md) -Meldung angegeben ist. Die für den Metadatenaustausch verwendete URL wird in der WSD-debugclientausgabe angezeigt, die dem Ausdruck vorangestellt ist `Using xAddr` . Das folgende Beispiel zeigt die xaddrs, die für den Metadatenaustausch in der obigen WSD-debugclientausgabe verwendet werden.

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    Wenn die angegebenen xaddrs nicht den [xaddr-Validierungsregeln](xaddr-validation-rules.md)entsprechen, kann der WSD-Debugclient die Metadaten des Geräts nicht erhalten.

-   Die Anwendung wird im falschen Sicherheitskontext ausgeführt. Vergewissern Sie sich, dass die Anwendung die richtigen Anmelde Informationen verwendet und dass der Client und der Host über ausreichende Zugriffsberechtigungen für das Netzwerk verfügen.
-   Die Firewallkonfiguration ist falsch. Befolgen Sie die Anweisungen unter Überprüfen der [Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md) , um sicherzustellen, dass die Windows-Firewall-Einstellungen korrekt sind und keine anderen Regeln zum Löschen der Pakete vorhanden sind. Der Client und der Host können auch auf einen "unverfälschten" Computer kopiert werden (einer mit einer Standardinstallation des Betriebssystems, der noch nie einer Domäne hinzugefügt wurde), um den Fehler zu reproduzieren.
-   Eine IPSec-Richtlinie blockiert die Anwendung. Kopieren Sie den Client und den Host auf einen Computer, der keine IPSec-Richtlinien unterliegt, und versuchen Sie, den Fehler zu reproduzieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



