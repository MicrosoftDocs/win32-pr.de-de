---
title: Konfigurieren des Lasten Ausgleichs
description: Konfigurieren des Lasten Ausgleichs
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82dbfc23e491d53a6687b50aa77b23878ce52ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316239"
---
# <a name="configuring-load-balancing"></a>Konfigurieren des Lasten Ausgleichs

Jeder RPC-Proxy Computer, der als Load Balancing Server (lbs)-Dienst fungieren soll, muss als lbs-Dienst konfiguriert werden, der über Kenntnisse der Server in der Server Farm verfügt. Optional kann die Standardressource festgelegt werden, und die Sicherheit von Proxy-zu-lbs-und lbs-RPC-Aufrufen kann festgelegt werden. Diese Einstellungen werden durch einen Satz **erforderlicher Registrierungsschlüssel** und **optionale Registrierungsschlüssel** konfiguriert, wie unten beschrieben.

## <a name="required-registry-keys"></a>Erforderliche Registrierungsschlüssel

Zum Konfigurieren eines LBS-Servers sind mehrere Registrierungsschlüssel und-Werte erforderlich. Wenn Schlüssel fehlen oder bei einem Fehler eingegeben werden, wird ein Windows-Ereignis protokolliert. Informationen zu dem protokollierten Ereignis finden Sie in der Beschreibung der einzelnen Schlüssel und Werte.

