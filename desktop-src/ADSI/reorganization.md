---
title: Reorganisation
description: Die Vertriebsorganisation wurde in eine neue Organisation verschoben \ 8212; \ 0034; Vertrieb und Support. \ 0034; Julie Bankert wurde zum Vice President aufgestuft und wird die neue Organisation leiten.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Neuorganisierung von ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368b4db1909c50242e3eda1402e46896e54785aa66739b324995b7edbdd1b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690755"
---
# <a name="reorganization"></a>Reorganisation

Die Vertriebsorganisation wurde in eine neue Organisation verschoben: "Vertrieb und Support". Julie Bankert wurde zum Vice President aufgestuft und wird die neue Organisation leiten. Joe Worden, der Unternehmensadministrator, muss die Organisationseinheit "Sales" in eine neue Organisationseinheit (Sales and Support) verschieben.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Mit diesem Codebeispiel werden alle Objekte in der Vertriebsorganisationseinheit, einschließlich der untergeordneten Organisationseinheiten, in die neue Organisationseinheit verschoben.

Nun kann Joe Julie in die Organisationseinheit Vertrieb und Support verschieben.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Beachten Sie, dass der Manager-direct-Berichtslink zwischen Julie Bankert und Chris Gray automatisch von Active Directory aktualisiert wird.

**So erstellen Sie einen Active Directory-Bericht**

1.  Öffnen Sie Visual Basic Version 6.0, und wählen Sie **daten Project** aus, wenn Sie zur Eingabe des Projekttyps aufgefordert werden.
2.  Doppelklicken **Sie unter Daten Project** auf **Datenumgebung1**.
3.  Klicken Sie im Fenster **Datenumgebung** mit der rechten Maustaste auf das Verbindungsobjekt **(Connection1),** und wählen Sie **Eigenschaften** aus.
4.  Wählen Sie **OLE DB Anbieter für Microsoft Directory Services aus,** und klicken Sie auf **Weiter.**
5.  Wählen **Sie Use Windows NT Integrated security (Integrierte NT-Sicherheit verwenden)** aus, und klicken Sie auf **OK**. Dadurch wird ein Verbindungsobjekt erstellt.
6.  Klicken Sie erneut mit der rechten Maustaste auf das Fenster **Datenumgebung,** um **Befehl hinzufügen** auszuwählen. Klicken Sie mit der rechten Maustaste auf das **Command1-Objekt,** und wählen Sie **Eigenschaften** aus. Das folgende Dialogfeld **Command1-Eigenschaften** wird angezeigt.

    ![Command1-Eigenschaften (Dialogfeld)](images/adadsi3.png)

7.  Klicken Sie auf die Optionsschaltfläche **SQL Anweisung,** und geben Sie Folgendes ein:

    SELECT Name,phoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'

    Das **Command-Objekt** wird erstellt. Fügen Sie dem Bericht das **Command-Objekt** hinzu.

8.  Doppelklicken Sie im **fenster Project** auf **Datenbericht1.**
9.  Ziehen Sie das **Command1-Objekt** aus dem **Fenster DataEnvironment1** in den Abschnitt **Detail** im **Datenberichtsfenster.**
10. Wählen Sie unter **DataReport1-Eigenschaften** für **DataSource** im Pull-Down-Menü die Option **DataEnvironment1** und im Feld **DataMember** die Option **Command1** aus.
11. Klicken Sie im Projektfenster mit der rechten Maustaste auf **Daten Project**, und wählen Sie **DatenProjekteigenschaften** aus.
12. Wählen Sie im Dialogfeld **DataProject - Project Properties (Datenprojekt** – Project Eigenschaften) unter **Startobjekt** im Pull-Down-Menü die Option **DataReport1** aus. Klicken Sie zum Speichern auf **OK**.
13. Kompilieren Das folgende Dialogfeld **DataReport1** wird angezeigt.

    ![datareport1 (Dialogfeld)](images/adadsi4.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verknüpfen heterogener Daten](joining-heterogeneous-data.md)
</dt> </dl>

 

 




