---
description: Nachdem Sie die Zugriffs Überprüfungen aktiviert haben, müssen Sie für die COM+-Anwendung die Ebene auswählen, auf der Sie die Zugriffs Überprüfungen durchführen möchten.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127396"
---
# <a name="setting-a-security-level-for-access-checks"></a>Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen

Nachdem Sie die [Zugriffs Überprüfungen](enabling-access-checks-for-an-application.md)aktiviert haben, müssen Sie für die COM+-Anwendung die Ebene auswählen, auf der Sie die Zugriffs Überprüfungen durchführen möchten.

**So wählen Sie eine Sicherheitsstufe aus**

1.  Klicken Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die Zugriffs Überprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .

3.  Wählen Sie unter **Sicherheitsstufe** eine der folgenden Aktionen aus:

    -   **Nur Zugriffs Prüfungen auf Prozessebene ausführen**– diese Einstellung gibt an, dass Benutzer in Rollen, die der Anwendung zugewiesen sind, der Prozess Sicherheits Beschreibung hinzugefügt werden. Dies hat folgende Auswirkungen und Implikationen:

        Die differenzierte Rollen Überprüfung ist auf Komponenten-, Methoden-und Schnittstellen Ebene deaktiviert. Sicherheitsüberprüfungen werden nur auf Anwendungsebene durchgeführt.

        Die Security-Eigenschaft ist nicht im Kontext für Objekte enthalten, die in der Anwendung ausgeführt werden. Dies kann sich potenziell auf die Aktivierung von Objekten auswirken. Siehe [Sicherheitskontext Eigenschaft](security-context-property.md).

        Der Sicherheits Aufrufkontext wird nicht verfügbar gemacht. Programmgesteuerte Sicherheit, die auf Sicherheitskontext Informationen basiert, funktioniert nicht. Siehe [Kontextinformationen zum Sicherheitsgespräch](security-call-context-information.md).

    -   **Ausführen von Zugriffs Überprüfungen auf Prozess-und Komponentenebene**– diese Einstellung gibt an, dass Sicherheits Deskriptoren auf Prozessebene und vollständige rollenbasierte Sicherheitsüberprüfungen durchgeführt werden. Dies hat folgende Auswirkungen und Implikationen:

        Um die Rollen Überprüfung für bestimmte Komponenten zu aktivieren, müssen Sie [Zugriffs Überprüfungen auf Komponentenebene aktivieren](enabling-access-checks-at-the-component-level.md).

        Die Security-Eigenschaft ist im Kontext für alle Objekte enthalten, die in der Anwendung ausgeführt werden. Dies kann sich potenziell auf die Aktivierung von Objekten auswirken. Siehe [Sicherheitskontext Eigenschaft](security-context-property.md).

        Der Sicherheits Aufrufkontext ist verfügbar. Programmgesteuerte rollenbasierte Sicherheit ist aktiviert. Siehe [Kontextinformationen zum Sicherheitsgespräch](security-call-context-information.md).

        > [!Note]  
        > Für COM+-Bibliotheksanwendungen müssen Sie sowohl auf der Prozess-als auch auf der Komponentenebene prüfen, ob eine sinnvolle Zugriffs Überprüfung funktioniert. Bibliotheksanwendungen basieren auf dem Host Prozess für Sicherheit auf Prozessebene. Sie können bestimmen, wie die Bibliotheks Anwendung mit der vom Host Prozess durchgeführten Authentifizierung interagiert, indem Sie die- [Authentifizierung festlegen](enabling-authentication-for-a-library-application.md). Weitere Informationen finden Sie unter [Bibliotheks Anwendungssicherheit](library-application-security.md).

         

4.  Klicken Sie auf **OK**.

Wenn die Anwendung das nächste Mal gestartet wird, wird die Sicherheit automatisch auf der angegebenen Ebene geprüft. Nur Benutzer, die Rollen zugewiesen sind, die der Anwendung zugewiesen sind, erhalten Zugriff auf die Anwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen auf Komponentenebene](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



