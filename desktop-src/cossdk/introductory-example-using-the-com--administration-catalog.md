---
description: Einführendes Beispiel mit dem COM+-Verwaltungskatalog
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Einführendes Beispiel mit dem COM+-Verwaltungskatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfd085cbe9a829a1248ddf36057c9d9f79de9d576236a2621b237063340cf95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070590"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a>Einführendes Beispiel mit dem COM+-Verwaltungskatalog

Bei der programmgesteuerten Verwendung des COM+-Verwaltungskatalogs führen Sie in der Regel die folgenden allgemeinen Schritte aus (hier nicht in einer strengen Reihenfolge angegeben):

-   Öffnen Sie eine Sitzung mit dem COM+-Katalog auf dem lokalen Computer. Stellen Sie optional eine Verbindung mit dem COM+-Katalog auf einem Remotecomputer herstellen.
-   Ausführen von Aktionen wie dem Starten oder Beenden von Diensten– Aktionen, die sich nicht auf eine bestimmte COM+-Anwendung beziehen.
-   Ausführen von Aktionen wie dem Installieren oder Exportieren von COM+-Anwendungen oder dem Installieren von Komponenten in Anwendungen – Aktionen zum Lesen aus oder Schreiben in Dateien.
-   Fügen Sie Sammlungen neue Elemente hinzu, z. B. erstellen Sie eine neue COM+-Anwendung, indem Sie der Sammlung "Anwendungen" ein neues Element hinzufügen.
-   Legen Sie Eigenschaften für ein Element in einer Auflistung fest, oder erhalten Sie sie.
-   Speichern oder verwerfen Sie ausstehende Änderungen am Katalog.
-   Behandeln Sie alle Fehler, die auftreten können.

Um zu zeigen, wie diese Schritte aussehen, wenn Sie die COMAdmin-Objekte verwenden, finden Sie Visual Basic Microsoft-Beispiel. Es veranschaulicht kurz einige der oben beschriebenen typischen Schritte, z. B. das Suchen von Sammlungen, das Aufzählen einer Auflistung zum Abrufen eines Elements und das Festlegen von Eigenschaften für dieses Element.

Im folgenden Beispiel führen Sie die folgenden Aktionen aus:

1.  Erstellen Sie die neue COM+-Anwendung "MyHomeZoo".
2.  Installieren Sie einige Komponenten , Cat und Dog, in der Anwendung. Beide Komponenten sind in einer einzelnen DLL enthalten, die bereits vorhanden sein muss: MyZoo.dll.
3.  Konfigurieren Sie die rollenbasierte Sicherheit für die Anwendung, indem Sie zwei Rollen definieren: ZooKeeper und AberToCats.
4.  Weisen Sie der gesamten Anwendung zugriff auf die ZooKeeper-Rolle zu.
5.  Weisen Sie nur der Dog-Komponente den Zugriff auf die Rolle "SolltoCats" zu.
6.  Aktivieren Sie Sicherheitseigenschaften, damit die Rollenüberprüfung für die Anwendung erzwungen wird.
7.  Exportieren Sie die Anwendung MyHomeZoo in eine Datei, damit sie auf anderen Computern installiert werden kann.

Um dieses Beispiel aus Visual Basic verwenden zu können, fügen Sie einen Verweis auf die COM+-Administratortypbibliothek hinzu.


