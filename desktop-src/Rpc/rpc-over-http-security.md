---
title: RPC über HTTP-Sicherheit
description: RPC über HTTP bietet neben der standardmäßigen RPC-Sicherheit drei Arten von Sicherheit, was dazu führt, dass RPC über HTTP-Datenverkehr einmal durch RPC und dann doppelt durch den tunneling-Mechanismus geschützt wird, der von RPC über HTTP bereitgestellt wird.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f1ebd5a7198a2b2ccae7703b92011bbd45b037db2f7ef8eb116e28ef06d8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926134"
---
# <a name="rpc-over-http-security"></a>RPC über HTTP-Sicherheit

RPC über HTTP bietet neben der standardmäßigen RPC-Sicherheit drei Arten von Sicherheit, was dazu führt, dass RPC über HTTP-Datenverkehr einmal durch RPC und dann doppelt durch den tunneling-Mechanismus geschützt wird, der von RPC über HTTP bereitgestellt wird. Eine Beschreibung der standardmäßigen RPC-Sicherheitsmechanismen finden Sie unter [Sicherheit.](security.md) Der RPC über HTTP-Tunnelingmechanismus erhöht die normale RPC-Sicherheit wie folgt:

-   Bietet Sicherheit über IIS (nur für RPC über HTTP v2 verfügbar).
-   Stellt SSL-Verschlüsselung und RPC-Proxyüberprüfung (gegenseitige Authentifizierung) bereit. Auch nur in RPC über HTTP v2 verfügbar.
-   Stellt Einschränkungen auf RPC-Proxyebene bereit, die diktieren, welche Computer im Servernetzwerk RPC über HTTP-Aufrufe empfangen dürfen.

Jede dieser drei Sicherheitsfeatures wird in den folgenden Abschnitten ausführlicher beschrieben.

## <a name="iis-authentication"></a>IIS-Authentifizierung

RPC über HTTP kann den normalen Authentifizierungsmechanismus von IIS nutzen. Das virtuelle Verzeichnis für den RPC-Proxy kann mithilfe des Rpc-Knotens unter der Standardwebsite im IIS-MMC-Snap-In konfiguriert werden:

![Screenshot: Rpc-Knoten unter der Standardwebsite im IIS-MMC-Snap-In](images/rpc-http-1.png)

IIS kann so konfiguriert werden, dass der anonyme Zugriff deaktiviert wird und eine Authentifizierung beim virtuellen Verzeichnis für den RPC-Proxy erforderlich ist. Klicken Sie hierzu mit der rechten Maustaste auf den Rpc-Knoten, und wählen Sie **Eigenschaften** aus. Wählen Sie die Registerkarte **Verzeichnissicherheit** aus, und klicken Sie in der Gruppe **Authentifizierung und Access Control** auf die Schaltfläche **Bearbeiten,** wie hier dargestellt:

![Screenshot des Dialogfelds "RPC-Eigenschaften"](images/rpc-http-2.png)

Obwohl Sie RPC über HTTP verwenden können, auch wenn das virtuelle Verzeichnis des RPC-Proxys anonymen Zugriff zulässt, empfiehlt Microsoft aus Sicherheitsgründen dringend, den anonymen Zugriff auf dieses virtuelle Verzeichnis zu deaktivieren. Aktivieren Sie für RPC über HTTP die Standardauthentifizierung, Windows integrierte Authentifizierung oder beides. Denken Sie daran, dass sich nur RPC über HTTP v2 bei RPC-Proxy authentifizieren kann, der eine einfache oder Windows integrierte Authentifizierung erfordert. RPC über HTTP v1 kann keine Verbindung herstellen, wenn **der anonyme Zugriff nicht** möglich ist. Da RPC über HTTP v2 die sicherere und stabilere Implementierung ist, verbessert die Verwendung einer Version von Windows, die dies unterstützt, die Sicherheit Ihrer Installationen.

> [!Note]  
> Standardmäßig ist das virtuelle RPC-Proxyverzeichnis markiert, um anonymen Zugriff zu ermöglichen. Der RPC-Proxy für RPC über HTTP v2 lehnt jedoch Anforderungen ab, die nicht standardmäßig authentifiziert sind.

 

## <a name="traffic-encryption"></a>Datenverkehrsverschlüsselung

RPC über HTTP kann Datenverkehr zwischen dem RPC über HTTP-Client und dem RPC-Proxy mit SSL verschlüsseln. Der Datenverkehr zwischen dem RPC-Proxy und dem RPC über HTTP-Server wird mit normalen RPC-Sicherheitsmechanismen verschlüsselt und verwendet kein SSL (auch wenn SSL zwischen dem Client und dem RPC-Proxy ausgewählt wird). Dies liegt daran, dass dieser Teil des Datenverkehrs innerhalb des Netzwerks einer Organisation und hinter einer Firewall übertragen wird.

Datenverkehr zwischen dem RPC über HTTP-Client und dem RPC-Proxy, der in der Regel über das Internet übertragen wird, kann mit SSL verschlüsselt werden, zusätzlich zu dem Verschlüsselungsmechanismus, der für RPC ausgewählt wurde. In diesem Fall wird der Datenverkehr im Internetbereich der Route doppelt verschlüsselt. Die Verschlüsselung des Datenverkehrs über den RPC-Proxy bietet eine sekundäre Verteidigung, falls der RPC-Proxy oder andere Computer im Umkreisnetzwerk kompromittiert sind. Da der RPC-Proxy die sekundäre Verschlüsselungsebene nicht entschlüsseln kann, hat der RPC-Proxy keinen Zugriff auf die gesendeten Daten. Weitere Informationen finden Sie [unter RPC over HTTP Deployment Empfehlungen (RPC über HTTP-Bereitstellung](rpc-over-http-deployment-recommendations.md) Empfehlungen). SSL-Verschlüsselung ist nur mit RPC über HTTP v2 verfügbar.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Einschränken von RPC über HTTP-Aufrufe auf bestimmte Computer

