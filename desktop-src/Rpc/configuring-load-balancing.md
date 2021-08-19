---
title: Konfigurieren des Lastenausgleichs
description: Konfigurieren des Lastenausgleichs
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3560359bd5ad064dc270e0840845674b97b093af66796dc92f31f7a15170f467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931693"
---
# <a name="configuring-load-balancing"></a>Konfigurieren des Lastenausgleichs

Jeder RPC-Proxycomputer, der als Lastenausgleichsserverdienst (Load Balancing Server, LBS) fungieren soll, muss als LBS-Dienst mit Kenntnissen der Server in der Serverfarm konfiguriert werden. Optional kann die Standardressource festgelegt werden, und die Sicherheit von Proxy-zu-LBS- und LBS-zu-LBS-RPC-Aufrufen kann festgelegt werden. Diese Einstellungen werden wie unten beschrieben durch einen Satz **erforderlicher Registrierungsschlüssel** und **optionaler Registrierungsschlüssel** konfiguriert.

## <a name="required-registry-keys"></a>Erforderliche Registrierungsschlüssel

Zum Konfigurieren eines LBS-Servers sind mehrere Registrierungsschlüssel und -werte erforderlich. Wenn Schlüssel fehlen oder fehlerhaft eingegeben werden, wird ein Windows Ereignis protokolliert. Informationen zum protokollierten Ereignis finden Sie in der Beschreibung der einzelnen Schlüssel und Werte.

