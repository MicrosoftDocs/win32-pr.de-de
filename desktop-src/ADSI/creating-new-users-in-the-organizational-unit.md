---
title: Erstellen neuer Benutzer in der Organisationseinheit
description: Terry Adams wurde bei der Fabrikam Sales-Organisation eingestellt. Sein direkter Bericht ist Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Erstellen neuer Benutzer in der Organisationseinheit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470805"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Erstellen neuer Benutzer in der Organisationseinheit

Terry Adams wurde bei der Fabrikam Sales-Organisation eingestellt. Sein direkter Bericht ist Patrick Hines.

Wie im folgenden Codebeispiel gezeigt, erstellt Joe andreshak, der Unternehmens Administrator, ein neues Konto für ihn.


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



Wenn Sie einen neuen Benutzer erstellen, müssen Sie einen **sAMAccountName** angeben. Dies ist ein obligatorisches Attribut für die User-Klasse. Bevor eine Instanz eines Objekts erstellt werden kann, müssen alle obligatorischen Attribute festgelegt werden. Der **sAMAccountName** wird automatisch generiert, wenn ein neuer Benutzer nicht angegeben wird.

Beim Erstellen eines neuen Benutzers müssen alle erforderlichen Attribute im lokalen Cache festgelegt werden, bevor die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode aufgerufen wird.

Joe kann als Administrator das Kennwort von Terry mithilfe der [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) -Methode zuweisen. Die **IADsUser. SetPassword** -Methode funktioniert erst, wenn die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode aufgerufen wurde.

Anschließend aktiviert Joe das Benutzerkonto, indem die [**IADsUser. accountdeaktiviert**](iadsuser-property-methods.md) -Eigenschaft auf **false** festgelegt wird.

Im folgenden Codebeispiel wird gezeigt, wie Oliver als Manager für Patrick festgelegt wird.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Sie Fragen sich vielleicht, was passiert, wenn Terry seinen Namen ändert, zu einer anderen Organisation wechselt oder das Unternehmen verlässt. Wer verwaltet diesen Manager-Direct Report Link? Weitere Informationen und die Lösung für dieses Problem finden Sie unter [Neuorganisation](reorganization.md). Da das Active Directory Schema erweiterbar ist, können Sie die Objekte modellieren, um ähnliche Manager-direkte Berichts Stil Beziehungen einzubeziehen.

Bevor Sie mit der nächsten Aufgabe fortfahren, sehen Sie sich ein Codebeispiel an, das zeigt, wie Joe die direkten Berichte von Oliver anzeigen würde.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



In diesem Codebeispiel wird Patrick als direkter Bericht von Oliver angezeigt, auch wenn das **DirectReports** -Attribut nie geändert wurde. Active Directory führt dies automatisch aus.

In der Verzeichnis Welt kann ein Attribut einen einzelnen oder mehrere Werte aufweisen. Da **DirectReports** über mehrere Werte verfügen, können Sie diese Informationen überprüfen, indem Sie sich das Schema ansehen. es ist einfacher, die [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode zu verwenden, die ein Array von Werten zurückgibt, unabhängig davon, ob ein oder mehrere Werte zurückgegeben werden.

Mit dem Snap-in "Active Directory-Benutzer und-Computer" können Sie direktberichte und Manager Beziehungen auf der Eigenschaften Seite des Benutzers anzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von Benutzern zu einer Gruppe](adding-users-to-a-group.md)
</dt> </dl>

 

 




