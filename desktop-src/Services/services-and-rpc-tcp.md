---
description: Ab Windows Vista unterstützt der Dienststeuerungs-Manager (Service Control Manager, SCM) Remote Prozedur Aufrufe über RPC/TCP (Transmission Control Protocol) und Named Pipes (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Dienste und RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363715"
---
# <a name="services-and-rpctcp"></a>Dienste und RPC/TCP

Ab Windows Vista unterstützt der Dienststeuerungs-Manager (Service Control Manager, SCM) Remote Prozedur Aufrufe über RPC/TCP (Transmission Control Protocol) und Named Pipes (RPC/NP). Client seitige SCM-Funktionen verwenden standardmäßig RPC/TCP.

RPC/TCP ist für die meisten Anwendungen geeignet, die SCM-Funktionen Remote verwenden, z. b. Remote Verwaltung oder Überwachungstools. Aus Kompatibilitätsgründen müssen einige Anwendungen jedoch möglicherweise RPC/TCP deaktivieren, indem Sie die in diesem Thema beschriebenen Registrierungs Werte festlegen.

Wenn ein Dienst eine Remote-SCM-Funktion aufruft, versucht der Client seitige SCM zunächst, RPC/TCP für die Kommunikation mit dem serverseitigen SCM zu verwenden. Wenn auf dem Server eine Version von Windows ausgeführt wird, die RPC/TCP unterstützt und RPC/TCP-Datenverkehr zulässt, wird die RPC/tcpp-Verbindung erfolgreich hergestellt. Wenn auf dem Server eine Version von Windows ausgeführt wird, die RPC/TCP nicht unterstützt, oder RPC/TCP unterstützt, aber eine Firewall verwendet, die nur Named Pipe-Datenverkehr zulässt, tritt für die RPC-/TCP-Verbindung ein Timeout auf, und der SCM versucht erneut, die Verbindung mit RPC/NP herzustellen. Dies ist zwar erfolgreich, kann jedoch einige Zeit in Anspruch nehmen (in der Regel mehr als 20 Sekunden), wodurch die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion blockiert wird.

TCP führt keine Benutzer Anmelde Informationen ein, die mit einem **net use** -Befehl angegeben werden. Wenn RPC/TCP aktiviert ist und **sc.exe** verwendet wird, um auf den angegebenen Dienst zuzugreifen, schlägt der Befehl daher möglicherweise fehl, und der Zugriff wird verweigert. Das Deaktivieren von RPC/TCP auf der Clientseite bewirkt, dass der **sc.exe** Befehl eine Named Pipe verwendet, die Benutzer Anmelde Informationen enthält, sodass der Befehl erfolgreich ausgeführt wird. Weitere Informationen zu sc.exe finden [Sie Untersteuern eines Dienstanbieter mit SC](controlling-a-service-using-sc.md).

> [!Note]  
> Ein Dienst sollte keinen expliziten Anmelde Informationen für einen **net use** -Befehl bereitstellen, da diese Anmelde Informationen versehentlich außerhalb der Dienst Grenzen freigegeben werden können. Stattdessen sollte der Dienst [Client](/windows/desktop/SecAuthZ/client-impersonation) Identitätswechsel verwenden, um die Identität des Benutzers anzunehmen.

 

### <a name="rpctcp-registry-values"></a>RPC/TCP-Registrierungs Werte

RPC/TCP wird von den Registrierungs Werten " **scmapiconnectionparam**", " **disablerpcovertcp**" und " **disableremotescmendpoints** " gesteuert, die alle unter dem **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** Key sind. Alle diese Werte haben einen reg \_ DWORD-Datentyp. In den folgenden Verfahren wird gezeigt, wie Sie diese Registrierungs Werte zum Steuern von RPC/TCP verwenden.

Im folgenden Verfahren wird beschrieben, wie Sie RPC/TCP auf Clientseite deaktivieren.

**So deaktivieren Sie RPC/TCP auf Clientseite**

1.  Kombinieren Sie den **scmapiconnectionparam** -Registrierungs Wert mit dem Maskenwert 0x80000000.
2.  Starten Sie die Anwendung neu, die die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion aufruft.

Im folgenden Verfahren wird beschrieben, wie Sie TCP auf Serverseite deaktivieren.

**So deaktivieren Sie TCP auf der Serverseite**

1.  Legen Sie den Registrierungs Wert **disablerpcovertcp** auf 1 fest.
2.  Starten Sie den Server neu.

Im folgenden Verfahren wird beschrieben, wie sowohl RPC/TCP als auch RPC/NP auf dem Server deaktiviert werden (z. b. um die Angriffsfläche zu verringern).

**So deaktivieren Sie sowohl RPC/TCP als auch RPC/NP auf dem Server**

1.  Legen Sie den Registrierungs Wert **disableremotescmendpoints** auf 1 fest.
2.  Starten Sie den Server neu.

Der **scmapiconnectionparam** -Registrierungs Wert kann auch verwendet werden, um das RPC/TCP-Timeout Intervall (in Millisekunden) anzugeben. Der Wert 30.000 gibt z. b. ein Timeout Intervall von 30 Sekunden an. Der Standardwert ist 21.000 (21 Sekunden).

 

 