Zum Konfigurieren der Serverfarm muss ein Registrierungsschlüssel erstellt werden **HKLM \\ SOFTWARE Microsoft \\ Rpc \\ \\ RpcProxy** namens **LBSConfiguration**. Unter dem **LBSConfiguration-Schlüssel** wird ein Schlüssel für jede Ressource in der Serverfarm erstellt. Der Schlüsselname ist die Zeichenfolgendarstellung der GUID für die Ressource. Es muss mindestens ein Ressourcenschlüssel vorhanden sein, und diese Ressource ist identisch mit der [**UUID,**](./rpcdce/ns-rpcdce-uuid.md) die von Clients im Bindungshandle festgelegt [**wird(RPC BINDING \_ \_ HANDLE),**](rpc-binding-handle.md)wenn sie die RPC/HTTP-Bindung erstellen (weitere Informationen finden Sie unter [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). Unter jedem Ressourcen-UUID-Schlüssel muss ein **DWORD-Wert** namens ConfigurationType vorhanden sein, der die verwendete Konfiguration beschreibt. Es muss auch eine **REG \_ SZ** mit durch Semikolons getrennten Serverbezeichnern namens **ServerFarm** vorhanden sein. Die im **ServerFarm-Schlüssel** identifizierten Server sind die Server, die Mitglieder der Lastenausgleichsserverfarm sind.

Im Folgenden finden Sie eine ausführliche Aufschlüsselung der erforderlichen Registrierungsschlüssel und -werte:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration**

Registrierungsschlüssel. Der **LBSConfiguration-Schlüssel** ist der Registrierungsschlüssel, der die LBS-Konfiguration enthält. Dazu gehören die [**Ressourcen-UUIDs,**](./rpcdce/ns-rpcdce-uuid.md) für die ein Lastenausgleich erfolgen soll, der Konfigurationstyp für jede Ressource und die Server in den Serverfarmen, die am Lastenausgleich beteiligt sind. Wenn dieser Schlüssel fehlt oder ungültig ist, wird LBS nicht als konfiguriert betrachtet, und der LBS-Dienst wird nicht ausgeführt.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**

Registrierungsschlüssel. Der **Ressourcen-UUID-Schlüssel** identifiziert die Ressourcen-UUID, für die ein Lastenausgleich erfolgen soll. Diese Ressourcen-UUID entspricht der [**UUID,**](./rpcdce/ns-rpcdce-uuid.md) die Clients für das Bindungshandle [**, RPC BINDING \_ \_ HANDLE,**](rpc-binding-handle.md)festlegen. Es muss mindestens eine Ressourcen-UUID vorhanden sein, um einen Lastenausgleich zu erhalten. Es können mehrere Ressourcen-UUIDs vorhanden sein. Es kann nur eine Serverfarm vorhanden sein, und alle Endpunkte müssen sich auf allen Servern innerhalb der Serverfarm befinden. Wenn dieser Schlüssel nicht in eine gültige UUID analysiert werden kann, wird das **Ereignis RPCPROXY \_ EVENTLOG \_ LB INVALID \_ \_ KEY (0xC0000006)** im Windows Ereignisprotokoll protokolliert.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ConfigurationType**

DWORD. Das **ConfigurationType-DWORD** wird unter dem **Ressourcen-UUID-Schlüssel** gespeichert. Der einzige zulässige Wert ist 1. Wenn dieser Wert nicht 1 ist, wird das **Ereignis RPCPROXY \_ EVENTLOG \_ LB UNKNOWN \_ \_ CFG TYPE \_ (0xC0000007)** im Windows-Ereignisprotokoll protokolliert.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ServerFarm**

REG \_ SZ. Der **ServerFarm-Registrierungswert** enthält eine durch Semikolons getrennte Liste von Serverbezeichnern. Das Format für die Serverbezeichner lautet:

"ServerID1,ServerPort1,LBSPort1, \[ LBSPort2, ... LBSPortN \] ;"

Mehrere Serverbezeichner sollten im **Registrierungsschlüssel ServerFarm** aufgeführt werden. Sie müssen durch ein Semikolon getrennt werden. Die Felder, die Teil des Serverbezeichners sind, werden in der folgenden Tabelle beschrieben. Wenn dieses Feld nicht ordnungsgemäß analysiert werden kann, wird das **Ereignis RPCPROXY \_ EVENTLOG \_ LB BAD \_ \_ CONFIG ENTRY \_ (0xC0000008)** im Windows-Ereignisprotokoll protokolliert.



| Bezeichnerfeld | Anforderung | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Erforderlich    | Ein auflösbarer Netzwerkname für den Server. Dies kann ein DNS-Name, ein Netbios-Name oder eine IP-Adresse sein.                                                                                                                                                                                |
| ServerPort       | Optional    | Wenn angegeben, der Port, an dem der Server auf RPC-/HTTP-Verbindungen lauscht. Wenn keine Angabe erfolgt, wird die Endpunktzuordnung auf dem Servercomputer verwendet, um den Serverport zu finden.                                                                                                         |
| LBSPort          | Optional    | Wenn angegeben, portiert den , auf dem der Server auf LBS lauscht. Um diesen Schlüssel verwenden zu können, müssen die LBS-Schnittstellen mithilfe eines netsh RPC-Firewallbefehls auf einen statischen Endpunkt festgelegt werden. Beispiele für den Netsh-Befehl finden Sie unter Bewährte Methoden für den [Lastenausgleich.](load-balancing-best-practices.md) |



 

## <a name="optional-registry-keys"></a>Optionale Registrierungsschlüssel

Es gibt drei optionale Registrierungswerte zum Konfigurieren eines LBS-Servers. Die Schlüssel steuern in erster Linie die Sicherheitsstufe für Aufrufe an den und vom LBS-Dienst sowie die zu verwendende Standardressourcen-UUID. Im Folgenden sind optionale Werte angegeben:

Im Folgenden finden Sie eine ausführliche Aufschlüsselung der erforderlichen Registrierungsschlüssel und -werte:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Wenn das **NoSecurity-DWORD** nicht vorhanden oder auf 0 festgelegt ist, werden eingehende nicht sichere Aufrufe an den LBS-Dienst abgelehnt. Wenn vorhanden und nicht 0, werden eingehende nicht sichere Aufrufe an den LBS-Dienst nicht abgelehnt. Dieser Schlüssel wird beim Start des LBS-Diensts einmal gelesen.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Wenn **assumeResourceUUID** DWORD nicht vorhanden ist, erfolgt keine Änderung im LBS-Dienst. Wenn vorhanden, muss es mit einer gültigen [**UUID**](./rpcdce/ns-rpcdce-uuid.md)festgelegt werden. Diese **UUID** wird als Ressourcen-UUID für alle Verbindungen verwendet, die keine Ressourcen-UUID angeben. Dies wird häufig in Fällen verwendet, in denen Clients beim Erstellen der RPC/HTTP-Bindung keine Ressourcen-UUID angeben, aber ein Administrator einen Lastenausgleich für den RPC/HTTP-Datenverkehr zu einer Serverfarm durchführen möchte. Wenn dieser Schlüssel nicht in eine UUID analysiert werden kann, wird ein interner RPC-Fehler behoben, wodurch [**RPC \_ EXTENDED ERROR \_ \_ INFO**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) generiert wird, wenn er aktiviert ist.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Wenn das **NoSecurity-DWORD** nicht angezeigt oder auf 0 festgelegt ist, verfügen alle ausgehenden Aufrufe an LBS-Dienste über Sicherheit. Wenn vorhanden und nicht auf 0 festgelegt, haben alle ausgehenden Aufrufe an LBS-Dienste keine Sicherheit. Stellen Sie sicher, dass diese Einstellung mit der **Einstellung HKLM \\ SOFTWARE Microsoft \\ Rpc \\ \\ RpcProxy \\ LBSConfiguration \\ NoSecurity** übereinstimmt.

 

 