---
title: Konfigurieren von Computern für RPC über http
description: Um HTTP als Transportprotokoll für RPC zu verwenden, muss der RPC-Proxy, der innerhalb von Internet Information Server (IIS) ausgeführt wird, im Netzwerk des Server Programms konfiguriert werden.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d1b39276633f3b827f778deef77edd5630c599
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340217"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Konfigurieren von Computern für RPC über http

Um HTTP als Transportprotokoll für RPC zu verwenden, muss der RPC-Proxy, der innerhalb von Internet Information Server (IIS) ausgeführt wird, im Netzwerk des Server Programms konfiguriert werden. In diesem Abschnitt werden die Konfigurationsoptionen beschrieben. Empfehlungen zu bewährten Programmier-und Konfigurationsverfahren bei der Verwendung von RPC über HTTP finden Sie unter [RPC-über-HTTP-Bereitstellungs Empfehlungen](rpc-over-http-deployment-recommendations.md). Der primäre Task ist die Konfiguration des RPC-Proxys zum akzeptieren und Weiterleiten von RPC-über-HTTP-Verbindungen an ein RPC über HTTP-Serverprogramm

IIS muss zunächst auf dem Computer installiert werden, auf dem der RPC-Proxy ausgeführt wird. Nach der Installation von IIS wird der RPC-Proxy installiert. Sowohl IIS als auch der RPC-Proxy können gleichzeitig von **Windows-Komponenten hinzufügen/entfernen** in der Systemsteuerung installiert werden. Der RPC-Proxy wird von den **Netzwerkdiensten** installiert und in Windows Setup als **RPC-über-HTTP-Proxy** bezeichnet. Wenn sowohl IIS als auch der RPC-Proxy gleichzeitig installiert werden, stellt Windows sicher, dass Sie in der richtigen Reihenfolge installiert werden.

> [!Note]  
> Nachdem die Installation beendet wurde, muss IIS neu gestartet werden, wenn Sie während des Installationsvorgangs ausgeführt wird.

 

Nach der Installation des RPC-Proxys müssen einige zusätzliche Konfigurationsaufgaben ausgeführt werden:

1.  Öffnen Sie das IIS-MMC-Snap-in, und konfigurieren Sie das virtuelle Verzeichnis des RPC-Proxys so, [dass Sicherheit erforderlich](rpc-over-http-security.md)ist Dieser Schritt ist nur erforderlich, wenn Sie RPC über HTTP v2 verwenden möchten.
2.  Wenn auf IIS kein Zertifikat installiert ist, muss ein gültiges Zertifikat für diesen Computer abgerufen und installiert werden, damit SSL bei der Kommunikation mit dem RPC-Proxy verwendet werden kann. Dieser Schritt ist nur für RPC über HTTP v2 relevant. Da RPC über HTTP v1 SSL nicht unterstützt, kann dieser Schritt für RPC über HTTP v1 ausgelassen werden.
3.  Legen Sie den **ValidPorts** -Schlüssel fest, wie in [RPC over HTTP Security](rpc-over-http-security.md)beschrieben.

Wenn diese Konfigurationsaufgaben abgeschlossen sind, kann der RPC-über-HTTP-Proxy Anforderungen vom RPC-über-HTTP-Client an den RPC-über-HTTP-Server weiterleiten.

## <a name="rpc-over-http-registry-keys"></a>RPC-über-HTTP-Registrierungsschlüssel

In diesem Abschnitt werden zusätzliche Registrierungsschlüssel erläutert, die zum Konfigurieren des Clients, Servers oder RPC-Proxys in einer RPC-über-HTTP-Verbindung verwendet Diese Schlüssel sind in der Regel nicht erforderlich. Diese werden aus Gründen der Vollständigkeit bereitgestellt.

**HKLM \\ Software \\ Microsoft \\ RPC \\ defaultchannelellifetime**

DWORD. Überschreibt die standardmäßige Kanal Lebensdauer. Wird auf dem Client und dem RPC-Proxy verwendet. Die Kanal Lebensdauer wird in Bytes ausgedrückt. Wenn kein Wert angegeben wird, wird 1 GB verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn der RPC-Proxy geändert wird, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ clientreceivewindow**

