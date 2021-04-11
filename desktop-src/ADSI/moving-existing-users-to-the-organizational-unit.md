---
title: Verschieben vorhandener Benutzer in die Organisationseinheit
description: Wenn der Enterprise-Administrator Joe der die Windows NT 4,0-Domäne auf Active Directory aktualisiert, werden alle Benutzer und Gruppen zu den Benutzer Containern in der Fabrikam-Domäne migriert.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Verschieben vorhandener Benutzer in die Organisationseinheit AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206240"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Verschieben vorhandener Benutzer in die Organisationseinheit

Wenn der Enterprise-Administrator Joe der die Windows NT 4,0-Domäne auf Active Directory aktualisiert, werden alle Benutzer und Gruppen zu den Benutzer Containern in der Fabrikam-Domäne migriert. Joe kann nun diese Benutzer und Gruppen in die entsprechenden Organisationseinheiten verschieben. Ein Objekt kann auch mithilfe von ADSI zwischen verwandten Windows 2000-Domänen verschoben werden.

Im folgenden Codebeispiel verschiebt Joe "JeffSmith" in die Vertriebsorganisation.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



Die [**IADsContainer. muvehere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) -Methode nimmt den ADsPath des zu verschiebenden Objekts und den neuen Objektnamen (RDN). Wenn Sie den gleichen Namen beibehalten möchten, können Sie **null** (**vbNullString**) für den *bstrinnewname* -Parameter angeben. Um das Objekt umzubenennen, wenn es verschoben wird, geben Sie den neuen relativen Distinguished Name für den *bstrinnewname* -Parameter an. Wenn Sie z. b. JeffSmith in die Vertriebsorganisation verschieben und das "JeffSmith"-Objekt \_ im gleichen Vorgang in "Jeff Smith" umbenennen, würde Joe den folgenden Code ausführen:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen neuer Benutzer in der Organisationseinheit](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




