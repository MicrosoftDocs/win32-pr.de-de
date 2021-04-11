---
description: Wenn die COM+-Anwendung rollenbasierte Sicherheit verwendet, müssen mehrere Aufgaben abgeschlossen werden.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Konfigurieren von Role-Based Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342139"
---
# <a name="configuring-role-based-security"></a>Konfigurieren von Role-Based Sicherheit

Wenn die COM+-Anwendung rollenbasierte Sicherheit verwendet, müssen mehrere Aufgaben abgeschlossen werden. Beim Entwerfen der Komponenten in Ihrer Anwendung definieren Sie die Rollen, die zum Schutz des Zugriffs auf diese Komponenten erforderlich sind. Außerdem entscheiden Sie, welche Rollen den Komponenten, Schnittstellen und Methoden der Anwendung zugewiesen werden sollen. Während der Anwendungsintegration verwenden Sie das Verwaltungs Programmkomponenten Dienste, um der Anwendung die definierten Rollen hinzuzufügen, und weisen die einzelnen Rollen den entsprechenden Komponenten, Schnittstellen und Methoden zu.

Beim Konfigurieren der rollenbasierten Sicherheit führen Sie die folgenden Schritte aus:

1.  Aktivieren Sie Zugriffs Überprüfungen auf Anwendungsebene. , Um die Sicherheitsüberprüfung für eine Anwendung zu aktivieren. Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md) .
2.  Legen Sie die Sicherheitsstufe für Zugriffs Überprüfungen fest. So legen Sie die Sicherheit entweder auf Prozess-, Prozess-und Komponentenebene fest Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md) .
3.  Aktivieren Sie Zugriffs Überprüfungen auf Komponentenebene. Aktivieren der Sicherheitsüberprüfung auf der Komponenten-, Schnittstellen-und Methoden Ebene. Ausführliche Informationen zum Ausführen dieses Schritts finden Sie [unter Aktivieren von Zugriffs Überprüfungen auf der Komponentenebene](enabling-access-checks-at-the-component-level.md) .
4.  Definieren von Rollen für eine Anwendung. Zum Erstellen von Rollen für eine Anwendung. Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md) .
5.  Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden. Zum Zuweisen von Rollen zu bestimmten Ressourcen in einer Anwendung. Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Software Einschränkungs Richtlinie](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Festlegen einer Identitätswechsel Ebene](setting-an-impersonation-level.md)
</dt> </dl>

 

 



