---
description: Sie können das Verwaltungstool Komponentendienste verwenden, um eine Rolle mit Benutzerkonten oder Gruppen zu füllen.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Zuweisen eines Benutzerkontos oder einer Gruppe zu einer Rolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0d2883f9aedb5f3a0edf5dc33de54a03767e53a48f2dd8b9b6ea86c3a6211f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047668"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Zuweisen eines Benutzerkontos oder einer Gruppe zu einer Rolle

Sie können das Verwaltungstool Komponentendienste verwenden, um eine Rolle mit Benutzerkonten oder Gruppen zu füllen. Die bevorzugte Methode zum Zuweisen eines Benutzerkontos zu einer Rolle besteht im Zuweisen des Benutzerkontos zu einer Gruppe und anschließenden Zuweisen der Gruppe zur Rolle. Die Verwendung von Gruppen zum Auffüllen von Rollen erleichtert ihnen die Verwaltung einer großen Anzahl von Benutzern. Weitere Informationen zum Erstellen von Gruppen oder Zuweisen eines Benutzerkontos zu einer Gruppe finden Sie in der Onlinehilfe für das Verwaltungstool computerverwaltung im Thema "Lokale Benutzer und Gruppen".

> [!Note]  
> Damit nicht authentifizierte Netzwerkbenutzer eine COM+-Anwendung ausführen können, müssen die Anwendungsrollen den anonymen Benutzer enthalten. Ab Windows Server 2003 ist der anonyme Benutzer standardmäßig nicht in der Gruppe Jeder enthalten.

 

Nachdem Sie das Benutzerkonto der entsprechenden Windows-Gruppe zugewiesen haben, führen Sie die folgenden Schritte aus, um die Windows der Rolle zu zuweisen.

**So weisen Sie Windows Sicherheitsgruppe zu**

1.  Suchen Sie in der Konsolenstruktur des Komponentendienste-Verwaltungstools die COM+-Anwendung, die die Rolle enthält, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten. Erweitern Sie die Ansicht in der Konsolenstruktur, bis die Rollen der Anwendung sichtbar sind.

2.  Suchen Sie die Rolle, der Sie das Benutzerkonto oder die Gruppe hinzufügen möchten.

    > [!Note]  
    > Wenn sich die gesuchte Rolle nicht im Ordner **Rollen** befindet, wurde die Rolle der Anwendung nicht hinzugefügt. Sie muss der Anwendung vom Entwickler hinzugefügt werden, bevor Sie der Rolle Benutzerkonten zuweisen können.

     

3.  Klicken Sie mit der rechten **Maustaste auf** den Ordner Benutzer in der Rolle, zeigen Sie **auf Neu,** und klicken Sie dann auf **Benutzer**.

4.  Geben Sie **im Fenster Benutzer** oder Gruppen auswählen im unteren Bereich den vollqualifizierten Namen des Benutzers oder der Gruppe ein, den bzw. die Sie hinzufügen möchten. Wenn Sie den Namen nicht kennen, klicken Sie  auf die Schaltfläche **Erweitert** und dann auf Jetzt suchen, um eine Liste der Benutzer und Gruppen in der ausgewählten Domäne zu sehen. Wählen Sie in der Liste Name **(RDN)** einen Benutzer oder eine Gruppe aus, und klicken Sie auf **OK.**

5.  Wiederholen Sie Schritt 4, um weitere Benutzerkonten oder Gruppen hinzuzufügen.

6.  Wenn Sie das Hinzufügen von Benutzerkonten und Gruppen zur Rolle abgeschlossen haben, klicken Sie auf **OK.**

Für jedes Benutzerkonto oder jede Gruppe, das bzw. die Sie der Rolle zugewiesen haben, wird im Ordner **Benutzer ein Symbol** angezeigt. Die neue Rollenmitgliedschaft wird wirksam, wenn die Anwendung das nächste Mal gestartet wird.

 

 



