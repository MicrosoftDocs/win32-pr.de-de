---
title: Konfigurieren von Computern für RPC über HTTP
description: Damit HTTP als Transportprotokoll für RPC verwendet werden kann, muss der auf dem Internetinformationsserver (IIS) ausgeführte RPC-Proxy im Netzwerk des Serverprogramms konfiguriert werden.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4628339afe09e2b6e9a6f216504f411550d37b7a285614e507c89a4a8052c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022470"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Konfigurieren von Computern für RPC über HTTP

Damit HTTP als Transportprotokoll für RPC verwendet werden kann, muss der auf dem Internetinformationsserver (IIS) ausgeführte RPC-Proxy im Netzwerk des Serverprogramms konfiguriert werden. In diesem Abschnitt werden die Konfigurationsoptionen beschrieben. Empfehlungen zu bewährten Programmier- und Konfigurationsmethoden bei der Verwendung von RPC über HTTP finden Sie unter [RPC über HTTP-Bereitstellung Empfehlungen](rpc-over-http-deployment-recommendations.md). Die Hauptaufgabe besteht darin, den RPC-Proxy so zu konfigurieren, dass RPC über HTTP-Verbindungen an ein RPC über HTTP-Serverprogramm akzeptiert und weitergeleitet wird.

IIS muss zuerst auf dem Computer installiert werden, auf dem der RPC-Proxy ausgeführt wird. Sobald IIS installiert ist, wird der RPC-Proxy installiert. Sowohl IIS als auch der RPC-Proxy können gleichzeitig über **Add/Remove** Windows Components in der Systemsteuerung. Der RPC-Proxy wird von **den Netzwerkdiensten installiert** und im Setup als **RPC über HTTP-Proxy** Windows bezeichnet. Wenn sowohl IIS als auch DER RPC-Proxy gleichzeitig installiert sind, stellt Windows sicher, dass sie in der richtigen Reihenfolge installiert werden.

> [!Note]  
> Nach Abschluss der Installation muss IIS neu gestartet werden, wenn es während des Installationsvorgangs ausgeführt wurde.

 

Nach der Installation des RPC-Proxys müssen einige zusätzliche Konfigurationsaufgaben ausgeführt werden:

1.  Öffnen Sie das IIS-MMC-Snap-In, und konfigurieren Sie das virtuelle RPC-Proxyverzeichnis so, dass Sicherheit erforderlich ist, wie unter [RPC über HTTP-Sicherheit erläutert.](rpc-over-http-security.md) Dieser Schritt ist nur erforderlich, wenn Sie RPC über HTTP v2 verwenden möchten.
2.  Wenn IIS kein Zertifikat installiert hat, muss ein gültiges Zertifikat für diesen Computer erhalten und installiert werden, damit SSL bei der Kommunikation mit dem RPC-Proxy verwendet werden kann. Dieser Schritt ist nur für RPC über HTTP v2 relevant. Da RPC über HTTP v1 SSL nicht unterstützt, kann dieser Schritt für RPC über HTTP v1 weggelassen werden.
3.  Legen Sie den **ValidPorts-Schlüssel** wie unter [RPC über HTTP-Sicherheit beschrieben fest.](rpc-over-http-security.md)

Wenn diese Konfigurationsaufgaben abgeschlossen sind, kann der RPC-über-HTTP-Proxy Anforderungen vom RPC-über-HTTP-Client an den RPC-über-HTTP-Server weiter senden.

## <a name="rpc-over-http-registry-keys"></a>RPC über HTTP-Registrierungsschlüssel

In diesem Abschnitt werden zusätzliche Registrierungsschlüssel erläutert, die zum Konfigurieren des Clients, Servers oder RPC-Proxys in einer RPC-über-HTTP-Verbindung verwendet werden. Diese Schlüssel sind im Allgemeinen nicht erforderlich. sie werden hier der Vollständigkeit halber bereitgestellt.

**HKLM \\ Software \\ Microsoft \\ Rpc \\ DefaultChannelLifetime**

