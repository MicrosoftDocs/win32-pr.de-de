---
title: Einschränkungen der server grafischen Shell
description: Server-Apps müssen ohne die grafische Servershell ausgeführt werden können.
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1742b87d0cb4ece4ac05b38b0ac2644967eee256931df5dfc8ec838574db33ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773185"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Server-Apps müssen ohne die grafische Servershell ausgeführt werden können.

## <a name="platform"></a>Plattform

**Server** – Windows Server 2012 

## <a name="description"></a>Beschreibung

Die grafische Servershell, das Feature, das Windows Explorer und Internet Explorer enthält, wird standardmäßig auf Installationen von "Server mit grafischer Benutzeroberfläche" Windows Server 2012. Das Feature "Grafische Servershell" kann deinstalliert werden, um den potenziellen Wartungs- und Leistungsbedarf zu reduzieren. Dadurch wird die Anzahl von Neustarts des Servers eingeschränkt, während verwaltungstools weiterhin lokal auf dem Server ausgeführt werden können.

Nachdem ein Administrator die grafische Servershell deinstalliert hat, befindet sich der Server in der Konfiguration der minimalen Serverschnittstelle:

![Konfiguration der grafischen Shellschnittstelle des Servers](images/minimalserverinterface.png)

Administratoren können dann die Ausführung in der Konfiguration der minimalen Serverschnittstelle (die eine Reihe von lokalen Verwaltungstools umfasst) als Standard und nicht im Server mit einer GUI-Konfiguration ausführen. Dies ermöglicht die lokale Überwachung und Verwaltung und reduziert gleichzeitig den Ressourcenverbrauch und die Häufigkeit der Wartung.

Administratoren können die serverseitige grafische Shell später neu installieren, wenn sie die funktionalität in ihr benötigen. (Administratoren können auch von einer Server Core-Installation beginnen und die Konfiguration der minimalen Serverschnittstelle mithilfe der Features bei Bedarf-Funktionalität "erstellen".)

Server-Apps müssen in der minimalen Serverschnittstellenkonfiguration ausgeführt werden können, um die geringere Ressourcennutzung und den geringeren Wartungsbedarf nutzen zu können. Diese Funktion kann erreicht werden, indem dem Administrator ermöglicht wird, teile der App, die die server grafische Shell benötigt, nicht zu installieren, oder indem das Vorhandensein der grafischen Servershell erkannt und einige Aspekte der App deaktiviert werden.

Die minimale Serverschnittstelle verfügt über einen reduzierten Ressourcen- und Wartungsbedarf, da viele APIs und Binärdateien, die in der server grafischen Shell enthalten sind, in dieser Konfiguration nicht verfügbar sind. Gegebenenfalls sollten Server-Apps auch die Remoteverwaltung (vorzugsweise über Windows PowerShell Remoting) von einem anderen Windows Server oder Windows Client zulassen. Dies ermöglicht eine bessere zentralisierte Verwaltung von einem oder mehr Computern in der Konfiguration der minimalen Serverschnittstelle oder von Computern in einer noch geringeren Speicherbedarfskonfiguration wie Server Core.

## <a name="manifestation"></a>Manifestation

Wenn eine App APIs oder Binärdateien erfordert, die in der Konfiguration der minimalen Serverschnittstelle nicht verfügbar sind, wird sie möglicherweise nicht ordnungsgemäß auf dem Bildschirm angezeigt und/oder kann nicht verwendet werden.

## <a name="mitigation"></a>Minderung

Server-App-Entwickler sollten die Teile ihrer Apps identifizieren, die eine der entfernten APIs oder Binärdateien erfordern, und Informationen für den Serveradministrator enthalten, die die Teile der App identifizieren, die bei Verwendung der minimalen Serverschnittstelle nicht ordnungsgemäß ausgeführt werden. Wenn diese Teile der App optional installiert werden können oder für die Produktfunktionalität nicht unbedingt erforderlich sind, kann die App weiterhin unter der Minimal Server Interface-Konfiguration installiert und ausgeführt werden.

