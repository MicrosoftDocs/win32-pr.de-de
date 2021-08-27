---
description: Nachdem Sie Zugriffsüberprüfungen aktiviert haben, müssen Sie für Ihre COM+-Anwendung die Ebene auswählen, auf der Zugriffsüberprüfungen durchgeführt werden sollen.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e912f671a27d35b51939376fa14af3b693c368e3375680913693d364ddf638
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120370"
---
# <a name="setting-a-security-level-for-access-checks"></a>Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen

Nachdem Sie [Zugriffsüberprüfungen](enabling-access-checks-for-an-application.md)für Ihre COM+-Anwendung aktiviert haben, müssen Sie die Ebene auswählen, auf der Zugriffsüberprüfungen durchgeführt werden sollen.

**So wählen Sie eine Sicherheitsstufe aus**

1.  Klicken Sie in der Konsolenstruktur des Component Services-Verwaltungstools mit der rechten Maustaste auf die COM+-Anwendung, für die Sie Zugriffsüberprüfungen aktivieren möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit.**

3.  Wählen Sie **unter Sicherheitsstufe** eine der folgenden Möglichkeiten aus:

    -   **Ausführen von Zugriffsüberprüfungen nur auf Prozessebene:** Diese Einstellung gibt an, dass Benutzer in Rollen, die der Anwendung zugewiesen sind, dem Prozesssicherheitsdeskriptor hinzugefügt werden. Dies hat die folgenden Auswirkungen und Auswirkungen:

        Die differenzierte Rollenüberprüfung wird auf Komponenten-, Methoden- und Schnittstellenebene deaktiviert. Sicherheitsüberprüfungen werden nur auf Anwendungsebene ausgeführt.

        Die Sicherheitseigenschaft ist nicht im Kontext für Objekte enthalten, die in der Anwendung ausgeführt werden. Dies kann sich möglicherweise darauf auswirken, wie Objekte aktiviert werden. Siehe [Sicherheitskontexteigenschaft](security-context-property.md).

        Der Sicherheitsaufrufkontext wird nicht verfügbar gemacht. Programmgesteuerte Sicherheit, die auf Sicherheitsaufrufkontextinformationen basiert, funktioniert nicht. Weitere Informationen finden Sie unter Kontextinformationen für [Sicherheitsaufrufe.](security-call-context-information.md)

    -   **Durchführen von Zugriffsüberprüfungen auf Prozess- und Komponentenebene:** Diese Einstellung gibt an, dass Sicherheitsbeschreibungsprüfungen auf Prozessebene und vollständige rollenbasierte Sicherheitsüberprüfungen durchgeführt werden. Dies hat die folgenden Auswirkungen und Auswirkungen:

        Um die Rollenüberprüfung für bestimmte Komponenten zu aktivieren, müssen Sie [Zugriffsüberprüfungen auf Komponentenebene aktivieren.](enabling-access-checks-at-the-component-level.md)

        Die Sicherheitseigenschaft ist im Kontext für alle Objekte enthalten, die in der Anwendung ausgeführt werden. Dies kann sich möglicherweise darauf auswirken, wie Objekte aktiviert werden. Siehe [Sicherheitskontexteigenschaft](security-context-property.md).

        Der Sicherheitsaufrufkontext ist verfügbar. Programmgesteuerte rollenbasierte Sicherheit ist aktiviert. Weitere Informationen finden Sie unter Kontextinformationen für [Sicherheitsaufrufe.](security-call-context-information.md)

        > [!Note]  
        > Bei COM+-Bibliotheksanwendungen müssen Sie sowohl auf Prozess- als auch auf Komponentenebene prüfen, ob eine sinnvolle Zugriffsüberprüfung funktioniert. Bibliotheksanwendungen basieren auf dem Hostprozess, um die Sicherheit auf Prozessebene zu gewährleisten. Sie können bestimmen, wie die Bibliotheksanwendung mit der vom Hostprozess durchgeführten Authentifizierung interagiert, indem Sie die [Authentifizierung festlegen.](enabling-authentication-for-a-library-application.md) Weitere Informationen finden Sie unter [Bibliotheksanwendungssicherheit.](library-application-security.md)

         

4.  Klicken Sie auf **OK**.

Wenn die Anwendung das nächste Mal gestartet wird, wird die Sicherheit automatisch auf der angegebenen Ebene überprüft. Nur Benutzern, die Der Anwendung zugewiesenen Rollen zugewiesen sind, wird Zugriff auf die Anwendung gewährt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Konfigurieren von Role-Based Security](configuring-role-based-security.md)
</dt> <dt>

[Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffsüberprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffsüberprüfungen auf Komponentenebene](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



