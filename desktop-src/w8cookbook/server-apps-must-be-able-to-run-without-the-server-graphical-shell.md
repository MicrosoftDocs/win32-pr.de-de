---
title: Einschränkungen für die Server-grafische Shell
description: Server-apps müssen ohne die servergrafikshell ausgeführt werden können
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7666ae07a28d798a36d249bf37ab2d7719b9fba0
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104391158"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Server-apps müssen ohne die servergrafikshell ausgeführt werden können

## <a name="platform"></a>Plattform

**Server** – Windows Server 2012 

## <a name="description"></a>BESCHREIBUNG

Die grafische Shell des Servers, das Feature, das Windows Explorer und Internet Explorer umfasst, wird standardmäßig auf der Seite "Server mit grafischer Benutzeroberfläche" von Windows Server 2012 installiert. Das Feature "grafische Shell für Server" kann deinstalliert werden, um den potenziellen Wartungs-und Leistungsbedarf zu reduzieren, wodurch die Anzahl der Neustarts beschränkt wird, die der Server verursachen kann, und gleichzeitig das lokale Ausführen von Verwaltungs Tools auf dem Server zulässt.

Nachdem ein Administrator die servergrafikshell deinstalliert hat, befindet sich der Server in der minimalen Server Schnittstellen Konfiguration:

![Konfiguration der Server grafischen Shell-Schnittstelle](images/minimalserverinterface.png)

Administratoren können dann in der Konfiguration mit minimaler Server Schnittstelle (die eine Reihe von lokalen Verwaltungs Tools umfasst) als Standardeinstellung und nicht auf dem Server mit einer GUI-Konfiguration ausgeführt werden. Dies ermöglicht die lokale Überwachung und Verwaltung, während gleichzeitig die Ressourcennutzung und die Wartungs Häufigkeit reduziert werden.

Administratoren können die servergrafikshell zu einem späteren Zeitpunkt neu installieren, wenn Sie die darin enthaltenen Funktionen benötigen. (Administratoren können auch von einer Server Core-Installation aus starten und die Konfiguration der minimalen Server Schnittstelle mithilfe der Features nach Bedarf-Funktionalität einrichten.)

Server-apps müssen in der Konfiguration mit minimaler Server Schnittstelle ausgeführt werden können, um von der geringeren Ressourcennutzung und Wartung profitieren zu können. Diese Funktion kann erreicht werden, indem Sie dem Administrator die Möglichkeit geben, keine Teile der APP zu installieren, die die grafische Shell des Servers benötigen, oder indem Sie das vorhanden sein der grafischen Shell des Servers erkennen und einige Aspekte der App deaktivieren.

Die minimale Server Schnittstelle verfügt über einen reduzierten Ressourcen-und Wartungsbedarf, da viele APIs und Binärdateien, die in der servergrafikshell enthalten sind, in dieser Konfiguration nicht verfügbar sind. Gegebenenfalls sollten Server-apps auch eine Remote Verwaltung (vorzugsweise über Windows PowerShell-Remoting) von einer anderen Windows Server-oder Windows-Client Installation zulassen. Dies ermöglicht eine bessere zentralisierte Verwaltung von einem oder mehreren Computern in der Konfiguration mit minimaler Server Schnittstelle oder von Computern mit einer noch geringeren Speicherbedarf, wie z. b. Server Core.

## <a name="manifestation"></a>Ausstrahlung

Wenn eine APP eine der APIs oder Binärdateien erfordert, die in der Konfiguration der minimalen Server Schnittstelle nicht verfügbar sind, wird Sie möglicherweise nicht ordnungsgemäß auf dem Bildschirm angezeigt und/oder ist unbrauchbar.

## <a name="mitigation"></a>Minderung

Server-App-Entwickler sollten diese Teile Ihrer Apps ermitteln, die eine der entfernten APIs oder Binärdateien erfordern, und Informationen für den Server Administrator einschließen, die die Teile der APP identifizieren, die bei Verwendung der minimalen Server Schnittstelle nicht ordnungsgemäß ausgeführt werden. Wenn diese Teile der APP optional installiert werden können oder für die Produktfunktionalität nicht unbedingt erforderlich sind, kann die APP weiterhin installiert und unter der Konfiguration der minimalen Server Schnittstelle ausgeführt werden.

