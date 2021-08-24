---
description: Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fcec11a52182bc0c9ac6f643c6c9cd75cb7b7462c35bbdea1ad0bc401f6ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029860"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Zuweisen von Rollen zu Komponenten, Schnittstellen oder Methoden

Sie können jedem Element in einer COM+-Anwendung, das über das Verwaltungstool Komponentendienste sichtbar ist, explizit eine Rolle zuweisen. Dadurch wird sichergestellt, dass allen Benutzern, die Mitglieder der Rolle sind, Zugriff auf dieses Element und alle anderen darin enthaltenen Elemente gewährt wird. Wenn Sie z. B. einer Komponente die Rolle "Leser" zuweisen, wird jedem Mitglied von "Readers" Zugriff auf diese Komponente sowie auf alle Schnittstellen und Methoden gewährt, die sie verfügbar macht. "Readers" wird als geerbte Rolle für jede dieser Schnittstellen und Methoden angezeigt.

Auf eine Methode kann nur zugegriffen werden, wenn Sie ihr eine Rolle zuweisen, indem Sie die Rolle entweder explizit direkt der -Methode zuweisen, oder indem Sie der Schnittstelle der Methode oder der -Komponente der Methode eine Rolle zuweisen. In diesem Fall wird die Rolle von der -Methode geerbt. Wenn keine Rolle zugewiesen ist und Zugriffsüberprüfungen aktiviert sind, schlagen alle Aufrufe der -Methode fehl.

Bevor Sie eine Rolle zuweisen können, müssen Sie sie für die Anwendung [definieren.](defining-roles-for-an-application.md) Alle für die Anwendung definierten Rollen werden im Fenster Rollen, die **explizit für ausgewählte Elemente festgelegt sind,** auf der Registerkarte **Sicherheit** für alle Komponenten, Methoden und Schnittstellen innerhalb der Anwendung angezeigt.

**So weisen Sie einer Komponente, Methode oder Schnittstelle Rollen zu**

1.  Suchen Sie in der Konsolenstruktur des Component Services-Verwaltungstools die COM+-Anwendung, für die die Rolle definiert wurde. Erweitern Sie die Struktur, um die Komponenten, Schnittstellen oder Methoden der Anwendung anzuzeigen, je nachdem, was Sie der Rolle zuweisen.

2.  Klicken Sie mit der rechten Maustaste auf das Element, dem Sie die Rolle zuweisen möchten, und klicken Sie dann auf **Eigenschaften.**

3.  Klicken Sie im Eigenschaftendialogfeld auf die Registerkarte **Sicherheit.**

4.  Wählen Sie im Feld Rollen, die **explizit für ausgewählte Elemente festgelegt sind,** die Rollen aus, die Sie dem Element zuweisen möchten.

5.  Klicken Sie auf **OK**.

Alle Rollen, die Sie explizit für ein Element festgelegt haben, werden von allen darin enthaltenen Elementen auf niedrigerer Ebene geerbt und im Fenster Rollen angezeigt, die von ausgewählten Elementen für diese Elemente **geerbt** werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Role-Based Security](configuring-role-based-security.md)
</dt> <dt>

[Definieren von Rollen für eine Anwendung](defining-roles-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffsüberprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Aktivieren von Zugriffsüberprüfungen auf Komponentenebene](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



