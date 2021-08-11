---
title: Erstellen neuer Benutzer in der Organisationseinheit
description: Adams wurde in der Fabrikam Sales-Organisation eingestellt. Sein direkter Bericht ist Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Erstellen neuer Benutzer in der Organisationseinheit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76d62c8d95e7d5e421fc562e38716477ff2dfb8f4097d4652710e2c50715487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180115"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Erstellen neuer Benutzer in der Organisationseinheit

Adams wurde in der Fabrikam Sales-Organisation eingestellt. Sein direkter Bericht ist Patrick Hines.

Wie im folgenden Codebeispiel gezeigt, erstellt Joe Andreshak, der Unternehmensadministrator, ein neues Konto für ihn.


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



Beim Erstellen eines neuen Benutzers müssen Sie einen **sAMAccountName angeben.** Dies ist ein obligatorisches Attribut für die Benutzerklasse. Bevor eine Instanz eines Objekts erstellt werden kann, müssen alle obligatorischen Attribute festgelegt werden. Der sAMAccountName wird automatisch generiert, wenn kein **sAMAccountName** für einen neuen Benutzer angegeben ist.

Beim Erstellen eines neuen Benutzers müssen alle erforderlichen Attribute im lokalen Cache festgelegt werden, bevor die [**IADs.SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aufgerufen wird.

Joe kann als Administrator mithilfe der [**IADsUser.SetPassword-Methode**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) das Kennwort von Administrators zuweisen. Die **IADsUser.SetPassword-Methode** funktioniert erst, wenn die [**IADs.SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aufgerufen wurde.

Anschließend aktiviert Joe das Benutzerkonto, indem die [**IADsUser.AccountDisabled-Eigenschaft**](iadsuser-property-methods.md) auf **FALSE festgelegt wird.**

Im folgenden Codebeispiel wird gezeigt, wie Sie Als Patricks Vorgesetzter festlegen.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Sie fragen sich vielleicht, was passiert, wenn Chef seinen Namen ändert, in eine andere Organisation wechselt oder das Unternehmen verlässt. Wer diesen Manager-Direct-Berichtslink? Weitere Informationen und die Lösung für dieses Problem finden Sie unter [Neuorganisation von](reorganization.md). Da das Active Directory-Schema erweiterbar ist, können Sie Ihre Objekte so modellieren, dass sie ähnliche Beziehungen im Manager-Direct-Berichtsstil enthalten.

Bevor Sie mit der nächsten Aufgabe los gehen, sehen Sie sich ein Codebeispiel an, das zeigt, wie Joe Die direkten Berichte von Joe anzeigen würde.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



In diesem Codebeispiel wird Patrick als direkter Bericht von Patrick angezeigt, obwohl das **directReports-Attribut** nie geändert wurde. Active Directory führt dies automatisch durch.

In der Verzeichniswelt kann ein Attribut über einzelne oder mehrere Werte verfügen. Da **directReports** über mehrere Werte verfügt, können Sie diese Informationen über das Schema erhalten. Es ist einfacher, die [**IADs.GetEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getex) zu verwenden, die unabhängig davon, ob einzelne oder mehrere Werte zurückgegeben werden, ein Array von Werten zurückgibt.

Mit Active Directory-Benutzer und -Computer-Snap-In können Sie direkte Berichte und Managerbeziehungen auf der Eigenschaftenseite des Benutzers anzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von Benutzern zu einer Gruppe](adding-users-to-a-group.md)
</dt> </dl>

 

 




