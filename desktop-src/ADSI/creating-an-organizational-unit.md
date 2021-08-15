---
title: Erstellen einer Organisationseinheit
description: Nachdem Sie nun über das Domänenobjekt verfügen, können Sie mit dem Erstellen von Organisationseinheiten beginnen.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Erstellen einer Organisationseinheit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf2db91c02836e2425cd25e72afe6e57ff6619948372a20d03079d65eee5c882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961989"
---
# <a name="creating-an-organizational-unit"></a>Erstellen einer Organisationseinheit

Nachdem Sie nun über das Domänenobjekt verfügen, können Sie mit dem Erstellen von Organisationseinheiten beginnen. Fabrikam verfügt über zwei Abteilungen: Vertrieb und Produktion. Das Unternehmen plant, zwei Windows 2.000 Administratoren für die Verwaltung der einzelnen Geschäftsbereiche zu einstellen. Joe Worden als Unternehmensadministrator erstellt zwei neue Organisationseinheiten unter der Domäne Fabrikam. Durch das Erstellen einer Organisationseinheit kann Joe mehrere Objekte gruppieren und eine andere Person diese Objekte verwalten lassen. Im folgenden Codebeispiel wird die Sales Organizational Unit (OU) erstellt.


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



Die [**IADsContainer.Create-Methode**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) akzeptiert den Klassennamen und den Namen des neuen Objekts. An diesem Punkt wird für das Objekt kein Committed in Active Directory erstellt. Sie verfügen jedoch über einen ADSI/COM-Objektverweis auf dem Client. Mit diesem ADSI-Objekt können Sie Attribute mithilfe der [**IADs.Put-Methode festlegen oder**](/windows/desktop/api/Iads/nf-iads-iads-put) ändern. Die **IADs.Put-Methode** akzeptiert den Attributnamen und den Wert des Attributs. Trotzdem wird nichts an das Verzeichnis gebunden. alles wird auf dem Client zwischengespeichert. Wenn Sie die [**IADs.SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aufrufen, werden die Änderungen, in diesem Fall objekterstellung und Attributänderung, in das Verzeichnis kopiert. Diese Änderungen werden durchgeführt, was bedeutet, dass entweder das neue Objekt mit allen von Ihnen festgelegten Attributen oder gar kein Objekt angezeigt wird.

Sie können auch Organisationseinheiten schachteln. Im folgenden Codebeispiel wird davon ausgegangen, dass die Division Sales weiter in die Regionen "East" und "West" unterteilt ist.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Dies gilt auch für die Region "Usa, Westen".

Um eine direkte Bindung an die Region "Osten" in der Vertriebsorganisation zu erstellen, geben Sie den Distinguished Name an.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Wenn Sie bereits an das übergeordnete Objekt (Sales) gebunden haben, können Sie eine Bindung an das untergeordnete Objekt (Osten) aus dem übergeordneten Objekt mithilfe des relativen Namens des untergeordneten Objekts erstellen.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Um sicherzustellen, dass die Objekte erstellt wurden, verwenden Sie Active Directory-Benutzer und -Computer MMC-Snap-In, um die neuen Organisationseinheiten zu sehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verschieben vorhandener Benutzer in die Organisationseinheit](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




