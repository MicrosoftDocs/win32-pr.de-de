---
description: Ab Windows Vista unterstützt der Dienststeuerungs-Manager (Service Control Manager, SCM) Remoteprozeduraufrufe sowohl über RPC/TCP (Transmission Control Protocol) als auch über Named Pipes (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Dienste und RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d4ddfe95e114a972c600c9bef44864aa99fbe4ec412312d03e08fa7d7fe15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888557"
---
# <a name="services-and-rpctcp"></a>Dienste und RPC/TCP

Ab Windows Vista unterstützt der Dienststeuerungs-Manager (Service Control Manager, SCM) Remoteprozeduraufrufe sowohl über RPC/TCP (Transmission Control Protocol) als auch über Named Pipes (RPC/NP). Clientseitige SCM-Funktionen verwenden standardmäßig RPC/TCP.

RPC/TCP ist für die meisten Anwendungen geeignet, die SCM-Funktionen remote verwenden, z. B. Remoteverwaltungs- oder Überwachungstools. Aus Kompatibilitäts- und Leistungssteigerungs-Grund müssen einige Anwendungen rpc/TCP jedoch möglicherweise deaktivieren, indem sie die in diesem Thema beschriebenen Registrierungswerte festlegen.

Wenn ein Dienst eine Remote-SCM-Funktion aufruft, versucht der clientseitige SCM zunächst, RPC/TCP für die Kommunikation mit dem serverseitigen SCM zu verwenden. Wenn auf dem Server eine Version von Windows ausgeführt wird, die RPC/TCP unterstützt und RPC/TCP-Datenverkehr zulässt, wird die RPC/TCPP-Verbindung erfolgreich hergestellt. Wenn auf dem Server eine Version von Windows ausgeführt wird, die RPC/TCP nicht unterstützt oder RPC/TCP unterstützt, aber hinter einer Firewall ausgeführt wird, die nur Named Pipe-Datenverkehr zulässt, kommt es bei der RPC/TCP-Verbindung zu einem Zeitbruch, und der SCM unterstütz die Verbindung mit RPC/NP erneut. Dies wird letztendlich erfolgreich sein, kann jedoch einige Zeit (in der Regel mehr als 20 Sekunden) dauern, sodass die [**OpenSCManager-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) blockiert erscheint.

TCP enthält keine Benutzeranmeldeinformationen, die mit einem **net use-Befehl angegeben** wurden. Wenn RPC/TCP aktiviert ist  undsc.exewird, um auf den angegebenen Dienst zu zugreifen, kann der Befehl daher fehlschlagen, wenn der Zugriff verweigert wird. Das Deaktivieren von RPC/TCP auf Clientseite bewirkt, dass der **sc.exe-Befehl** eine Named Pipe verwendet, die Benutzeranmeldeinformationen enthält, sodass der Befehl erfolgreich ausgeführt wird. Weitere Informationen zu sc.exe sie unter [Steuern eines Diensts mit sc](controlling-a-service-using-sc.md).

> [!Note]  
> Ein Dienst sollte keine expliziten Anmeldeinformationen für einen **net use-Befehl** bereitstellen, da diese Anmeldeinformationen möglicherweise versehentlich außerhalb der Dienstgrenzen freigegeben werden. Stattdessen sollte der Dienst [clientpersonation verwenden,](/windows/desktop/SecAuthZ/client-impersonation) um die Identität des Benutzers zu imitieren.

 

### <a name="rpctcp-registry-values"></a>RPC/TCP-Registrierungswerte

RPC/TCP wird durch die Registrierungswerte **SCMApiConnectionParam,** **DisableRPCOverTCP** und **DisableRemoteScmEndpoints** gesteuert, die sich alle unter dem **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control-Schlüssel** befinden. Alle diese Werte haben einen REG \_ DWORD-Datentyp. Die folgenden Verfahren zeigen, wie sie diese Registrierungswerte verwenden, um RPC/TCP zu steuern.

Im folgenden Verfahren wird beschrieben, wie RPC/TCP auf clientseitiger Seite deaktiviert wird.

**So deaktivieren Sie RPC/TCP auf Clientseite**

1.  Kombinieren Sie **den Registrierungswert SCMApiConnectionParam** mit dem Maskenwert 0x80000000.
2.  Starten Sie die Anwendung neu, die die [**OpenSCManager-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) aufruft.

Im folgenden Verfahren wird beschrieben, wie TCP auf Serverseite deaktiviert wird.

**So deaktivieren Sie TCP auf Serverseite**

1.  Legen Sie **den Registrierungswert DisableRPCOverTCP** auf 1 fest.
2.  Starten Sie den Server neu.

Im folgenden Verfahren wird beschrieben, wie Sie sowohl RPC/TCP als auch RPC/NP auf dem Server deaktivieren (z. B. um die Angriffsfläche zu verringern).

**So deaktivieren Sie sowohl RPC/TCP als auch RPC/NP auf dem Server**

1.  Legen Sie **den Registrierungswert DisableRemoteScmEndpoints auf** 1 fest.
2.  Starten Sie den Server neu.

Der **Registrierungswert SCMApiConnectionParam** kann auch verwendet werden, um das RPC/TCP-Time out-Intervall in Millisekunden anzugeben. Beispielsweise gibt der Wert 30.000 ein Time out-Intervall von 30 Sekunden an. Der Standardwert ist 21.000 (21 Sekunden).

 

 
