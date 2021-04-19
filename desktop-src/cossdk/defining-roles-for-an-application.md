---
description: Sie bestimmen eine Sicherheitsrichtlinie für eine Anwendung, indem Sie die erforderlichen Sicherheits Privilegien definieren.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definieren von Rollen für eine Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342585"
---
# <a name="defining-roles-for-an-application"></a>Definieren von Rollen für eine Anwendung

Sie bestimmen eine Sicherheitsrichtlinie für eine Anwendung, indem Sie die erforderlichen Sicherheits Privilegien definieren. Zu diesem Zweck deklarieren Sie eine symbolische Berechtigungsebene als Rolle – definieren Sie die Rolle für die Anwendung – und [weisen Sie die Rolle](assigning-roles-to-components--interfaces--or-methods.md) dann bestimmten Ressourcen innerhalb der Anwendung zu. Dieser Entwurf wird erfüllt, wenn die Anwendung bereitgestellt wird und Systemadministratoren die Rolle mit den tatsächlichen Benutzern und Benutzergruppen auffüllen. Ausführlichere Informationen finden Sie unter [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md).

**So fügen Sie einer Anwendung eine Rolle hinzu**

1.  Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, der Sie die Rolle hinzufügen möchten. Erweitern Sie die Struktur, um die Ordner für die Anwendung anzuzeigen.

2.  Klicken Sie mit der rechten Maustaste auf den Ordner **Rollen** für die Anwendung, zeigen Sie auf **neu**, und klicken Sie dann auf **Rolle**.

3.  Geben Sie im Dialogfeld **Rolle** den Namen der neuen Rolle in das bereitgestellte Feld ein.

4.  Klicken Sie auf **OK**.

> [!Note]  
> Nachdem Sie der Anwendung Rollen hinzugefügt haben, müssen Sie sicherstellen, dass Sie die Rollen den entsprechenden Komponenten, Schnittstellen und Methoden zuweisen. Andernfalls treten bei allen Aufrufen der Anwendung Fehler auf, wenn rollenbasierte Sicherheit ausgewählt und aktiviert wurde und Rollen hinzugefügt, aber nicht zugewiesen wurden. Weitere Informationen finden Sie unter [Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen auf Komponentenebene](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



