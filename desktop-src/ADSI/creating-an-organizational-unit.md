---
title: Erstellen einer Organisationseinheit
description: Nachdem Sie nun über das Domänen Objekt verfügen, können Sie damit beginnen, Organisationseinheiten zu erstellen.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Erstellen einer Organisationseinheit für ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947351"
---
# <a name="creating-an-organizational-unit"></a>Erstellen einer Organisationseinheit

Nachdem Sie nun über das Domänen Objekt verfügen, können Sie damit beginnen, Organisationseinheiten zu erstellen. Fabrikam hat zwei Bereiche: Vertrieb und Produktion. Das Unternehmen plant, zwei Windows 2000-Administratoren zur Verwaltung der einzelnen Abteilungen zu beauftragen. Joe kam, als Unternehmens Administrator, erstellt in der Domäne "Fabrikam" zwei neue Organisationseinheiten. Durch das Erstellen einer Organisationseinheit kann Joe mehrere Objekte gruppieren und anderen Personen die Möglichkeit geben, diese Objekte zu verwalten. Im folgenden Codebeispiel wird die Organisationseinheit "Sales" (OU) erstellt.


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



Die [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) -Methode akzeptiert den Klassennamen und den Namen des neuen Objekts. An diesem Punkt wird das Objekt nicht an Active Directory committet. Sie verfügen jedoch über einen ADSI/COM-Objekt Verweis auf dem Client. Mit diesem ADSI-Objekt können Sie Attribute mithilfe der [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) -Methode festlegen oder ändern. Die **IADs. Put** -Methode akzeptiert den Attributnamen und den Wert des Attributs. Trotzdem wird nichts in das Verzeichnis übertragen. alles wird auf dem Client zwischengespeichert. Wenn Sie die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode aufruft, werden die Änderungen, in diesem Fall die Objekt Erstellung und die Attribut Änderung, in das Verzeichnis übertragen. Diese Änderungen werden transaktiv durchgeführt. das bedeutet, dass Sie entweder das neue Objekt mit allen von Ihnen festgelegten Attributen oder überhaupt kein Objekt sehen werden.

Sie können auch Organisationseinheiten Schachteln. Im folgenden Codebeispiel wird davon ausgegangen, dass die Vertriebsabteilung in die Regionen "Osten" und "West" aufgeteilt ist.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Dies gilt auch für die Region "Europa, Westen".

Geben Sie den Distinguished Name an, um direkt an die Region "Osten" in der Vertriebsorganisation zu binden.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Wenn Sie bereits an das übergeordnete Objekt (Sales) gebunden sind, können Sie mit dem relativen Namen des untergeordneten Objekts an das untergeordnete Objekt (Osten) des übergeordneten Objekts binden.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Um sicherzustellen, dass die Objekte erstellt wurden, verwenden Sie das MMC-Snap-in "Active Directory-Benutzer und-Computer", um die neuen Organisationseinheiten anzuzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verschieben vorhandener Benutzer in die Organisationseinheit](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




