---
title: Verschieben vorhandener Benutzer in die Organisationseinheit
description: Wenn der Unternehmensadministrator Joe Worden die Windows NT 4.0-Domäne auf Active Directory aktualisiert, werden alle Benutzer und Gruppen zu den Benutzercontainern in der Domäne Fabrikam migriert.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Verschieben vorhandener Benutzer in die Organisationseinheit AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26104feb5d4c8b6a1f24176ce23fcbb6ef6a965ca29c58887f02724b3ccba8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178954"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Verschieben vorhandener Benutzer in die Organisationseinheit

Wenn der Unternehmensadministrator Joe Worden die Windows NT 4.0-Domäne auf Active Directory aktualisiert, werden alle Benutzer und Gruppen zu den Benutzercontainern in der Domäne Fabrikam migriert. Joe kann diese Benutzer und Gruppen jetzt in die entsprechenden Organisationseinheiten verschieben. Ein Objekt kann auch mit ADSI zwischen verwandten Windows 2000 Domänen verschoben werden.

Im folgenden Codebeispiel verschiebt Joe "jeffsmith" in die Vertriebsorganisation.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



Die [**IADsContainer.MoveHere-Methode**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) verwendet den ADsPath des zu verschiebenden Objekts und den neuen Objektnamen (RDN). Um den gleichen Namen beizubehalten, können Sie **NULL** (**vbNullString**) für den *bstrNewName-Parameter* angeben. Um das Objekt beim Verschieben umzubenennen, geben Sie den neuen relativen Distinguished Name für den *bstrNewName-Parameter* an. Um jeffsmith beispielsweise in die Vertriebsorganisation zu verschieben und das Objekt "jeffsmith" in demselben Vorgang in "jeff smith" umzubenennen, \_ würde Joe den folgenden Code ausführen:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen neuer Benutzer in der Organisationseinheit](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




