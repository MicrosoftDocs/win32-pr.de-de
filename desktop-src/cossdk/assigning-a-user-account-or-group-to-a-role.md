---
description: Mit dem Verwaltungs Programmkomponenten Dienste können Sie eine Rolle mit Benutzerkonten oder Gruppen auffüllen.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Zuweisen eines Benutzerkontos oder einer Gruppe zu einer Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338918"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Zuweisen eines Benutzerkontos oder einer Gruppe zu einer Rolle

Mit dem Verwaltungs Programmkomponenten Dienste können Sie eine Rolle mit Benutzerkonten oder Gruppen auffüllen. Die bevorzugte Methode zum Zuweisen eines Benutzerkontos zu einer Rolle besteht darin, das Benutzerkonto einer Gruppe zuzuweisen und die Gruppe dann der Rolle zuzuweisen. Die Verwendung von Gruppen zum Auffüllen von Rollen erleichtert Ihnen die Verwaltung einer großen Anzahl von Benutzern. Weitere Informationen zum Erstellen von Gruppen oder Zuweisen eines Benutzerkontos zu einer Gruppe finden Sie in der Online Hilfe für das Verwaltungs Tool "Computer Verwaltung" im Thema "lokale Benutzer und Gruppen".

> [!Note]  
> Damit nicht authentifizierte Netzwerk Benutzer eine COM+-Anwendung ausführen können, müssen die Anwendungs Rollen den anonymen Benutzer einschließen. Ab Windows Server 2003 ist der anonyme Benutzer standardmäßig nicht in der Gruppe "jeder" enthalten.

 

Nachdem Sie das Benutzerkonto der entsprechenden Windows-Gruppe zugewiesen haben, führen Sie die folgenden Schritte aus, um die Windows-Gruppe der Rolle zuzuweisen.

**So weisen Sie einer Sicherheitsrolle eine Windows-Gruppe zu**

1.  Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Anwendung, die die Rolle enthält, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten. Erweitern Sie die Ansicht in der Konsolen Struktur, bis die Rollen der Anwendung sichtbar sind.

2.  Suchen Sie die Rolle, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten.

    > [!Note]  
    > Wenn sich die gesuchte Rolle nicht im Ordner " **Rollen** " befindet, wurde die Rolle der Anwendung nicht hinzugefügt. Sie muss der Anwendung vom Entwickler hinzugefügt werden, bevor Sie der Rolle Benutzerkonten zuweisen können.

     

3.  Klicken Sie mit der rechten Maustaste auf den Ordner **Benutzer** in der Rolle, zeigen Sie auf **neu**, und klicken Sie dann auf **Benutzer**.

4.  Geben Sie im Fenster **Benutzer oder Gruppen auswählen** im unteren Bereich den voll qualifizierten Namen des Benutzers oder der Gruppe ein, den bzw. die Sie hinzufügen möchten. Wenn Sie den Namen nicht kennen, klicken Sie auf die Schaltfläche **erweitert** , und klicken Sie dann auf **Jetzt suchen** , um eine Liste der Benutzer und Gruppen in der ausgewählten Domäne anzuzeigen. Wählen Sie einen Benutzer oder eine Gruppe aus der Liste **Name (RDN)** aus, und klicken Sie auf **OK**.

5.  Wenn Sie weitere Benutzerkonten oder Gruppen hinzufügen möchten, wiederholen Sie Schritt 4.

6.  Wenn Sie das Hinzufügen von Benutzerkonten und Gruppen zur Rolle abgeschlossen haben, klicken Sie auf **OK**.

Für jedes Benutzerkonto oder jede Gruppe, das Sie der Rolle zugewiesen haben, wird im Ordner **Benutzer** ein Symbol angezeigt. Die neue Rollen Mitgliedschaft tritt beim nächsten Start der Anwendung in Kraft.

 

 



