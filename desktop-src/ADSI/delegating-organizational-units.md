---
title: Delegieren von Organisationseinheiten
description: Das Fabrikam-Unternehmen beauftragt zwei Administratoren, Mike und Paul, um die Organisationseinheiten "Ost" und "Europa, Westen" zu verwalten.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337137"
---
# <a name="delegating-organizational-units"></a>Delegieren von Organisationseinheiten

Das Fabrikam-Unternehmen beauftragt zwei Administratoren, Mike und Paul, um die Organisationseinheiten "Ost" und "Europa, Westen" zu verwalten. Joe delegiert seine administrativen Zuständigkeiten an Sie, damit Sie Benutzer in den jeweiligen Organisationseinheiten erstellen und löschen können.

Bevor Sie sehen, wie Sie diese Organisationseinheiten unter Mike und Paul einrichten, müssen Sie wissen, wie Sie den Zugriff auf Objekte in Active Directory einrichten. Jedes Objekt in Active Directory verfügt über eine Sicherheits Beschreibung. Mit der Sicherheits Beschreibung können Sie Berechtigungen für das Objekt ändern, Berechtigungen weitergeben, die Überwachung aktivieren usw. Die Sicherheits Beschreibung selbst verfügt über zwei Zugriffs Steuerungs Listen (Access Control Lists, ACLs): eine freigegebene ACL (DACL) und eine System-ACL (SACL). Jede ACL kann Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) enthalten. Mit einem ACE können Sie den zulässigen oder verweigerten Zugriff für ein Objekt festlegen. Außerdem können Sie bestimmte Aktionen angeben, die Sie zulassen oder verweigern möchten. Beispiele für Aktionen sind das Erstellen von untergeordneten Elementen, das Löschen von untergeordneten Elementen, Leseeigenschaften und Schreib Eigenschaften. Diese Rechte werden mit der [**AccessMask**](iadsaccesscontrolentry-property-methods.md)angegeben.

Als nächstes können Sie die Klassen oder Attribute angeben, denen dieser ACE zugeordnet ist. Im folgenden Beispiel für Fabrikam wählt Joe die Benutzerklasse aus, sodass jeder Administrator dem Systembenutzer hinzufügen kann. Als nächstes müssen Sie die folgende Frage beantworten: "Wer wird der Empfänger dieses ACE sein?" Joe legt Mike fest.

Schließlich können Sie das Verhalten der ACE-Vererbung festlegen – beispielsweise kann ACEs angegeben werden, um die Hierarchie nach unten zu übertragen. Zusammenfassend führt das vorherige Beispiel dazu, dass Mike in der Lage ist, Benutzer Objekte unter der Organisationseinheit "Ost Sales" zu erstellen und zu löschen.

Joe verwendet das folgende Codebeispiel, um die ACEs und ACLs für die Region "Osten" einzurichten.


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



In der folgenden Abbildung wird das Menü Active Directory **neue Ansicht erstellen** nach dem Ausführen des Codes angezeigt. Wenn sich Joe, der Administrator, anmeldet, sieht er verschiedene Klassen, die er erstellen kann. Wenn Mike sich jedoch anmeldet, kann er nur Benutzer Objekte erstellen.

![Optionsmenü "neue Ansicht erstellen"](images/adadsi5.png)

Weitere Informationen finden Sie unter [ADSI Security Model](adsi-security-model.md).

 

 




