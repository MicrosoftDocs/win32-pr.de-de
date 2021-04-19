---
description: Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db24f3985538b7189534c9fef3ef279ed240e3a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339705"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a>Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog

Wenn Sie den com+-Verwaltungs Katalog Programm gesteuert verwenden, führen Sie in der Regel die folgenden allgemeinen Schritte aus (Dies ist hier nicht in einer strengen Reihenfolge angegeben):

-   Öffnen Sie eine Sitzung mit dem com+-Katalog auf dem lokalen Computer. Stellen Sie optional eine Verbindung mit dem com+-Katalog auf einem Remote Computer her.
-   Aktionen ausführen, z. b. das Starten oder Beenden von Diensten – Aktionen, die sich nicht auf eine bestimmte COM+-Anwendung beziehen.
-   Führen Sie Aktionen aus, z. b. das Installieren oder Exportieren von com+-Anwendungen oder das Installieren von Komponenten in Anwendungen – Aktionen, die das Lesen oder schreiben in Dateien betreffen.
-   Hinzufügen neuer Elemente zu Sammlungen, z. b. Erstellen einer neuen COM+-Anwendung durch Hinzufügen eines neuen Elements zur Sammlung "Anwendungen".
-   Legen Sie Eigenschaften für ein Element in einer Auflistung fest oder legen Sie diese fest.
-   Speichern oder verwerfen Sie ausstehende Änderungen im Katalog.
-   Behandeln Sie eventuell auftretenden Fehler.

Um anzuzeigen, wie diese Schritte aussehen, wenn Sie die COMAdmin-Objekte verwenden, wird unten ein Microsoft Visual Basic-Beispiel bereitgestellt. Es werden einige der oben beschriebenen typischen Schritte kurz erläutert, wie z. b. das Suchen von Sammlungen, das Auflisten einer Auflistung zum Abrufen eines Elements und das Festlegen von Eigenschaften für dieses Element.

Im folgenden Beispiel führen Sie die folgenden Aktionen aus:

1.  Erstellen Sie eine neue COM+-Anwendung mit dem Namen "myhomezoo".
2.  Installieren Sie einige Komponenten (Cat und Dog) in der Anwendung. Beide Komponenten sind in einer einzigen dll enthalten, die bereits vorhanden sein muss: MyZoo.dll.
3.  Konfigurieren Sie die rollenbasierte Sicherheit für die Anwendung, indem Sie zwei Rollen definieren: Zookeeper und allergictocats.
4.  Weisen Sie der Zookeeper-Rolle den Zugriff auf die gesamte Anwendung zu.
5.  Weisen Sie der Rolle "allergicdecats" nur Zugriff auf die Dog-Komponente zu.
6.  Aktivieren Sie die Sicherheitseigenschaften, damit die Rollen Überprüfung für die Anwendung erzwungen wird.
7.  Exportieren Sie die Anwendung myhomezoo in eine Datei, damit Sie auf anderen Computern installiert werden kann.

Um dieses Beispiel in Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu.


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

[Com+-Verwaltungsvorgänge in Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



