---
description: Eine neue COM+-Anwendung wird erstellt.
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Eine neue COM+-Anwendung wird erstellt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344002"
---
# <a name="creating-a-new-com-application"></a>Eine neue COM+-Anwendung wird erstellt.

Zum Erstellen einer neuen COM+-Anwendung sind zwei grundlegende Schritte erforderlich:

-   Erstellen einer leeren COM+-Anwendung (siehe unten).
-   Hinzufügen von Komponenten zur Anwendung. (Weitere Informationen finden Sie unter [Installieren neuer Komponenten](installing-new-components.md) und [Importieren von Komponenten](importing-components.md).)

**So erstellen Sie eine leere com+-Anwendung**

1.  Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, auf dem Sie eine Anwendung erstellen möchten.

2.  Wählen Sie den Ordner **com+-Anwendungen** für diesen Computer aus.

3.  Zeigen Sie im Menü **Aktion** auf **neu**, und klicken Sie dann auf **Anwendung**. Sie können auch mit der rechten Maustaste auf den Ordner **com+-Anwendungen** , zeigen Sie auf **neu**, und klicken Sie dann auf **Anwendung**.

4.  Klicken Sie auf der **Willkommens** Seite des COM+-Anwendungsinstallations-Assistenten auf **weiter**, und klicken Sie dann im Dialogfeld **neue Anwendung installieren oder erstellen** auf **leere Anwendung erstellen**.

5.  Geben Sie in das bereitgestellte Feld einen Namen für die neue Anwendung ein. (Beachten Sie, dass die folgenden Sonderzeichen nicht in einem Anwendungsnamen verwendet werden können: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ', >, <,.,?,:, und;.) Klicken Sie unter **Aktivierungstyp** auf **Bibliotheks Anwendung** oder **Server Anwendung**. Klicken Sie auf **Weiter**.

    > [!Note]  
    > Eine Serveranwendung wird in einem eigenen Prozess ausgeführt. Server Anwendungen können alle com+-Dienste unterstützen. Eine Bibliotheks Anwendung wird im Prozess des Clients ausgeführt, von dem Sie erstellt wird. Bibliotheksanwendungen können rollenbasierte Sicherheit verwenden, aber keinen Remote Zugriff oder in die Warteschlange eingereihten Komponenten unterstützen.

     

6.  Wählen Sie im Dialogfeld **Anwendungs Identität festlegen** eine Identität aus, unter der die Anwendung ausgeführt wird. Wenn Sie **diesen Benutzer** auswählen, geben Sie den Benutzernamen und das Kennwort ein. Außerdem müssen Sie das Kennwort erneut in das Feld **Kennwort bestätigen** eingeben. Klicken Sie auf **Weiter**. (Die Standardauswahl für Anwendungs Identität ist **interaktiver Benutzer**. Der interaktive Benutzer ist der Benutzer, der zu einem beliebigen Zeitpunkt am Server Computer angemeldet ist. Sie können einen anderen Benutzer auswählen, indem Sie **diesen Benutzer** auswählen und einen bestimmten Benutzer oder eine bestimmte Gruppe eingeben.)

    > [!Note]  
    > Das Dialogfeld **Anwendungs Identität festlegen** wird nur angezeigt, wenn Sie im vorherigen Dialogfeld COM-Anwendungsinstallations-Assistent die Option **Server Anwendung** für den Aktivierungstyp der neuen Anwendung ausgewählt haben. Die Identity-Eigenschaft wird nicht für Bibliotheksanwendungen verwendet.

     

7.  Fügen Sie im Dialogfeld **Anwendungs Rollen hinzufügen** alle Rollen hinzu, die Sie der Anwendung zuordnen möchten. Standardmäßig ist nur die Rolle " **kreatorowner** " definiert. Weitere Informationen zu Rollen finden Sie unter [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md).

8.  Füllen Sie im Dialogfeld **Benutzer zu Rollen hinzufügen** jede Rolle, die Sie im letzten Schritt erstellt haben, mit den Benutzern, Gruppen oder integrierten Sicherheits Prinzipale auf, denen Sie die Berechtigungen erteilen möchten, die dieser Rolle zugeordnet sind. Standardmäßig wird der interaktive Benutzer in der Rolle "Administrator **Besitzer** " platziert.

9.  Klicken Sie auf **Fertig stellen**.

Die neue Anwendung wird jetzt unter dem Ordner **com+-Anwendungen** in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste angezeigt.

> [!Note]  
> Ab Windows Server 2003 sind Zugriffs Überprüfungen beim Erstellen einer COM+-Anwendung standardmäßig aktiviert. In früheren Versionen wurden Zugriffs Überprüfungen standardmäßig auf Anwendungsebene deaktiviert. Das Ergebnis ist, dass der Zugriff auf eine COM+-Anwendung standardmäßig nur Benutzern gestattet wird, die sich in den Rollen befinden, die der Anwendung zugeordnet sind. (Siehe [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md).) Alternativ können Sie den Zugriff auf alle Benutzer zulassen, indem Sie die Zugriffs Überprüfungen für eine COM+-Anwendung deaktivieren. (Siehe [Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md).)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kopieren von Komponenten](copying-components.md)
</dt> <dt>

[Eine COM+-Anwendung wird gelöscht.](deleting-a-com--application.md)
</dt> <dt>

[Importieren von Komponenten](importing-components.md)
</dt> <dt>

[Installieren neuer Komponenten](installing-new-components.md)
</dt> <dt>

[Verschieben von Komponenten](moving-components.md)
</dt> <dt>

[Entfernen einer Komponente aus einer COM+-Anwendung](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