Die IIS-Sicherheitskonfiguration basiert auf zulässigen Computer- und Portbereichen. Die Möglichkeit, RPC über HTTP zu verwenden, wird durch zwei Registrierungseinträge auf dem Computer gesteuert, auf dem IIS und der RPC-Proxy ausgeführt werden. Der erste Eintrag ist ein Flag, das die RPC-Proxyfunktionalität umschaltet. Die zweite ist eine optionale Liste von Computern, an die der Proxy RPC-Aufrufe weiterleiten kann.

Standardmäßig kann ein Client, der den RPC-Proxy kontaktiert, um RPC über HTTP-Aufrufe zu tunneln, nicht auf RPC-Serverprozesse zugreifen, mit Ausnahme der RPC über HTTP-Serverprozesse, die auf demselben Computer wie der RPC-Proxy ausgeführt werden. Wenn das ENABLED-Flag nicht definiert oder auf einen Nullwert festgelegt ist, deaktiviert IIS den RPC-Proxy. Wenn das ENABLED-Flag definiert und auf einen Wert ungleich 0 (null) festgelegt ist, kann ein Client eine Verbindung mit RPC über HTTP-Server auf dem Computer herstellen, auf dem IIS ausgeführt wird. Um dem Client das Tunneln zu einem RPC über HTTP-Serverprozess auf einem anderen Computer zu ermöglichen, müssen Sie der Liste der RPC über HTTP-Server des IIS-Computers einen Registrierungseintrag hinzufügen.

RPC-Server können RPC über HTTP-Aufrufe nicht akzeptieren, es sei denn, sie forderten RPC ausdrücklich auf, RPC über HTTP zu lauschen.

Im folgenden Beispiel wird veranschaulicht, wie die Registrierung so konfiguriert wird, dass Clients eine Verbindung mit Servern über das Internet herstellen können:

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

Der **ValidPorts-Eintrag** ist ein REG \_ SZ-Eintrag, der eine Liste der Computer enthält, an die der IIS-RPC-Proxy RPC-Aufrufe weiterleiten darf, sowie die Ports, die er zum Herstellen einer Verbindung mit den RPC-Servern verwenden sollte. Der REG \_ SZ-Eintrag hat das folgende Format: Rosco:593; Rosco:2000-8000;Data \* :4000-8000.

In diesem Beispiel kann IIS RPC über HTTP-Aufrufe an den Server "Rosco" an den Ports 593 und 2000 bis 8000 weiterleiten. Sie kann auch Aufrufe an jeden Server senden, dessen Name mit "Data" beginnt. Die Verbindung wird über die Ports 4000 bis 8000 hergestellt. Darüber hinaus führt der RPC-Proxy vor dem Weiterleiten von Datenverkehr an einen bestimmten Port auf dem RPC über HTTP-Server einen speziellen Paketaustausch mit dem RPC-Dienst durch, der an diesem Port lauscht, um sicherzustellen, dass er bereit ist, Anforderungen über HTTP zu akzeptieren.

Wenn ein RPC-Dienst an Port 4500 auf Server "Data1" lauscht, aber keine der [ * *\* RpcServerUseProtseq_-Funktionen*](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) mit _*ncacn http** aufgerufen \_ hat, wird die Anforderung abgelehnt. Dieses Verhalten bietet zusätzlichen Schutz für Server, die aufgrund eines Konfigurationsfehlers an einem geöffneten Port lauschen. Sofern der Server nicht ausdrücklich angefordert hat, RPC über HTTP zu lauschen, empfängt er keine Aufrufe, die von außerhalb der Firewall stammen.

Einträge im **ValidPorts-Schlüssel** müssen eine genaue Übereinstimmung mit dem RPC über HTTP-Server sein, der vom Client angefordert wird (die Groß-/Kleinschreibung muss nicht beachtet werden). Um die Verarbeitung zu optimieren, führt der RPC-Proxy keine Kanonisierung des vom RPC über HTTP-Client bereitgestellten Namens durch. Wenn der Client daher nach rosco.microsoft.com fragt und in **ValidPorts** nur Rosco enthält, stimmt der RPC-Proxy nicht mit den Namen überein, obwohl beide Namen möglicherweise auf denselben Computer verweisen. Wenn die IP-Adresse von Rosco 66.77.88.99 lautet und der Client 66.77.88.99 anfragt, der **ValidPorts-Schlüssel** jedoch nur Rosco enthält, verweigert der RPC-Proxy die Verbindung. Wenn ein Client den RPC über HTTP-Server nach Namen oder IP-Adresse anfordern kann, fügen Sie beide in den **ValidPorts-Schlüssel** ein.

> [!Note]  
> Obwohl RPC IPv6 aktiviert ist, unterstützt der RPC-Proxy keine IPv6-Adressen im **ValidPorts-Schlüssel.** Wenn IPv6 verwendet wird, um den RPC-Proxy und den RPC über HTTP-Server zu verbinden, können nur DNS-Namen verwendet werden.

 

IIS liest die Registrierungseinträge **Enabled** und **ValidPorts** beim Start. Darüber hinaus wird der Inhalt des **ValidPorts-Schlüssels** von RPC über HTTP ungefähr alle 5 Minuten erneut gelesen. Wenn der **ValidPorts-Eintrag** geändert wird, werden die Änderungen innerhalb von 5 Minuten implementiert.

**RPC über HTTP v1:** Der WEBDIENST muss mithilfe des Internet-Service Manager beendet und neu gestartet werden, damit neue Werte in den Registrierungseinträgen implementiert werden.

 

 