```VB
Function SetupMyZoo() As Boolean  ' Return False if any errors occur.

    '  Initialize error handling for this function.
    SetupMyZoo = False 
    On Error GoTo My_Error_Handler

    '  Open a session with the catalog.
    '  Instantiate a COMAdminCatalog object. 
    Dim objCatalog As COMAdminCatalog
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")

    '  Create a new COM+ application.
    '  First get the "Applications" collection from the catalog.
    Dim objApplicationsColl As COMAdminCatalogCollection
    Set objApplicationsColl = objCatalog.GetCollection("Applications")

    '  Add a new item to this collection. 
    Dim objZooApp As COMAdminCatalogObject
    Set objZooApp = objApplicationsColl.Add

    '  The "Applications" collection determines the available properties.
    '  Set the "Name" property of the new application item. 
    objZooApp.Value("Name") = "MyHomeZoo"

    '  Set the "Description" property of the new application item. 
    objZooApp.Value("Description") = "My pets at home"

    '  Save changes made to the "Applications" collection. 
    objApplicationsColl.SaveChanges

    '  Install components into the application.
    '  Use the InstallComponent method on COMAdminCatalog. 
    '  In this case, the last two parameters are passed as empty strings.
    objCatalog.InstallComponent "MyHomeZoo","MyZoo.DLL","","" 

    '  Define the roles ZooKeeper and AllergicToCats 
    '  by adding them to the "Roles" collection related to MyHomeZoo. 
    '  First get the "Roles" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Roles", 
    '  and the Key property value of objZooApp.   
    '  The Key property uniquely identifies the object, serving
    '  here to distinguish the "Roles" collection related 
    '  to MyHomeZoo from that of any other application. 
    Dim objRolesColl As COMAdminCatalogCollection
    Set objRolesColl = objApplicationsColl.GetCollection("Roles", objZooApp.Key)

    '  Add new items to this "Roles" collection. 
    Dim objZooKeeperRole As COMAdminCatalogObject
    Dim objAllergicToCatsRole As COMAdminCatalogObject
    Set objZooKeeperRole = objRolesColl.Add
    Set objAllergicToCatsRole = objRolesColl.Add

    '  Set the "Name" for the new items.
    objZooKeeperRole.Value("Name") = "ZooKeeper" 
    objAllergicToCatsRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to any items in this "Roles" collection. 
    objRolesColl.SaveChanges

    '  Assign the AllergicToCats role to the Dog component to 
    '  restrict its scope of access. (The ZooKeeper role, if assigned
    '  only at the application level, can access the whole application.)
    '  First get the "Components" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Components", and
    '  the Key property value of objZooApp. 
    Dim objZooComponentsColl As COMAdminCatalogCollection
    Set objZooComponentsColl = objApplicationsColl.GetCollection("Components", objZooApp.Key) 

    '  Find the Dog component item in this "Components" collection.
    '  First Populate the collection to read in data for all its items. 
    objZooComponentsColl.Populate

    '  Enumerate through the "Components" collection 
    '  until the Dog component item is located. 
    Dim objDog As COMAdminCatalogObject 
    For Each objDog in objZooComponentsColl
        If objDog.Name = "Dog" Then 
            Exit For
        End If
    Next 
    '  Set the role checking property at the component level for Dog.
        objDog.Value("ComponentAccessChecksEnabled") = True 

    '  Save these changes.
        objZooComponentsColl.SaveChanges
    '  Get the "RolesForComponent" collection related to the 
    '  Dog component, using the Key property of objDog. 
    Dim objRolesForDogColl As COMAdminCatalogCollection 
    Set objRolesForDogColl = objZooComponentsColl.GetCollection("RolesForComponent", objDog.Key) 

    '  Add a new item to this "RolesForComponent" collection. 
    Dim objCatSneezerRole As COMAdminCatalogObject
    Set objCatSneezerRole = objRolesForDogColl.Add

    '  Set the "Name" of the new item to be "AllergicToCats". 
    objCatSneezerRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to this "RolesForComponent" collection. 
    objRolesForDogColl.SaveChanges

    '  Now set properties to enforce role-based security. 
    '  First set role-based security at the application level.
    objZooApp.Value("ApplicationAccessChecksEnabled") = True 
    objZooApp.Value("AccessChecksLevel") = COMAdminAccessChecksApplicationComponentLevel 

    '  Save these changes.
    objApplicationsColl.SaveChanges

    '  Finally, export the new configured MyHomeZoo application to an 
    '  MSI file, used to install the application on other machines.
    '  Use the ExportApplication method on COMAdminCatalogObject.
    objCatalog.ExportApplication "MyHomeZoo", "c:\Program Files\COM applications\MyHomeZoo.MSI", 4

    '  Exit the function gracefully.
    SetupMyZoo = True

My_Error_Handler:
    If Not SetupMyZoo Then
        MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) & ")" & vbNewLine & Err.Description
    End If
    objCatSneezerRole = Nothing
    objRolesForDogColl = Nothing
    objDog = Nothing
    objZooComponentsColl = Nothing
    objAllergicToCatsRole = Nothing
    objZooKeeperRole = Nothing
    objRolesColl = Nothing
    objZooApp = Nothing
    objApplicationsColl = Nothing
    objCatalog = Nothing
Exit Function
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Verwaltungsvorgänge innerhalb von Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von COM+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am COM+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



