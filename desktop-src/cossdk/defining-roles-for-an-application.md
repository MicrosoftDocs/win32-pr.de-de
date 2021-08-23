---
description: Sie bestimmen eine Sicherheitsrichtlinie für eine Anwendung, indem Sie die erforderlichen Sicherheitsberechtigungen definieren.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definieren von Rollen für eine Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc4b4fb6aaee557eea69dec405254925cd669d18ac73cdea229f548145d8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637710"
---
# <a name="defining-roles-for-an-application"></a>Definieren von Rollen für eine Anwendung

Sie bestimmen eine Sicherheitsrichtlinie für eine Anwendung, indem Sie die erforderlichen Sicherheitsberechtigungen definieren. To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application. Dieser Entwurf wird erfüllt, wenn die Anwendung bereitgestellt wird und Systemadministratoren die Rolle mit tatsächlichen Benutzern und Benutzergruppen auffüllen. Ausführlichere Informationen finden Sie unter [Rollenbasierte Sicherheitsverwaltung.](role-based-security-administration.md)

**So fügen Sie einer Anwendung eine Rolle hinzu**

1.  Suchen Sie in der Konsolenstruktur des Verwaltungstool Komponentendienste die COM+-Anwendung, der Sie die Rolle hinzufügen möchten. Erweitern Sie die Struktur, um die Ordner für die Anwendung anzeigen zu können.

2.  Klicken Sie mit der rechten **Maustaste auf** den Ordner Rollen für die Anwendung, zeigen Sie **auf Neu,** und klicken Sie dann auf **Rolle**.

3.  Geben Sie **im** Dialogfeld Rolle den Namen der neuen Rolle in das bereitgestellte Feld ein.

4.  Klicken Sie auf **OK**.

> [!Note]  
> Nachdem Sie der Anwendung Rollen hinzugefügt haben, müssen Sie sicherstellen, dass Sie die Rollen den entsprechenden Komponenten, Schnittstellen und Methoden zuweisen. Andernfalls können alle Aufrufe der Anwendung fehlschlagen, wenn die rollenbasierte Sicherheit ausgewählt und aktiviert wurde und Rollen hinzugefügt, aber nicht zugewiesen wurden. Weitere Informationen finden Sie unter [Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden.](assigning-roles-to-components--interfaces--or-methods.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Konfigurieren der Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Aktivieren von Zugriffsüberprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffsüberprüfungen auf Komponentenebene](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



