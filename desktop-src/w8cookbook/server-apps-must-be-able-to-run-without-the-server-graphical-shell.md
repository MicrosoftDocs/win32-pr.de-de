---
title: Einschränkungen der grafischen Shell für Server
description: Server-Apps müssen ohne die grafische Shell des Servers ausgeführt werden können.
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2a3002fc2395faba3e07d90a2322c770fe3ee9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443221"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Server-Apps müssen ohne die grafische Shell des Servers ausgeführt werden können.

## <a name="platform"></a>Plattform

**Server** – Windows Server 2012 

## <a name="description"></a>BESCHREIBUNG

Die grafische Servershell, das Feature, das Windows-Explorer und Internet Explorer enthält, wird standardmäßig auf "Server mit grafischer Benutzeroberfläche" von Windows Server 2012 installiert. Die Funktion der grafischen Shell für Server kann deinstalliert werden, um den potenziellen Wartungs- und Leistungsbedarf zu reduzieren. Dadurch wird die Anzahl von Neustarts eingeschränkt, die auf dem Server auftreten können, während verwaltungstools weiterhin lokal auf dem Server ausgeführt werden können.

Nachdem ein Administrator die grafische Shell für den Server deinstalliert hat, befindet sich der Server in der Konfiguration minimaler Serverschnittstellen:

![Konfiguration der grafischen Shellschnittstelle des Servers](images/minimalserverinterface.png)

Administratoren können dann die Minimale Serverschnittstellenkonfiguration (die einen Satz lokaler Verwaltungstools enthält) als Standard ausführen, anstatt auf dem Server mit einer GUI-Konfiguration. Dies ermöglicht eine lokale Überwachung und Verwaltung, während gleichzeitig die Ressourcennutzung und die Wartungshäufigkeit reduziert werden.

Administratoren können die grafische Servershell später erneut installieren, wenn sie die darin enthaltene Funktionalität benötigen. (Administratoren können auch mit einer Server Core-Installation beginnen und mithilfe der Features bei Bedarf die Konfiguration der minimalen Serverschnittstelle "erstellen".)

Server-Apps müssen in der Lage sein, in der minimalen Serverschnittstellenkonfiguration ausgeführt zu werden, um die geringere Ressourcenauslastung und den geringeren Wartungsbedarf nutzen zu können. Diese Funktion kann erreicht werden, indem es dem Administrator gestattet wird, Teile der App, die die grafische Servershell benötigen, nicht zu installieren, oder indem er das Vorhandensein der grafischen Servershell erkennt und einige Aspekte der App deaktiviert.

Die minimale Serverschnittstelle weist einen reduzierten Ressourcen- und Wartungsbedarf auf, da viele APIs und Binärdateien, die in der grafischen Servershell enthalten sind, in dieser Konfiguration nicht verfügbar sind. Gegebenenfalls sollten Server-Apps auch die Remoteverwaltung (vorzugsweise über Windows PowerShell Remoting) über eine andere Windows Server- oder Windows-Clientinstallation zulassen. Dies ermöglicht eine bessere zentralisierte Verwaltung von mindestens einem Computer in der Minimalen Serverschnittstellenkonfiguration oder von Computern in einer noch geringeren Speicherbedarfskonfiguration wie Server Core.

## <a name="manifestation"></a>Manifestation

Wenn eine App APIs oder Binärdateien erfordert, die in der Konfiguration der minimalen Serverschnittstelle nicht verfügbar sind, wird sie möglicherweise nicht ordnungsgemäß auf dem Bildschirm angezeigt und/oder nicht verwendet werden.

## <a name="mitigation"></a>Minderung

Server-App-Entwickler sollten die Teile ihrer Apps identifizieren, die entfernte APIs oder Binärdateien erfordern, und Informationen für den Serveradministrator enthalten, die die Teile der App identifizieren, die bei Verwendung der minimalen Serverschnittstelle nicht ordnungsgemäß ausgeführt werden. Wenn diese Teile der App optional installiert werden können oder für die Produktfunktionalität nicht unbedingt erforderlich sind, kann die App weiterhin installiert und unter der Minimalkonfiguration der Serverschnittstelle ausgeführt werden.

