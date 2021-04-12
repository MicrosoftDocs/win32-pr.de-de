---
title: RPC-über-HTTP-Sicherheit
description: RPC-über-HTTP bietet neben der Standard-RPC-Sicherheit drei Arten von Sicherheit, was dazu führt, dass RPC-über-HTTP-Datenverkehr einmal durch RPC geschützt wird und dann doppelt durch den von RPC über HTTP bereitgestellten tunnelingmechanismus geschützt wird.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527cf5ff74120c41606d83a248e355a6ea46d9d5
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104218949"
---
# <a name="rpc-over-http-security"></a>RPC-über-HTTP-Sicherheit

RPC-über-HTTP bietet neben der Standard-RPC-Sicherheit drei Arten von Sicherheit, was dazu führt, dass RPC-über-HTTP-Datenverkehr einmal durch RPC geschützt wird und dann doppelt durch den von RPC über HTTP bereitgestellten tunnelingmechanismus geschützt wird. Eine Beschreibung der standardmäßigen RPC-Sicherheitsmechanismen finden Sie unter [Sicherheit](security.md). Der RPC-über-HTTP-tunnelingmechanismus erhöht die normale RPC-Sicherheit auf folgende Weise:

-   Bietet Sicherheit über IIS (nur für RPC über HTTP v2 verfügbar).
-   Bietet SSL-Verschlüsselung und RPC-Proxy Überprüfung (gegenseitige Authentifizierung). Auch nur in RPC über HTTP v2 verfügbar.
-   Bietet Einschränkungen auf der Ebene des RPC-Proxys, die feststellen, welche Computer im Servernetzwerk RPC-über-http-Aufrufe empfangen dürfen.

Jede dieser drei Sicherheitsfeatures wird in den folgenden Abschnitten ausführlicher beschrieben.

## <a name="iis-authentication"></a>IIS-Authentifizierung

RPC-über-HTTP kann den normalen Authentifizierungsmechanismus von IIS nutzen. Das virtuelle Verzeichnis für den RPC-Proxy kann mithilfe des RPC-Knotens unter der Standard Website im IIS-MMC-Snap-in konfiguriert werden:

![Screenshot, der den RPC-Knoten unter der Standard Website im IIS-MMC-Snap-in anzeigt](images/rpc-http-1.png)

IIS kann so konfiguriert werden, dass der anonyme Zugriff deaktiviert wird und eine Authentifizierung für das virtuelle Verzeichnis des RPC-Proxys erforderlich ist. Klicken Sie hierzu mit der rechten Maustaste auf den RPC-Knoten, und wählen Sie **Eigenschaften** aus. Wählen Sie die Registerkarte **Verzeichnis Sicherheit** aus, und klicken Sie in der Gruppe **Authentifizierung und Access Control** auf die Schaltfläche **Bearbeiten** , wie im folgenden dargestellt:

![Screenshot, der das Dialogfeld "RPC-Eigenschaften" anzeigt](images/rpc-http-2.png)

Obwohl Sie RPC über HTTP verwenden können, auch wenn das virtuelle Verzeichnis des RPC-Proxys anonymen Zugriff zulässt, empfiehlt Microsoft dringend, den anonymen Zugriff auf dieses virtuelle Verzeichnis aus Sicherheitsgründen zu deaktivieren. Aktivieren Sie stattdessen für RPC über HTTP die Standard Authentifizierung, die integrierte Windows-Authentifizierung oder beides. Beachten Sie, dass sich nur RPC über HTTP v2 beim RPC-Proxy authentifizieren kann, der die Standard Authentifizierung oder die integrierte Windows-Authentifizierung erfordert. RPC-über-HTTP v1 kann keine Verbindung herstellen, wenn die Option **anonymen Zugriff nicht zulassen** deaktiviert ist. Da RPC über HTTP v2 die sicherere und stabilere Implementierung ist, wird die Sicherheit ihrer Installationen durch die Verwendung einer Windows-Version, die diese unterstützt, verbessert.

