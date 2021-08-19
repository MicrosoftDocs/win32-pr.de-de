---
description: Die Sicherheit wird nur an Anwendungsgrenzen überprüft.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Sicherheitsgrenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050be064c8a2fe3dc8eb81e2297e1699504f92ae7b8b4352d9b875dfc50e91a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047268"
---
# <a name="security-boundaries"></a>Sicherheitsgrenzen

Die Sicherheit wird nur an Anwendungsgrenzen überprüft. Das heißt, dass für zwei Komponenten in derselben Anwendung keine Sicherheitsüberprüfung durchgeführt wird, wenn eine Komponente die andere aufruft. Wenn jedoch zwei Anwendungen denselben Prozess gemeinsam nutzen und eine Komponente in einer eine Komponente in der anderen eine Komponente aufruft, wird eine Sicherheitsüberprüfung durchgeführt, da eine Anwendungsgrenze überschritten wird. Wenn sich zwei Anwendungen in unterschiedlichen Serverprozessen befinden und eine Komponente in der ersten Anwendung eine Komponente in der zweiten Anwendung aufruft, wird ebenfalls eine Sicherheitsüberprüfung durchgeführt.

Wenn Sie also über zwei Komponenten verfügen und Sicherheitsüberprüfungen durchführen möchten, wenn eine die andere aufruft, müssen Sie die Komponenten in separaten COM+-Anwendungen unterteilen.

Da COM+-Bibliotheksanwendungen von anderen Prozessen gehostet werden, besteht eine Sicherheitsgrenze zwischen der Bibliotheksanwendung und dem Hostingprozess. Darüber hinaus wird die Sicherheit auf Prozessebene von der Bibliotheksanwendung nicht kontrolliert. Dies wirkt sich darauf aus, wie Sie die Sicherheit dafür konfigurieren müssen. Weitere Informationen finden Sie unter [Sicherheit von Bibliotheksanwendung.](library-application-security.md)

Die Ermittlung, ob bei einem Aufruf einer Komponente eine Sicherheitsüberprüfung durchgeführt werden muss, basiert auf der Sicherheitseigenschaft des Objektkontexts, der beim Instanziieren der konfigurierten Komponente erstellt wird. Weitere Informationen finden Sie unter [Security Context Property](security-context-property.md).

## <a name="component-level-access-checks"></a>Component-Level Zugriffsüberprüfungen

Für eine COM+-Serveranwendung haben Sie die Möglichkeit, Zugriffsüberprüfungen entweder auf Komponenten- oder Prozessebene zu erzwingen.

Wenn Sie zugriffsüberprüfung auf Komponentenebene auswählen, aktivieren Sie fein abgrenzende Rollenzuweisungen. Sie können Komponenten, Schnittstellen und Methoden Rollen zuweisen und eine artikulierte Autorisierungsrichtlinie erreichen. Dies ist die Standardkonfiguration für Anwendungen mit rollenbasierter Sicherheit.

Für COM+-Bibliotheksanwendungen müssen Sie Sicherheit auf Komponentenebene auswählen, wenn Sie Rollen verwenden möchten. Bibliotheksanwendungen können keine Sicherheit auf Prozessebene verwenden.

Sie sollten die Zugriffsüberprüfung auf Komponentenebene auswählen, wenn Sie die programmgesteuerte rollenbasierte Sicherheit verwenden. Kontextinformationen zu Sicherheitsaufrufen sind nur verfügbar, wenn sicherheit auf Komponentenebene aktiviert ist. Weitere Informationen finden Sie unter [Security Call Context Information](security-call-context-information.md).

Wenn Sie außerdem zugriffsüberprüfung auf Komponentenebene auswählen, wird die Sicherheitseigenschaft in den Objektkontext eingeschlossen. Dies bedeutet, dass die Sicherheitskonfiguration eine Rolle bei der Aktivierung des Objekts spielen kann. Weitere Informationen finden Sie unter [Security Context Property](security-context-property.md).

## <a name="process-level-access-checks"></a>Process-Level Zugriffsüberprüfungen

Überprüfungen auf Prozessebene gelten nur für die Anwendungsgrenze. Das heißt, die Rollen, die Sie für die gesamte COM+-Anwendung definiert haben, bestimmen, wer Zugriff auf eine Ressource innerhalb der Anwendung erhält. Es gelten keine feiner abgrenzenden Rollenzuweisungen. Im Wesentlichen werden die Rollen verwendet, um einen Sicherheitsdeskriptor zu erstellen, anhand dessen jeder Aufruf der Komponenten der Anwendung überprüft wird. In diesem Fall sollten Sie keine detaillierte Autorisierungsrichtlinie mit mehreren Rollen erstellen. Die Anwendung verwendet einen einzelnen Sicherheitsdeskriptor.

Für COM+-Bibliotheksanwendungen würden Sie keine Zugriffsüberprüfungen auf Prozessebene auswählen. Die Bibliotheksanwendung wird im Prozess des Clients gehostet und kontrolliert daher nicht die Sicherheit auf Prozessebene. Weitere Informationen finden Sie unter [Sicherheit von Bibliotheksanwendung.](library-application-security.md)

Wenn Zugriffsüberprüfungen auf Prozessebene aktiviert sind, sind keine Kontextinformationen zu Sicherheitsaufrufen verfügbar. Dies bedeutet, dass Sie keine programmgesteuerte Sicherheit erreichen können, wenn Sie nur Sicherheit auf Prozessebene verwenden. Weitere Informationen finden Sie unter [Security Call Context Information](security-call-context-information.md).

Darüber hinaus wird die Sicherheitseigenschaft nicht in den Objektkontext eingeschlossen. Dies bedeutet, dass die Sicherheitskonfiguration bei ausschließlicher Verwendung von Zugriffsüberprüfungen auf Prozessebene keine Rolle bei der Aktivierung des Objekts spielt. Weitere Informationen finden Sie unter [Security Context Property](security-context-property.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektives Entwerfen von Rollen](designing-roles-effectively.md)
</dt> <dt>

[Kontextinformationen zu Sicherheitsaufrufen](security-call-context-information.md)
</dt> <dt>

[Sicherheitskontexteigenschaft](security-context-property.md)
</dt> <dt>

[Verwenden von Rollen für die Clientautorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