Wenn die App ohne die grafische Shell des Servers überhaupt nicht verwendet werden kann, sollte diese Einschränkung dokumentiert werden, und der Serveradministrator sollte angewiesen werden, die grafische Shell des Servers zu installieren. (Wenn Sie zu einer Server Core-Installation hinzufügen, kann dies das Hinzufügen von Features mithilfe von Features bei Bedarf erfordern.) Darüber hinaus sollte die App beim Start überprüfen, ob alle erforderlichen Dateien verfügbar sind, da die grafische Servershell jederzeit vor oder nach der Installation der App deinstalliert werden kann.

## <a name="solution"></a>Lösung

Verlassen Sie sich auf den kleinstmöglichen Satz von Abhängigkeiten, und modularisieren Sie Apps, sodass die Kernfunktionen der App funktionieren können, ohne dass komplexere Komponenten der Benutzeroberfläche installiert werden müssen. Entwickeln Sie Apps, die keine der entfernten APIs oder Binärdateien benötigen, und nutzen Sie stattdessen die Funktionen, die in minimaler Serverschnittstelle oder Server Core enthalten sind. Dies reduziert die Wartungsanforderungen und verbessert gleichzeitig die Leistung und benutzerzufriedenheit.

Wenn es Teile einer App gibt, die wichtige Funktionen hinzufügen können, wenn die grafische Shell des Servers verfügbar ist, haben App-Entwickler folgende Möglichkeiten:

-   Lassen Sie zu, dass diese zusätzlichen Features, die die grafische Servershell verwenden, optional installiert werden, damit sie bei Installationen in einer Minimalkonfiguration der Serverschnittstelle weggelassen werden können.
-   Erkennen des Vorhandenseins der grafischen Shell des Servers und Anpassen des App-Verhaltens

App-Entwickler sollten auch sicherstellen, dass Server-Apps nach Möglichkeit remote verwaltet werden können.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Erkennen von minimaler Serverschnittstelle und Server Core

Windows Server installiert einen entsprechenden Registrierungswert für jede installierte Serverebene. Sie können abfragen, ob diese Schlüssel vorhanden sind, um zu ermitteln, ob die Funktionen der grafischen Shell oder der minimalen Serverschnittstelle installiert und aktiviert sind.

HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels:



|   &nbsp;         | Server Core | Minimale Serverbenutzeroberfläche | Grafische Shell des Servers |
|------------------|-------------|--------------------------|------------------------|
| ServerCore=1     | X           | X                        | X                      |
| Server-GuiMgmt=1 |             | X                        | X                      |
| ServerGuiShell=1 |             |                          | X                      |



 

Ein "X" in der obigen Tabelle bedeutet, dass der Registrierungsschlüssel vorhanden ist, wenn das entsprechende Feature installiert wird.

Beachten Sie, dass diese Serverebenen additiv sind. , wenn die grafische Servershell installiert ist, ebenso wie die minimale Serverschnittstelle und Server Core. In diesem Fall sind beide Registrierungsschlüssel vorhanden.

## <a name="tests"></a>Tests

Überprüfen Sie Ihren App-Code auf Anforderungen, die eine der entfernten APIs und Binärdateien verwenden. Nachdem Sie alle Instanzen dieser Instanzen aus "Kernanwendungsbinärdateien" entfernt haben, testen Sie Ihre App in einer Umgebung, die nicht die grafische Servershell enthält. Tools wie der Prozessmonitor können dabei hilfreich sein.

Wenn Sie die Verwendung dieser APIs und Binärdateien nicht vollständig beenden können, stellen Sie sicher, dass Ihre App ordnungsgemäß fehlschlägt, wenn sie auf minimaler Serverschnittstelle oder Server Core ausgeführt wird.

## <a name="resources"></a>Ressourcen

-   [Vorhandene Server Core-Dokumentation auf MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 