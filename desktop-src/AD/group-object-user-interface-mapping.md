---
title: Zuordnung von Gruppen Objekt-Benutzeroberflächen
description: In diesem Thema werden die Eigenschaften Blätter für Gruppen Objekte im-Snap-in "Active Directory-Benutzer und-Computer" beschrieben. Allgemeines eigenschaftensheetmember der Eigenschaft sheetmembers-Eigenschaft sheetmanaged by Property Sheet
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Zuordnung von Gruppen Objekt-Benutzeroberflächen Zuordnung
- Zuordnung von Benutzeroberflächen, Gruppen Objekt-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2277c24f621f8e32f46b9e9571d0d0d4de9cfc
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038751"
---
# <a name="group-object-user-interface-mapping"></a>Zuordnung von Gruppen Objekt-Benutzeroberflächen

In diesem Thema werden die Eigenschaften Blätter für Gruppen Objekte im-Snap-in "Active Directory-Benutzer und-Computer" beschrieben.

-   [Eigenschaften Blatt "Allgemein"](#general-property-sheet)
-   [Mitglied des Eigenschaften Blatts](#member-of-property-sheet)
-   [Eigenschaften Blatt "Eigenschaften"](#members-property-sheet)
-   [Verwaltet von einem Eigenschaften Blatt](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Eigenschaften Blatt "Allgemein"

In der folgenden Tabelle werden die Benutzeroberflächen Bezeichnungen der **allgemeinen** Eigenschaften Seite angezeigt.



| UI-Bezeichnung                      | Attribut in Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Gruppen Name (Pre-Windows 2000) | [**Sam-Account-Name**](/windows/desktop/ADSchema/a-samaccountname) |
| BESCHREIBUNG                   | [**Beschreibung**](/windows/desktop/ADSchema/a-description)         |
| E-Mail                        | [**E-Mail-Adressen**](/windows/desktop/ADSchema/a-mail)           |
| Gruppenbereich                   | [**Gruppentyp**](/windows/desktop/ADSchema/a-grouptype)            |
| Gruppentyp                    | [**Gruppentyp**](/windows/desktop/ADSchema/a-grouptype)            |
| Notizen                         | [**Geäußert**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Mitglied des Eigenschaften Blatts

In der folgenden Tabelle werden die Benutzeroberflächen Bezeichnungen des-Elements **des** -Eigenschaften Blatts angezeigt.



| UI-Bezeichnung  | Attribut in Active Directory Domain Services | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mitglied von | [**Is-Member-of-DL**](/windows/desktop/ADSchema/a-memberof)    | Enthält die Distinguished Names der Gruppen, zu denen diese Gruppe gehört. Das Member-Attribut der einzelnen Gruppen in dieser Liste enthält den Distinguished Name dieses Gruppen Objekts. Die Benutzeroberfläche ändert das [**is-Member-of-DL**](/windows/desktop/ADSchema/a-memberof) -Attribut nicht direkt. Er ändert das [**Member**](/windows/desktop/ADSchema/a-member) -Attribut für das Group-Objekt, in dem dieses Objekt als Member erstellt wird. Der Active Directory Server verwaltet das **is-Member-of-DL** -Attribut.<br/> |



 

## <a name="members-property-sheet"></a>Eigenschaften Blatt "Eigenschaften"

In der folgenden Tabelle werden die Benutzeroberflächen Bezeichnungen **des Eigenschaften Blatts** "Eigenschaften" angezeigt.



| UI-Bezeichnung | Attribut in Active Directory Domain Services | BESCHREIBUNG                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Member  | [**Member**](/windows/desktop/ADSchema/a-member)               | Enthält die Distinguished Names der Member dieses Gruppen Objekts. |



 

## <a name="managed-by-property-sheet"></a>Verwaltet von einem Eigenschaften Blatt

In der folgenden Tabelle werden die Benutzeroberflächen Bezeichnungen des Eigenschaften Blatts " **verwaltet von** " angezeigt.



| UI-Bezeichnung                           | Attribut in Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Name                               | [**Verwaltet von**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Manager kann die Mitgliedschafts Liste aktualisieren | Keine. Ein ACE mit der Berechtigung "Allow-Write Members" wird dem durch den **Namen** identifizierten Konto hinzugefügt.                        |
| Office                             | Das [**Physical-delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) -Attribut des durch den **Namen** identifizierten Kontos. |
| Street                             | Das [**Straßen Adress**](/windows/desktop/ADSchema/a-street) Attribut des durch den **Namen** identifizierten Kontos.                                    |
| City                               | Das Attribut " [**lokalitäts Name**](/windows/desktop/ADSchema/a-l) " des durch den **Namen** identifizierten Kontos.                                          |
| Bundesland/Kanton                     | Das [**State-oder Province-Name-**](/windows/desktop/ADSchema/a-st) Attribut des durch den **Namen** identifizierten Kontos.                                |
| Land/Region                     | Das [**Country-Name**](/windows/desktop/ADSchema/a-c) -Attribut des durch den **Namen** identifizierten Kontos.                                           |
| Telefonnummer                   | Das [**Telefonnummern**](/windows/desktop/ADSchema/a-telephonenumber) Attribut des durch den **Namen** identifizierten Kontos.                         |
| Faxnummer                         | Das Attribut für das [**Fax-Telefonnummer**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) des Kontos, das durch den **Namen** identifiziert wird.      |



 

 