> [!Note]  
> Standardmäßig ist das virtuelle Verzeichnis des RPC-Proxys so gekennzeichnet, dass es anonymen Zugriff zulässt. Der RPC-Proxy für RPC über HTTP v2 lehnt jedoch Anforderungen ab, die nicht standardmäßig authentifiziert werden.

 

## <a name="traffic-encryption"></a>Verschlüsselung des Datenverkehrs

RPC-über-HTTP kann den Datenverkehr zwischen dem RPC-über-HTTP-Client und dem RPC-Proxy mit SSL verschlüsseln. Der Datenverkehr zwischen dem RPC-Proxy und dem RPC-über-HTTP-Server wird mit den normalen RPC-Sicherheitsmechanismen verschlüsselt und verwendet nicht SSL (auch wenn SSL zwischen dem Client und dem RPC-Proxy ausgewählt ist). Dies liegt daran, dass dieser Teil des Datenverkehrs innerhalb des Netzwerks einer Organisation und hinter einer Firewall unterwegs ist.

Der Datenverkehr zwischen dem RPC-über-HTTP-Client und dem RPC-Proxy, der in der Regel über das Internet übertragen wird, kann mit SSL verschlüsselt werden, zusätzlich zu dem für RPC ausgewählten Verschlüsselungsmechanismus. In diesem Fall wird der Datenverkehr im Internet Teil der Route doppelt verschlüsselt. Das Verschlüsseln des Datenverkehrs über den RPC-Proxy bietet eine sekundäre Verteidigung, für den Fall, dass der RPC-Proxy oder andere Computer im Umkreis Netzwerk kompromittiert sind. Da der RPC-Proxy die sekundäre Verschlüsselungs Schicht nicht entschlüsseln kann, hat der RPC-Proxy keinen Zugriff auf die gesendeten Daten. Weitere Informationen finden Sie unter [RPC-über-HTTP-Bereitstellungs Empfehlungen](rpc-over-http-deployment-recommendations.md) . SSL-Verschlüsselung ist nur mit RPC über HTTP v2 verfügbar.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Einschränken von RPC-über-HTTP-aufrufen auf bestimmte Computer

Die IIS-Sicherheitskonfiguration basiert auf zulässigen Computern und Port Bereichen. Die Funktion zur Verwendung von RPC über HTTP wird durch zwei Registrierungseinträge auf dem Computer gesteuert, auf dem IIS ausgeführt wird, und den RPC-Proxy. Der erste Eintrag ist ein Flag, das die RPC-Proxy Funktionalität schaltet. Bei der zweiten handelt es sich um eine optionale Liste von Computern, an die der Proxy RPC-Aufrufe weiterleiten kann.

Standardmäßig kann ein Client, der den RPC-Proxy zum Tunneln von RPC-über-HTTP-aufrufen kontaktiert, nicht auf RPC-Server Prozesse außer den RPC-über-HTTP-Server Prozessen zugreifen, die auf dem gleichen Computer wie der RPC-Proxy Wenn das aktivierte Flag nicht definiert oder auf einen Wert von 0 (null) festgelegt ist, wird der RPC-Proxy von IIS deaktiviert. Wenn das aktivierte Flag definiert und auf einen Wert ungleich 0 (null) festgelegt ist, kann ein Client eine Verbindung mit RPC über HTTP-Servern auf dem Computer mit IIS herstellen. Damit der Client auf einem anderen Computer zu einem RPC-über-HTTP-Server-Prozess Tunneln kann, müssen Sie der Liste der RPC-über-HTTP-Server des IIS-Computers einen Registrierungs Eintrag hinzufügen.

RPC-Server können keine RPC-über-http-Aufrufe akzeptieren, es sei denn, Sie haben speziell RPC zum lauschen an RPC über http

