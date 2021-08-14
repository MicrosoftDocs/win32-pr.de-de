---
title: Gruppenobjekt-Benutzeroberfläche Zuordnung
description: In diesem Thema werden die Eigenschaftenblätter des Gruppenobjekts im Active Directory-Benutzer und -Computer-Snap-In beschrieben. General Property SheetMember Of Property SheetMembers Property SheetManaged By Property Sheet
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Group Object Benutzeroberfläche Mapping AD
- Benutzeroberfläche Mapping,Group Object AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308b3bafc24f8b8419b23c351d981f4f01961885cd535ac2d24b96cd62e17633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188964"
---
# <a name="group-object-user-interface-mapping"></a>Gruppenobjekt-Benutzeroberfläche Zuordnung

In diesem Thema werden die Eigenschaftenblätter des Gruppenobjekts im Active Directory-Benutzer und -Computer-Snap-In beschrieben.

-   [Allgemeines Eigenschaftenblatt](#general-property-sheet)
-   [Member des Eigenschaftenblatts](#member-of-property-sheet)
-   [Members-Eigenschaftenblatt](#members-property-sheet)
-   [Von Eigenschaftenblatt verwaltet](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Allgemeines Eigenschaftenblatt

Die folgende Tabelle zeigt die Benutzeroberflächenbezeichnungen des **Eigenschaftenblatts Allgemein.**



| Benutzeroberflächenbezeichnung                      | Attribut in Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Gruppenname (vor Windows 2000) | [**SAM-Account-Name**](/windows/desktop/ADSchema/a-samaccountname) |
| BESCHREIBUNG                   | [**Beschreibung**](/windows/desktop/ADSchema/a-description)         |
| E-Mail                        | [**E-Mail-Adressen**](/windows/desktop/ADSchema/a-mail)           |
| Gruppenbereich                   | [**Gruppentyp**](/windows/desktop/ADSchema/a-grouptype)            |
| Gruppentyp                    | [**Gruppentyp**](/windows/desktop/ADSchema/a-grouptype)            |
| Hinweise                         | [**Kommentar**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Member des Eigenschaftenblatts

In der folgenden Tabelle sind die Benutzeroberflächenbezeichnungen des **Eigenschaftenblatts Member Of** aufgeführt.



| Benutzeroberflächenbezeichnung  | Attribut in Active Directory Domain Services | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mitglied von | [**Is-Member-of-DL**](/windows/desktop/ADSchema/a-memberof)    | Enthält die Distinguished Names der Gruppen, zu denen diese Gruppe gehört. Das Memberattribut der einzelnen Gruppen in dieser Liste enthält den Distinguished Name dieses Gruppenobjekts. Die Benutzeroberfläche ändert das [**Is-Member-Of-DL-Attribut nicht**](/windows/desktop/ADSchema/a-memberof) direkt. Sie ändert das [**Member-Attribut**](/windows/desktop/ADSchema/a-member) für das Gruppenobjekt, dessen Member dieses Objekt ist. Der Active Directory-Server verwaltet das **Is-Member-of-DL-Attribut.**<br/> |



 

## <a name="members-property-sheet"></a>Members-Eigenschaftenblatt

Die folgende Tabelle zeigt die Benutzeroberflächenbezeichnungen des **Eigenschaftenblatts Members.**



| Benutzeroberflächenbezeichnung | Attribut in Active Directory Domain Services | BESCHREIBUNG                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Member  | [**Member**](/windows/desktop/ADSchema/a-member)               | Enthält die Distinguished Names der Elemente dieses Gruppenobjekts. |



 

## <a name="managed-by-property-sheet"></a>Von Eigenschaftenblatt verwaltet

In der folgenden Tabelle sind die Benutzeroberflächenbezeichnungen des **Eigenschaftenblatts Verwaltet von** aufgeführt.



| Benutzeroberflächenbezeichnung                           | Attribut in Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Name                               | [**Verwaltet von**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Manager kann Mitgliedschaftsliste aktualisieren | Keine. Ein ACE mit der Berechtigung "Zulassen – Mitglieder schreiben" wird dem Konto hinzugefügt, das mit dem Namen identifiziert **wird.**                        |
| Office                             | Das [**Physical-Delivery-Office-Name-Attribut**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) des Kontos, das durch Name identifiziert **wird.** |
| Straße                             | Das [**Street-Address-Attribut**](/windows/desktop/ADSchema/a-street) des Kontos, das durch Name **identifiziert wird.**                                    |
| City                               | Das [**Locality-Name-Attribut**](/windows/desktop/ADSchema/a-l) des Kontos, das durch Name identifiziert **wird.**                                          |
| Bundesland/Kanton                     | Das [**State-Or-Province-Name-Attribut**](/windows/desktop/ADSchema/a-st) des Kontos, das durch Name **identifiziert wird.**                                |
| Land/Region                     | Das [**Country-Name-Attribut**](/windows/desktop/ADSchema/a-c) des Kontos, das durch Name **identifiziert wird.**                                           |
| Telefonnummer                   | Das [**Telephone-Number-Attribut**](/windows/desktop/ADSchema/a-telephonenumber) des Kontos, das durch Name **identifiziert wird.**                         |
| Faxnummer                         | Das [**Facsimile-Telephone-Number-Attribut**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) des Kontos, das anhand des Namens identifiziert **wird.**      |



 

 