DWORD. Überschreibt die Standardmäßige Kanallebensdauer. Wird auf dem Client und dem RPC-Proxy verwendet. Die Kanallebensdauer wird in Bytes ausgedrückt. Wenn nicht angegeben, wird 1 GB verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn iiS auf dem RPC-Proxy geändert wird, muss iiS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ClientReceiveWindow**

DWORD. Wenn vorhanden, gibt das Empfangsfenster an, das vom Client für daten verwendet wird, die vom RPC-Proxy empfangen werden. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ InProxyReceiveWindow**

DWORD. Wenn vorhanden, gibt das Empfangsfenster an, das vom RPC-Proxy für vom Client empfangene Daten verwendet wird. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn Änderungen an diesem Wert vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ OutProxyReceiveWindow**

DWORD. Wenn vorhanden, gibt das Empfangsfenster an, das vom RPC-Proxy für vom Server empfangene Daten verwendet wird. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn Änderungen an diesem Wert vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ServerReceiveWindow**

DWORD. Wenn vorhanden, gibt das Empfangsfenster an, das vom Server für daten verwendet wird, die vom RPC-Proxy empfangen werden. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn Änderungen an diesem Wert vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**\\HKLM-Softwarerichtlinien \\ Microsoft Windows NT Rpc \\ \\ \\ \\ MinimumConnectionTimeout**

DWORD. Wenn vorhanden, gibt das minimale Verbindungs-Timeout in Sekunden an, das vom Client und RPC-Proxy verwendet wird. Das tatsächlich verwendete Timeout ist der niedrigere Wert dieses Werts und das IIS-Leerlaufverbindungs-Timeout. Wenn 0 (null) oder der Schlüssel nicht vorhanden ist, wird das IIS-Leerlaufverbindungs-Timeout verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn am RPC-Proxy Änderungen an diesem Wert vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ UseProxyForIPAddrIfRDNSFails**

Wenn vorhanden und auf nicht null festgelegt ist und eine numerische IP-Adresse als RPC-Proxyadresse bereitgestellt wird, versucht ein RPC-über-HTTP-Client eine umgekehrte Namensauflösung. Wenn dies fehlschlägt, wird versucht, über einen HTTP-Proxy eine Verbindung mit dem RPC-Proxy herzustellen. Kann verwendet werden, um das NT Windows bei Installationen zu emulieren, die ein solches Verhalten erfordern. Wird für RPC über HTTP v2 ignoriert. Wird nur verwendet, wenn RPC über HTTP v1 verwendet wird. Wird nur auf Windows 2000 mit Service Pack 3 (SP3) und höher unterstützt.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RpcProxy \\ AllowAnonymous**

DWORD. Wenn die Verbindung nicht vorhanden oder auf 0 (null) festgelegt ist, überprüft der RPC-Proxy, ob die Verbindung authentifiziert ist und ob sie sicher ist (SSL oder eine andere Art der Verschlüsselung wird verwendet). Wenn einer der Beiden false ist, wird die Verbindung abgelehnt. Wenn dieser Wert nicht 0 (null) enthält, sind anonyme und nicht verschlüsselte Verbindungen zulässig. Diese Einstellung ist eine Ergänzung zu allen Einstellungen für virtuelle Verzeichnisse. Wenn beispielsweise der anonyme Zugriff auf der Ebene des virtuellen Verzeichnisses deaktiviert ist, **AllowAnonymous** jedoch nicht 0 (null) ist, wird der anonyme Zugriff weiterhin auf IIS-Ebene blockiert. Wird nur auf dem RPC-Proxy in RPC über HTTP v2 verwendet. Wenn am RPC-Proxy Änderungen an diesem Wert vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

> [!WARNING]
> Microsoft empfiehlt aus Sicherheitsgründen dringend, den **Wert AllowAnonymous** auf Produktionssystemen zu setzen. Dieser Schlüssel sollte nur für Tests in geschlossenen Netzwerken ohne externen Zugriff festgelegt werden. Jedes System, das mit dem Internet verbunden ist und den RPC-Proxy mit dem **AllowAnonymous-Schlüssel** auf einen Wert ungleich 0 (null) ausgeführt, kann anfällig für Angriffe sein.

 

 

 