Im folgenden Beispiel wird veranschaulicht, wie Sie die Registrierung so konfigurieren, dass Clients über das Internet eine Verbindung mit Servern herstellen können:

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

Der Eintrag **ValidPorts** ist ein reg \_ SZ-Eintrag, der eine Liste der Computer enthält, an die der IIS-RPC-Proxy RPC-Aufrufe weiterleiten darf, sowie die Ports, die zum Herstellen einer Verbindung mit den RPC-Servern verwendet werden sollen. Der \_ Eintrag REG SZ hat die folgende Form: Rosco: 593; Rosco: 2000-8000; Daten \* : 4000-8000.

In diesem Beispiel kann IIS RPC-über-http-Aufrufe an den Server "Rosco" an den Ports 593 und 2000 bis 8000 weiterleiten. Es kann auch Aufrufe an jeden Server senden, dessen Name mit "Data" beginnt. Er stellt eine Verbindung über die Ports 4000 bis 8000 her. Außerdem führt der RPC-Proxy vor der Weiterleitung von Datenverkehr an einen bestimmten Port auf dem RPC-über-HTTP-Server einen speziellen Paket Austausch mit dem RPC-Dienst aus, der diesen Port überwacht, um sicherzustellen, dass er für die Annahme von Anforderungen über HTTP bereit ist

Wenn ein RPC-Dienst auf dem Server "data1" auf dem Server "" 4500 auf dem Server "" lauscht, aber keine der [ * *rpcserveruseprotabq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) -Funktionen mit _ * ncacn \_ http * * aufgerufen hat, wird die Anforderung abgelehnt. Dieses Verhalten bietet zusätzlichen Schutz für Server, die einen geöffneten Port aufgrund von Konfigurationsfehlern überwachen. Wenn der Server nicht speziell für die Überwachung von RPC über HTTP aufgefordert wird, empfängt er keine Aufrufe, die von außerhalb der Firewall ausgehen.

Einträge im **ValidPorts** -Schlüssel müssen exakt mit dem RPC-über-HTTP-Server, der vom Client angefordert wird, identisch sein (die Groß-/Kleinschreibung wird nicht beachtet). Zur Optimierung der Verarbeitung führt der RPC-Proxy keine Kanonisierung des Namens durch, der vom RPC-über-HTTP-Client bereitgestellt wird. Wenn der Client also Rosco.Microsoft.com anfordert, und in **ValidPorts** nur Rosco enthalten, stimmt der RPC-Proxy nicht mit den Namen überein, obwohl beide Namen auf denselben Computer verweisen können. Wenn die IP-Adresse von Rosco 66.77.88.99 lautet und der Client nach 66.77.88.99 fragt, **der Schlüssel jedoch** nur Rosco enthält, lehnt der RPC-Proxy die Verbindung ab. Wenn ein Client den RPC-über-HTTP-Server anhand des Namens oder anhand der IP-Adresse anfordern kann, fügen Sie beide in den **ValidPorts** -Schlüssel ein.

> [!Note]  
> Obwohl RPC auf IPv6 aktiviert ist, unterstützt der RPC-Proxy keine IPv6-Adressen im **ValidPorts** -Schlüssel. Wenn IPv6 verwendet wird, um den RPC-Proxy und den RPC-über-HTTP-Server zu verbinden, können nur DNS-Namen verwendet werden.

 

IIS liest beim Start die Registrierungseinträge " **aktiviert** " und " **ValidPorts** ". Darüber hinaus wird der Inhalt des **ValidPorts** -Schlüssels ungefähr alle 5 Minuten durch RPC über HTTP erneut angezeigt. Wenn der Eintrag **ValidPorts** geändert wird, werden die Änderungen innerhalb von 5 Minuten implementiert.

**RPC über HTTP v1:** Der Webdienst muss beendet und mithilfe des Internet Service Manager neu gestartet werden, damit neue Werte in den Registrierungs Einträgen implementiert werden.

 

 




