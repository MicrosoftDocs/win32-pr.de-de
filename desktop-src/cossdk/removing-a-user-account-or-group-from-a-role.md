---
description: Wenn sich Benutzerberechtigungen ändern oder einer Anwendung Rollen hinzugefügt werden, können Sie ein Konto von einer Rolle in eine andere Rolle verschieben.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Entfernen eines Benutzerkontos oder einer Gruppe aus einer Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342612"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a>Entfernen eines Benutzerkontos oder einer Gruppe aus einer Rolle

Wenn die Berechtigungen eines Benutzers geändert werden oder einer Anwendung Rollen hinzugefügt werden, können Sie ein Konto von einer Rolle in eine andere Rolle verschieben. Wenn Sie ein Benutzerkonto oder eine Gruppe von Benutzern von einer Rolle in eine andere verschieben möchten, müssen Sie das Benutzerkonto oder die Gruppe aus der aktuellen Rolle entfernen und dann der neuen Rolle zuweisen.

**So verschieben Sie ein Benutzerkonto oder eine Gruppe von einer Rolle in eine andere**

1.  Entfernen Sie das Benutzerkonto oder die Gruppe aus der Rolle, der Sie nicht mehr angehören soll, wie folgt:

    1.  Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Rolle enthält, an der Sie interessiert sind. Erweitern Sie die Ansicht in der Konsolen Struktur, bis die Benutzer für die Rolle sichtbar sind.

    2.  Klicken Sie mit der rechten Maustaste auf das Benutzerkonto oder die Gruppe, das Sie entfernen möchten, und klicken Sie auf **Löschen**.

    3.  Wenn Sie im Dialogfeld **delete Element DELETE** aufgefordert werden, klicken Sie auf **Ja** , um das Benutzerkonto oder die Gruppe zu löschen.

    Das Benutzerkonto oder die Gruppe, das Sie aus der Rolle entfernt haben, wird nicht mehr im Ordner " **Benutzer** " angezeigt.

2.  Weisen Sie das Benutzerkonto oder die Gruppe, das Sie entfernt haben, den Rollen zu, denen der Benutzer oder die Gruppe zugewiesen werden soll. gehen Sie folgendermaßen vor:

    1.  Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Rolle enthält, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten. Erweitern Sie die Ansicht in der Konsolen Struktur, bis die Rollen der Anwendung sichtbar sind.

    2.  Suchen Sie die Rolle, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten.

        > [!Note]  
        > Wenn sich die gesuchte Rolle nicht im Ordner " **Rollen** " befindet, wurde die Rolle der Anwendung nicht hinzugefügt. Sie muss der Anwendung vom Entwickler hinzugefügt werden, bevor Sie der Rolle Benutzerkonten zuweisen können.

         

    3.  Klicken Sie mit der rechten Maustaste auf den Ordner **Benutzer** in der Rolle, zeigen Sie auf **neu**, und klicken Sie dann auf **Benutzer**.

    4.  Geben Sie im Fenster **Benutzer oder Gruppen auswählen** im unteren Bereich den voll qualifizierten Namen des Benutzers oder der Gruppe ein, den bzw. die Sie hinzufügen möchten. Wenn Sie den Namen nicht kennen, klicken Sie auf die Schaltfläche **erweitert** , und klicken Sie dann auf **Jetzt suchen** , um eine Liste der Benutzer und Gruppen in der ausgewählten Domäne anzuzeigen. Wählen Sie einen Benutzer oder eine Gruppe aus der Liste **Name (RDN)** aus, und klicken Sie auf **OK**.

    5.  Wenn Sie das Benutzerkonto oder die Gruppe der Rolle hinzugefügt haben, klicken Sie auf **OK**.

    Für jedes Benutzerkonto oder jede Gruppe, das Sie der Rolle zugewiesen haben, wird im Ordner **Benutzer** ein Symbol angezeigt.

Die geänderte Rollen Mitgliedschaft für das Benutzerkonto oder die Gruppe tritt beim nächsten Start der Anwendung in Kraft.

 

 