Zum Konfigurieren der Serverfarm muss ein Registrierungsschlüssel erstellt werden. **HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy** heißt **lbsconfiguration**. Unter dem Schlüssel **lbsconfiguration** wird ein Schlüssel für jede Ressource in der Serverfarm erstellt. Der Schlüssel Name ist die Zeichen folgen Darstellung der GUID für die Ressource. Mindestens ein Ressourcen Schlüssel muss vorhanden sein, und diese Ressource ist identisch mit der [**UUID**](./rpcdce/ns-rpcdce-uuid.md) , die von Clients auf dem Bindungs handle, dem [**RPC- \_ Bindungs \_ handle**](rpc-binding-handle.md), festgelegt wird, wenn Sie die RPC/HTTP-Bindung erstellen (Weitere Informationen finden Sie unter [**rpcbindingsetobject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). Unter jedem Ressourcen-UUID-Schlüssel muss ein DWORD-Wert mit dem Namen **ConfigurationType** vorhanden sein, der die verwendete Konfiguration beschreibt. Es muss auch eine **reg \_ SZ** mit durch Semikolon getrennten Server Bezeichnernamen vorhanden sein, die als **Serverfarm** bezeichnet werden. Die Server, die im Server **Farm** Schlüssel identifiziert werden, sind die Server, die Mitglieder der Serverfarm für den Lastenausgleich sind.

Im folgenden finden Sie eine detaillierte Aufschlüsselung der erforderlichen Registrierungsschlüssel und-Werte:

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ lbsconfiguration**

Registrierungsschlüssel. Der **lbsconfiguration** -Schlüssel ist der Registrierungsschlüssel, der die lbs-Konfiguration enthält. Dies umfasst die Ressourcen- [**UUIDs**](./rpcdce/ns-rpcdce-uuid.md) , für die ein Lastenausgleich ausgeführt werden soll, der Konfigurationstyp für jede Ressource und die Server in den Serverfarmen, die am Lastenausgleich beteiligt sind. Wenn dieser Schlüssel fehlt oder ungültig ist, wird lbs nicht als konfiguriert betrachtet, und der lbs-Dienst wird nicht ausgeführt.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ lbsconfiguration \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx**

Registrierungsschlüssel. Der **Ressourcen-UUID** -Schlüssel identifiziert die Ressourcen-UUID für den Lastenausgleich. Diese Ressourcen-UUID ist identisch mit der [**UUID**](./rpcdce/ns-rpcdce-uuid.md) , die von Clients auf dem Bindungs handle, dem [**RPC- \_ Bindungs \_ handle**](rpc-binding-handle.md), festgelegt wurde. Mindestens eine Ressourcen-UUID muss vorhanden sein, um einen Lastenausgleich ausführen zu können. möglicherweise sind mehrere Ressourcen-UUIDs vorhanden. Es kann nur eine Serverfarm vorhanden sein, und alle Endpunkte müssen sich auf allen Servern innerhalb der Serverfarm befinden. Wenn dieser Schlüssel nicht zu einer gültigen UUID analysiert werden kann, wird der Ereignis- **RpcProxy-Ereignis \_ Protokoll-lb- \_ \_ \_ Schlüssel (0xc0000006)** im Windows-Ereignisprotokoll protokolliert.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ lbsconfiguration \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ ConfigurationType**

DWORD. Der **ConfigurationType** DWORD wird unter dem **Ressourcen-UUID** -Schlüssel gespeichert. Der einzige zulässige Wert ist 1. Wenn dieser Wert etwas anderes als 1 ist, wird das Ereignis **RpcProxy \_ EventLog \_ lb \_ Unknown \_ cfg \_ Type (0xc0000007)** im Windows-Ereignisprotokoll protokolliert.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ lbsconfiguration \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ Serverfarm**

REG \_ SZ. Der **Serverfarm** -Registrierungs Wert enthält eine durch Semikolons getrennte Liste von Server bezeichgern. Der Server Bezeichner weist das folgende Format auf:

"ServerID1, ServerPort1, LBSPort1, \[ LBSPort2,... Lbsportn \] ; "

Im Registrierungsschlüssel " **Serverfarm** " sollten mehrere Server Bezeichner aufgelistet werden. Sie müssen durch ein Semikolon begrenzt werden. Die Felder, die Teil des Server Bezeichners sind, werden in der folgenden Tabelle beschrieben. Wenn dieses Feld nicht ordnungsgemäß analysiert werden kann, wird das Ereignis **RpcProxy \_ EventLog lb fehlerhafter \_ \_ \_ Konfigurations \_ Eintrag (0xc0000008)** im Windows-Ereignisprotokoll protokolliert.



| Bezeichnerfeld | Anforderung | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Erforderlich    | Ein auflösbarer Netzwerkname für den Server. Dabei kann es sich um einen DNS-Namen, einen NetBIOS--Namen oder eine IP-Adresse handeln.                                                                                                                                                                                |
| ServerPort       | Optional    | Wenn angegeben, der Port, auf dem der Server auf RPC/HTTP-Verbindungen lauscht. Wenn kein Wert angegeben ist, wird die Endpunkt Zuordnung auf dem Server Computer verwendet, um den Serverport zu ermitteln.                                                                                                         |
| Lbsport          | Optional    | Wenn angegeben, der Port, auf dem der Server auf lbs lauscht. Um diesen Schlüssel verwenden zu können, müssen die lbs-Schnittstellen mithilfe des Befehls netsh RPC Firewall auf einen statischen Endpunkt festgelegt werden. Beispiele für den Netsh-Befehl finden Sie unter [bewährte Methoden für den Lastenausgleich](load-balancing-best-practices.md) . |



 

## <a name="optional-registry-keys"></a>Optionale Registrierungsschlüssel

Es gibt drei optionale Registrierungs Werte, um einen lbs-Server zu konfigurieren. Die Schlüssel Steuern hauptsächlich die Sicherheitsstufe für Aufrufe von und vom lbs-Dienst und Steuern außerdem die zu verwendende standardmäßige Ressourcen-UUID. Im folgenden sind optionale Werte aufgeführt:

Im folgenden finden Sie eine detaillierte Aufschlüsselung der erforderlichen Registrierungsschlüssel und-Werte:

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ lbsconfiguration \\ NoSecurity**

DWORD. Wenn **NoSecurity** DWORD nicht vorhanden ist oder auf 0 festgelegt ist, werden eingehende nicht sichere Aufrufe des lbs-Diensts abgelehnt. Wenn vorhanden und nicht 0, werden eingehende nicht sichere Aufrufe an den lbs-Dienst nicht zurückgewiesen. Dieser Schlüssel wird beim Start des lbs-Dienstanbieter einmal eingelesen.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ lbsconfiguration \\ assumeresourceuuid**

DWORD. Wenn das " **assumeresourceuuid** DWORD" nicht vorhanden ist, erfolgt keine Änderung im lbs-Dienst. Wenn Sie vorhanden ist, muss Sie mit einer gültigen [**UUID**](./rpcdce/ns-rpcdce-uuid.md)festgelegt werden. Diese **UUID** wird als Ressourcen-UUID für alle Verbindungen verwendet, die keine Ressourcen-UUID angeben. Dies wird häufig in Fällen verwendet, in denen Clients bei der Erstellung der RPC/HTTP-Bindung keine Ressourcen-UUID angeben, aber ein Administrator möchte einen Lastenausgleich für den RPC/HTTP-Datenverkehr zu einer Serverfarm durchführen. Wenn dieser Schlüssel nicht in eine UUID analysiert werden kann, wird ein interner RPC-Fehler ausgegeben, der die [**erweiterten RPC- \_ \_ Fehler \_ Informationen**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) erzeugt, wenn er aktiviert ist.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ rpchttplbsserver \\ NoSecurity**

DWORD. Wenn **NoSecurity** DWORD nicht angezeigt oder auf 0 festgelegt wird, haben alle ausgehenden Aufrufe an die lbs-Dienste Sicherheit. Wenn Sie vorhanden und nicht auf 0 festgelegt ist, haben alle ausgehenden Aufrufe an die lbs-Dienste keine Sicherheit. Stellen Sie sicher, dass diese Einstellung mit der Einstellung " **HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ lbsconfiguration \\ NoSecurity** " übereinstimmt.

 

 