Wenn die App ohne die grafische Servershell überhaupt nicht verwendet werden kann, sollte diese Einschränkung dokumentiert werden, und der Serveradministrator sollte angewiesen werden, die server grafische Shell zu installieren. (Wenn Sie zu einer Server Core-Installation hinzufügen, müssen Sie möglicherweise Features mithilfe von Features bei Bedarf hinzufügen.) Darüber hinaus sollte die App beim Start überprüfen, ob alle erforderlichen Dateien verfügbar sind, da die grafische Servershell jederzeit vor oder nach der Installation der App deinstalliert werden kann.

## <a name="solution"></a>Lösung

Verlassen Sie sich auf den kleinsten möglichen Satz von Abhängigkeiten, und modularisieren Sie Apps, sodass die Kernfunktionen der App funktionieren können, ohne dass mehr benutzeroberflächenkomponenten installiert werden müssen. Entwickeln Sie Apps, die keine der entfernten APIs oder Binärdateien erfordern, und nutzen Sie stattdessen die Funktionalität, die in der minimalen Serverschnittstelle oder in Server Core enthalten ist. Dadurch werden die Wartungsanforderungen reduziert und gleichzeitig die Leistung und Benutzerzufriedenheit verbessert.

Wenn Es Teile einer App gibt, die möglicherweise erhebliche Funktionen hinzufügen, wenn die grafische Servershell verfügbar ist, haben App-Entwickler die folgenden Vorteile:

-   Lassen Sie zu, dass diese zusätzlichen Features, die die grafische Servershell verwenden, optional installiert werden, sodass sie bei Installationen in einer Minimal Server Interface-Konfiguration weggelassen werden können.
-   Erkennen des Vorhandenseins einer grafischen Servershell und Anpassen des App-Verhaltens

App-Entwickler sollten außerdem sicherstellen, dass Server-Apps nach Möglichkeit und nach Möglichkeit remote verwaltet werden können.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Erkennen der minimalen Serverschnittstelle und des Serverkerns

Windows Server installiert einen entsprechenden Registrierungswert für jede installierte Serverebene. Sie können das Vorhandensein dieser Schlüssel abfragen, um zu ermitteln, ob die Funktionen der grafischen Servershell oder der minimalen Serverschnittstelle installiert und aktiviert sind.

HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ \\ ServerLevels:



|   &nbsp;         | Server Core | Minimale Serverbenutzeroberfläche | Grafische Servershell |
|------------------|-------------|--------------------------|------------------------|
| ServerCore=1     | X           | X                        | X                      |
| Server-GuiMgmt=1 |             | X                        | X                      |
| ServerGuiShell=1 |             |                          | X                      |



 

Ein "X" in der obigen Tabelle bedeutet, dass der Registrierungsschlüssel vorhanden ist, wenn das entsprechende Feature installiert wird.

Beachten Sie, dass diese Serverebenen additiv sind. , wenn die grafische Servershell installiert ist, ist dies auch die minimale Serverschnittstelle und Server Core. In diesem Fall sind beide Registrierungsschlüssel vorhanden.

## <a name="tests"></a>Tests

Überprüfen Sie Ihren App-Code auf Anforderungen, die eine der entfernten APIs und Binärdateien verwenden. Nachdem Sie diese Instanzen aus den Binärdateien der "Kernanwendung" entfernt haben, testen Sie Ihre App in einer Umgebung, in der die grafische Servershell nicht enthalten ist. Tools wie der Prozessmonitor können dabei helfen.

Wenn Sie die Verwendung dieser APIs und Binärdateien nicht vollständig einstellen können, stellen Sie sicher, dass Ihre App ordnungsgemäß fehlschlägt, wenn sie auf minimaler Serverschnittstelle oder Server Core ausgeführt wird.

## <a name="resources"></a>Ressourcen

-   [Vorhandene Server Core-Dokumentation auf MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 