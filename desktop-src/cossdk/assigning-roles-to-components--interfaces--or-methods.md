---
description: Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393142"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden

Sie können einem beliebigen Element innerhalb einer COM+-Anwendung, die über das Verwaltungs Programmkomponenten Dienste sichtbar ist, explizit eine Rolle zuweisen. Dadurch wird sichergestellt, dass alle Benutzer, die Mitglieder der Rolle sind, Zugriff auf dieses Element und alle anderen darin enthaltenen Elemente erhalten. Wenn Sie z. b. die Rolle "Reader" einer Komponente zuweisen, wird jedem Mitglied von "Readers" der Zugriff auf diese Komponente und alle von ihr verfügbar gemachten Schnittstellen und Methoden gestattet. "Readers" wird als geerbte Rolle für diese Schnittstellen und Methoden angezeigt.

Aufrufer können nur von Aufrufern aufgerufen werden, indem Sie Ihr eine Rolle zuweisen, indem Sie die Rolle entweder direkt der-Methode zuweisen oder der-Schnittstelle der Methode oder der-Komponente der Methode eine Rolle zuweisen. in diesem Fall wird die Rolle von der-Methode geerbt. Wenn keine Rolle zugewiesen ist und Zugriffs Überprüfungen aktiviert sind, schlagen alle Aufrufe der-Methode fehl.

Bevor Sie eine Rolle zuweisen können, müssen Sie Sie für die Anwendung [definieren](defining-roles-for-an-application.md) . Alle für die Anwendung definierten Rollen werden im Fenster für **ausgewählte Elemente explizit** auf der Registerkarte **Sicherheit** für alle Komponenten, Methoden und Schnittstellen in der Anwendung angezeigt.

**So weisen Sie einer Komponente, Methode oder Schnittstelle Rollen zu**

1.  Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, für die die Rolle definiert wurde. Erweitern Sie die Struktur, um die Komponenten, Schnittstellen oder Methoden der Anwendung anzuzeigen, je nachdem, welchen Sie die Rolle zuweisen.

2.  Klicken Sie mit der rechten Maustaste auf das Element, dem Sie die Rolle zuweisen möchten, und klicken Sie dann auf **Eigenschaften**.

3.  Klicken Sie im Dialogfeld Eigenschaften auf die Registerkarte **Sicherheit** .

4.  Wählen Sie im Feld **explizit für ausgewählte Element (e) festgelegte Rollen** die Rollen aus, die Sie dem Element zuweisen möchten.

5.  Klicken Sie auf **OK**.

Alle Rollen, die Sie explizit für ein Element festgelegt haben, werden von den darin enthaltenen Elementen auf niedrigerer Ebene geerbt und in den Rollen angezeigt, die **vom ausgewählten Element (en)** für diese Elemente geerbt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffs Überprüfungen auf Komponentenebene](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



