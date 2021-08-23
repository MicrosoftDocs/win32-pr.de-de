---
description: Active Directory-Objekte können verwendet werden, um Ressourcen in einer Computernetzwerkdomäne zu suchen, z. B. Benutzer, Sicherheitsrichtlinien, Drucker, verteilte Komponenten und andere Ressourcen.
ms.assetid: 96f89537-9419-495e-819c-fd07ba546620
ms.tgt_platform: multiple
title: Erstellen und Aktualisieren von Active Directory-Objekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e2b1cee8010a5eff143fc7ff073eeea5e83b3b46cb41177e5ddbde5e931e056
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374830"
---
# <a name="creating-and-updating-active-directory-objects"></a>Erstellen und Aktualisieren von Active Directory-Objekten

Active Directory-Objekte können verwendet werden, um Ressourcen in einer Computernetzwerkdomäne zu suchen, z. B. Benutzer, Sicherheitsrichtlinien, Drucker, verteilte Komponenten und andere Ressourcen. Active Directory-Objekte können mithilfe von WMI erstellt und aktualisiert werden. Sie können ein Active Directory-Objekt aktualisieren, wenn neue Informationen über das Objekt mithilfe der WMI-Ereignisbenachrichtigung verfügbar werden. Sobald beispielsweise ein Active Directory-Benutzerobjekt erstellt wurde, können Sie dessen Erstellung mit einer Ereignisabfrage in WMI erkennen. Wenn das Ereignis empfangen wird, können Sie das Objekt mit neuen Informationen aktualisieren.

Im folgenden Codebeispiel wird eine neue WMI-Instanz der -Klasse erstellt, die das Active Directory-Benutzerobjekt darstellt. Das Beispiel zeigt, wie Werte verschiedenen Eigenschaften zugewiesen werden, die zum Erstellen der neuen Active Directory-Benutzerinstanz erforderlich sind.


```VB
Const cUserID = "WMIUser"
Const cComputerName = "LocalHost"
Const cWMInamespace = "root/directory/LDAP"
Const cWMIclass = "ds_user"

Const ADS_UF_ACCOUNTDISABLE = &h000002

Set objWMILocator = _
    CreateObject("WbemScripting.SWbemLocator")
objWMILocator.Security_.AuthenticationLevel = _
    wbemAuthenticationLevelDefault

Set objWMIServices = objWMILocator. _
    ConnectServer(cComputerName, cWMInamespace, "", "")

Set objWMIClass = objWMIServices.Get(cWMIclass)

Set objWMIInstance = objWMIClass.SpawnInstance_

objWMIInstance.DS_sAMAccountName = userID
objWMIInstance.ADSIPath = "LDAP://CN=" & userID & _
    ",CN=Users,DC=LissWare,DC=Net"

objWMIInstance.Put_ (wbemChangeFlagCreateOrUpdate Or _
    wbemFlagReturnWhenComplete)

WScript.Echo "Active Directory user created."
```



Im folgenden Codebeispiel wird eine WMI-Instanz eines Active Directory-Objekts aktualisiert. In diesem Beispiel wird das Displayname-Attribut aktualisiert.


```VB
set svc = getObject("Winmgmts:root\directory\ldap")

' A context object is used to tell the provider which
' specific properties are going to be updated.  
' In most cases, when you update a WMI object you do not
' need to specify an additional context object. 
' However,  if a context object is not supplied for a
' directory service provider, the update fails.

set octx = createobject( _
    "wbemscripting.swbemnamedvalueset")
octx.add "__PUT_EXT_PROPERTIES", array("ds_displayname")
octx.add "__PUT_EXTENSIONS", true
octx.add "__PUT_EXT_CLIENT_REQUEST", true


set objEnum = svc.execQuery( _
    "select * from ds_computer where ds_cn = 'userName'", "WQL", 32)

for each obj in objEnum
 obj.ds_DisplayName = "updatedName"
 obj.put_ 1, octx
next

WScript.Echo "Active Directory user successfully updated"
```



 

 



