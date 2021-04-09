---
title: Neuorganisation
description: 'Die Vertriebsorganisation wurde in eine neue Organisation verschoben: \ 8212; \ 0034; Vertrieb und Support. \ 0034; Julie Bankert wurde zu Vice President herauf gestuft und führt die neue Organisation aus.'
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Reorganisations-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036307"
---
# <a name="reorganization"></a>Neuorganisation

Die Vertriebsorganisation wurde in eine neue Organisation verlagert – "Vertrieb und Support". Julie Bankert wurde zu Vice President herauf gestuft und führt die neue Organisation aus. Joe von, der Unternehmens Administrator, muss Vertriebs-ou in eine neue Organisationseinheit, Vertrieb und Support verschieben.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Mit diesem Codebeispiel werden alle Objekte in der Organisationseinheit "Sales", einschließlich der untergeordneten Organisationseinheiten, in die neue Organisationseinheit verschoben.

Nun kann Joe Julie in die Organisationseinheit Vertrieb und Support verschieben.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Beachten Sie, dass die Verknüpfung "Manager-direkter Bericht" zwischen Julie Bankert und Chris Gray automatisch durch Active Directory aktualisiert wird.

**So erstellen Sie einen Active Directory Bericht**

1.  Öffnen Sie Visual Basic Version 6,0, und wählen Sie bei Aufforderung für den Projekttyp **Daten Projekt** aus.
2.  Doppelklicken Sie unter **Daten Projekt** auf **Data Environment1**.
3.  Klicken Sie im Fenster **Daten Umgebung** mit der rechten Maustaste auf das Verbindungs Objekt **(Connection1)** , und wählen Sie **Eigenschaften** aus.
4.  Wählen Sie **OLE DB Anbieter für Microsoft-Verzeichnisdienste aus**, und klicken Sie auf **weiter**.
5.  Wählen Sie **integrierte Sicherheit von Windows NT verwenden** aus, und klicken Sie auf **OK**. Dadurch wird ein Connection-Objekt erstellt.
6.  Klicken Sie mit der rechten Maustaste erneut auf das Fenster **Daten Umgebung** , um **Befehl hinzufügen** auszuwählen. Klicken Sie mit der rechten Maustaste auf **Command1** , und wählen Sie **Eigenschaften** aus. Das folgende Dialogfeld " **Command1-Eigenschaften** " wird angezeigt.

    ![Dialogfeld "Command1-Eigenschaften"](images/adadsi3.png)

7.  Klicken Sie auf das Optionsfeld **SQL-Anweisung** , und geben Sie Folgendes ein:

    SELECT Name, telefonienumber from ' LDAP://DC = fabrikam, DC = com ' WHERE objectCategory = ' Person ' and objectClass = ' User '

    Das **Command** -Objekt wird erstellt. Fügen Sie dem Bericht das **Befehls** Objekt hinzu.

8.  Doppelklicken Sie im **Projekt** Fenster auf **Data Report1** .
9.  Ziehen Sie das **Command1** -Objekt aus dem **DataEnvironment1** -Fenster in den **Detail** Abschnitt des **Datenbericht** Fensters.
10. Wählen Sie unter **DataReport1-Eigenschaften** für **Daten** Quelle im Pulldownmenü **DataEnvironment1** aus, und wählen Sie im Feld **DataMember** **Command1** aus.
11. Klicken Sie im Projektfenster mit der rechten Maustaste auf **Daten Projekt**, und wählen Sie **dataproject-Eigenschaften** aus.
12. Wählen Sie im Dialogfenster **dataproject-Projekteigenschaften** unter **Start Objekt** die Option **DataReport1** aus dem Pulldownmenü aus. Klicken Sie zum Speichern auf **OK**.
13. Kompilieren Das folgende Dialogfeld **DataReport1** wird angezeigt.

    ![datareport1 (Dialogfeld)](images/adadsi4.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beitreten zu heterogenen Daten](joining-heterogeneous-data.md)
</dt> </dl>

 

 