DWORD. Gibt ggf. das Empfangs Fenster an, das vom Client für Daten verwendet wird, die vom RPC-Proxy empfangen werden. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ inproxyreceivewindow**

DWORD. Gibt ggf. das Empfangs Fenster an, das vom RPC-Proxy für Daten verwendet wird, die vom Client empfangen werden. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn an diesem Wertänderungen vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ outproxyreceivewindow**

DWORD. Gibt ggf. das Empfangs Fenster an, das vom RPC-Proxy für Daten verwendet wird, die vom Server empfangen werden. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn an diesem Wertänderungen vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ serverreceivewindow**

DWORD. Gibt ggf. das Empfangs Fenster an, das vom Server für Daten verwendet wird, die vom RPC-Proxy empfangen werden. Der minimale gültige Wert ist 8K. Der Höchstwert beträgt 1 GB. Wenn der Wert nicht vorhanden ist, wird 64K verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn an diesem Wertänderungen vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Policies \\ Microsoft \\ Windows NT \\ RPC \\ minimumconnectiontimeout**

DWORD. Gibt ggf. das minimale Verbindungs Timeout an, das vom Client und RPC-Proxy verwendet wird (in Sekunden). Der tatsächliche Timeout Wert ist der niedrigere dieses Werts und des IIS-Leerlauf Verbindungs Timeouts. Wenn 0 (null) oder der Schlüssel nicht vorhanden ist, wird das IIS-Leerlauf Verbindungs Timeout verwendet. Wird nur in RPC über HTTP v2 verwendet. Wenn an diesem Wert auf dem RPC-Proxy Änderungen vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ useproxyforipaddrifrdnsschlägt fehl**

Wenn vorhanden und auf ungleich 0 (null) festgelegt ist und eine numerische IP-Adresse als RPC-Proxy Adresse bereitgestellt wird, versucht ein RPC-über-HTTP-Client, die Namensauflösung umzukehren. wenn dies fehlschlägt, versucht, eine Verbindung mit dem RPC-Proxy über einen HTTP-Proxy herzustellen. Kann verwendet werden, um das Verhalten von Windows NT bei Installationen zu emulieren, die ein solches Verhalten erfordern. Wird für RPC über HTTP v2 ignoriert. Wird nur verwendet, wenn RPC über HTTP v1 verwendet wird. Wird nur unter Windows 2000 mit Service Pack 3 (SP3) und höher unterstützt.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ Zuordnung**

DWORD. Wenn Sie nicht vorhanden oder auf 0 (null) festgelegt ist, überprüft der RPC-Proxy, ob die Verbindung authentifiziert ist und ob Sie sicher ist (SSL oder eine andere Form der Verschlüsselung wird verwendet). Wenn eine der beiden Optionen false ist, wird die Verbindung zurückgewiesen. Wenn dieser Wert ungleich 0 (null) enthält, sind anonyme und nicht verschlüsselte Verbindungen zulässig. Diese Einstellung ist eine Ergänzung zu den Einstellungen des virtuellen Verzeichnisses. Wenn z. b. anonymer Zugriff auf der Ebene des virtuellen Verzeichnisses deaktiviert ist, die **Zuordnung** aber nicht NULL ist, wird der anonyme Zugriff auf IIS-Ebene weiterhin blockiert. Wird nur auf dem RPC-Proxy in RPC über HTTP v2 verwendet. Wenn an diesem Wert auf dem RPC-Proxy Änderungen vorgenommen werden, muss IIS neu gestartet werden, damit die Änderung wirksam wird.

> [!WARNING]
> Microsoft empfiehlt dringend, den **zugewiesenen** Wert auf Produktionssystemen auf Sicherheitsaspekte festzulegen. Der einzige Grund, warum dieser Schlüssel festgelegt werden sollte, ist das Testen von geschlossenen Netzwerken ohne externen Zugriff. Alle mit dem Internet verbundenen Systeme und die Ausführung des RPC-Proxys mit dem **zugewiesenen** Schlüssel, der auf einen Wert ungleich 0 (null) festgelegt ist, können anfällig für Angriffe sein.

 

 

 