Wenn die APP nicht ohne die servergrafikshell verwendet werden kann, sollte diese Einschränkung dokumentiert werden, und der Server Administrator sollte angewiesen werden, die servergrafikshell zu installieren. (Wenn Sie eine Server Core-Installation hinzufügen, erfordert dies möglicherweise das Hinzufügen von Features mithilfe von Features bei Bedarf.) Außerdem sollte die APP beim Start prüfen, ob alle erforderlichen Dateien verfügbar sind, da die servergrafikshell jederzeit vor oder nach der Installation der APP deinstalliert werden kann.

## <a name="solution"></a>Lösung

Verlassen Sie sich auf den kleinsten möglichen Satz von Abhängigkeiten, und modularisieren Sie apps, damit die Kern-App-Funktionalität funktionieren kann, ohne dass eine größere Anzahl von Benutzeroberflächen Komponenten installiert werden muss. Entwickeln Sie apps, für die keine der entfernten APIs oder Binärdateien erforderlich ist, und verlassen Sie sich stattdessen auf die Funktionen, die in der minimalen Server Schnittstelle oder im Server Core enthalten sind. Dies reduziert die Wartungsanforderungen und verbessert gleichzeitig die Leistung und die Benutzer Zufriedenheit.

Wenn es Teile einer APP gibt, die möglicherweise bedeutende Funktionen hinzufügen, wenn die servergrafikshell verfügbar ist, können App-Entwickler folgende Aktionen ausführen:

-   Diese zusätzlichen Funktionen, die die Verwendung der servergrafikshell verwenden, können optional installiert werden. Daher können Sie bei Installationen bei einer minimalen Server Schnittstellen Konfiguration ausgelassen werden.
-   Erkennen, ob die grafische Shell des Servers vorhanden ist, und passen das Verhalten der APP an

App-Entwickler sollten außerdem sicherstellen, dass Server-apps nach Möglichkeit und entsprechend Remote verwaltet werden können.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Erkennen der minimalen Server Schnittstelle und des Server Kerns

Windows Server installiert einen entsprechenden Registrierungs Wert für jede installierte Server Ebene. Sie können Abfragen, ob diese Schlüssel vorhanden sind, um zu bestimmen, ob die servergrafikshell oder die minimalen Server Schnittstellen Funktionen installiert und aktiviert sind.

HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server Server \\ Levels:



|                  | Server Core | Minimale Serverbenutzeroberfläche | Grafische Shell für Server |
|------------------|-------------|--------------------------|------------------------|
| Server Core = 1     | X           | X                        | X                      |
| Server-guimgmt = 1 |             | X                        | X                      |
| Serverguishell = 1 |             |                          | X                      |



 

Ein "X" in der obigen Tabelle bedeutet, dass der Registrierungsschlüssel vorhanden ist, wenn das entsprechende Feature installiert wird.

Beachten Sie, dass diese Server Ebenen Additiv sind. Wenn die servergrafikshell installiert ist, ist dies die minimale Server Schnittstelle und Server Core. In diesem Fall sind beide Registrierungsschlüssel vorhanden.

## <a name="tests"></a>Tests

Überprüfen Sie Ihren app-Code auf Anforderungen, bei denen eine der entfernten APIs und Binärdateien verwendet wird. Nachdem Sie alle Instanzen dieser Dateien aus den Binärdateien der Kernanwendung entfernt haben, testen Sie Ihre APP in einer Umgebung, in der die grafische Shell des Servers nicht enthalten ist. Hierfür können Tools wie der Prozess Monitor hilfreich sein.

Wenn Sie die Verwendung dieser APIs und Binärdateien nicht vollständig beenden können, sollten Sie sicherstellen, dass Ihre APP ordnungsgemäß fehlschlägt, wenn Sie auf minimaler Server Schnittstelle oder Server Core ausgeführt wird.

## <a name="resources"></a>Ressourcen

-   [Vorhandene Server Core-Dokumentation auf MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 