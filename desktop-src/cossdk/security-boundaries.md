---
description: Die Sicherheit wird nur an Anwendungsgrenzen geprüft.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Sicherheitsgrenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcfca8868677ba14c8544657aa77acf04262805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344227"
---
# <a name="security-boundaries"></a>Sicherheitsgrenzen

Die Sicherheit wird nur an Anwendungsgrenzen geprüft. Das heißt, für zwei Komponenten in derselben Anwendung wird eine Sicherheitsüberprüfung durchgeführt, wenn eine Komponente die andere aufruft. Wenn jedoch zwei Anwendungen denselben Prozess nutzen und eine Komponente in einem anderen eine Komponente aufruft, wird eine Sicherheitsüberprüfung durchgeführt, weil eine Anwendungs Grenze überschritten wird. Wenn sich zwei Anwendungen in verschiedenen Server Prozessen befinden und eine Komponente in der ersten Anwendung eine Komponente in der zweiten Anwendung aufruft, wird eine Sicherheitsüberprüfung durchgeführt.

Wenn Sie also über zwei Komponenten verfügen und Sicherheitsüberprüfungen durchgeführt werden sollen, wenn ein anderer aufruft, müssen Sie die Komponenten in separaten com+-Anwendungen platzieren.

Da com+-Bibliotheksanwendungen von anderen Prozessen gehostet werden, gibt es eine Sicherheitsgrenze zwischen der Bibliotheks Anwendung und dem Hostingprozess. Außerdem steuert die Bibliotheks Anwendung nicht die Sicherheit auf Prozessebene, was sich darauf auswirkt, wie Sie die Sicherheit für die Anwendung konfigurieren müssen. Weitere Informationen finden Sie unter [Bibliotheks Anwendungssicherheit](library-application-security.md).

Die Bestimmung, ob eine Sicherheitsüberprüfung für einen-Vorgang in einer-Komponente ausgeführt werden muss, basiert auf der Sicherheits Eigenschaft des Objekt Kontexts, der erstellt wird, wenn die konfigurierte Komponente instanziiert wird. Weitere Informationen finden Sie unter [Sicherheitskontext Eigenschaft](security-context-property.md).

## <a name="component-level-access-checks"></a>Component-Level Zugriffs Überprüfungen

Bei einer COM+-Serveranwendung haben Sie die Wahl, Zugriffs Überprüfungen entweder auf der Komponentenebene oder auf der Prozessebene zu erzwingen.

Wenn Sie die Zugriffs Überprüfung auf Komponentenebene auswählen, aktivieren Sie differenzierte Rollenzuweisungen. Sie können Komponenten, Schnittstellen und Methoden Rollen zuweisen und eine Richtlinie für die Übersetzung von Richtlinien erreichen. Dabei handelt es sich um die Standardkonfiguration für Anwendungen, die rollenbasierte Sicherheit verwenden.

Für COM+-Bibliotheksanwendungen müssen Sie Sicherheit auf Komponentenebene auswählen, wenn Sie Rollen verwenden möchten. Bibliotheksanwendungen können keine Sicherheit auf Prozessebene verwenden.

Sie sollten die Zugriffs Überprüfung auf Komponentenebene auswählen, wenn Sie die programmgesteuerte rollenbasierte Sicherheit verwenden. Kontextinformationen für den Sicherheits Rückruf sind nur verfügbar, wenn die Sicherheit auf Komponentenebene aktiviert ist. Weitere Informationen finden Sie unter [Kontextinformationen zum Sicherheitsgespräch](security-call-context-information.md).

Wenn Sie außerdem die Zugriffs Überprüfung auf Komponentenebene auswählen, wird die Sicherheits Eigenschaft in den Objekt Kontext eingeschlossen. Dies bedeutet, dass die Sicherheitskonfiguration eine Rolle beim Aktivieren des Objekts spielen kann. Weitere Informationen finden Sie unter [Sicherheitskontext Eigenschaft](security-context-property.md).

## <a name="process-level-access-checks"></a>Process-Level Zugriffs Überprüfungen

Überprüfungen auf Prozessebene gelten nur für die Anwendungs Grenze. Das heißt, die Rollen, die Sie für die gesamte com+-Anwendung definiert haben, bestimmen, wem der Zugriff auf eine Ressource in der Anwendung gewährt wird. Es gelten keine präziseren Rollenzuweisungen. Im Wesentlichen werden die Rollen verwendet, um eine Sicherheits Beschreibung zu erstellen, für die alle Aufrufe der Anwendungskomponenten überprüft werden. In diesem Fall empfiehlt es sich nicht, eine ausführliche Autorisierungs Richtlinie mit mehreren Rollen zu erstellen. Die Anwendung verwendet einen einzelnen Sicherheits Deskriptor.

Für COM+-Bibliotheksanwendungen wählen Sie keine Zugriffs Überprüfungen auf Prozessebene aus. Die Bibliotheks Anwendung wird im Client Prozess gehostet und steuert daher nicht die Sicherheit auf Prozessebene. Weitere Informationen finden Sie unter [Bibliotheks Anwendungssicherheit](library-application-security.md).

Mit aktivierten Zugriffs Überprüfungen auf Prozessebene sind keine Kontextinformationen für den Sicherheits Rückruf verfügbar. Dies bedeutet, dass Sie keine programmgesteuerte Sicherheit ausführen können, wenn Sie nur die Sicherheit auf Prozessebene verwenden. Weitere Informationen finden Sie unter [Kontextinformationen zum Sicherheitsgespräch](security-call-context-information.md).

Außerdem wird die Sicherheits Eigenschaft nicht in den Objekt Kontext eingeschlossen. Dies bedeutet, dass bei der Verwendung von Zugriffs Überprüfungen auf Prozessebene die Sicherheitskonfiguration nie eine Rolle spielt, wie das Objekt aktiviert wird. Weitere Informationen finden Sie unter [Sicherheitskontext Eigenschaft](security-context-property.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Informationen zum Sicherheits Aufrufkontext](security-call-context-information.md)
</dt> <dt>

[Sicherheitskontext Eigenschaft](security-context-property.md)
</dt> <dt>

[Verwenden von Rollen für die Client Autorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



