---
description: Wenn Ihre COM+-Anwendung rollenbasierte Sicherheit verwendet, müssen mehrere Aufgaben ausgeführt werden.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Konfigurieren von Role-Based Security
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba7df6b11bf44b53adaa9776435e43eabe3188fccb789a01d996f45331298dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859060"
---
# <a name="configuring-role-based-security"></a>Konfigurieren von Role-Based Security

Wenn Ihre COM+-Anwendung rollenbasierte Sicherheit verwendet, müssen mehrere Aufgaben ausgeführt werden. Beim Entwerfen der Komponenten in Ihrer Anwendung definieren Sie die Rollen, die zum Schutz des Zugriffs auf diese Komponenten erforderlich sind. Außerdem entscheiden Sie, welche Rollen den Komponenten, Schnittstellen und Methoden der Anwendung zugewiesen werden sollen. Während der Anwendungsintegration verwenden Sie das Verwaltungstool Komponentendienste, um der Anwendung die definierten Rollen hinzuzufügen und jede Rolle den entsprechenden Komponenten, Schnittstellen und Methoden zuzuweisen.

Führen Sie beim Konfigurieren der rollenbasierten Sicherheit die folgenden Schritte aus:

1.  Aktivieren Sie Zugriffsüberprüfungen auf Anwendungsebene. So aktivieren Sie die Sicherheitsüberprüfung für eine Anwendung. Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter Aktivieren von [Zugriffsüberprüfungen für eine Anwendung.](enabling-access-checks-for-an-application.md)
2.  Legen Sie die Sicherheitsstufe für Zugriffsüberprüfungen fest. So legen Sie die Sicherheit auf Prozess- oder Prozess- und Komponentenebene fest. Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen.](setting-a-security-level-for-access-checks.md)
3.  Aktivieren Sie Zugriffsüberprüfungen auf Komponentenebene. So aktivieren Sie die Sicherheitsüberprüfung auf Komponenten-, Schnittstellen- und Methodenebene. Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter Aktivieren von [Zugriffsüberprüfungen auf Komponentenebene.](enabling-access-checks-at-the-component-level.md)
4.  Definieren von Rollen für eine Anwendung. So erstellen Sie Rollen für eine Anwendung Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter Definieren von [Rollen für eine Anwendung.](defining-roles-for-an-application.md)
5.  Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden. So weisen Sie bestimmten Ressourcen innerhalb einer Anwendung Rollen zu Ausführliche Informationen zum Ausführen dieses Schritts finden Sie unter [Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden.](assigning-roles-to-components--interfaces--or-methods.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Softwareeinschränkungsrichtlinie](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Festlegen einer Identitätswechselebene](setting-an-impersonation-level.md)
</dt> </dl>

 

 



