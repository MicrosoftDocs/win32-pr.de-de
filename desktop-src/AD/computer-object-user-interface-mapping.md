---
title: Zuordnung von Computer Objekt-Benutzeroberfläche
description: In der folgenden Tabelle sind die Elemente der Eigenschaften Blätter für Computer Objekte im Active Directory Snap-in "Benutzer und Computer" aufgeführt.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724616"
---
# <a name="computer-object-user-interface-mapping"></a>Zuordnung von Computer Objekt-Benutzeroberfläche

In der folgenden Tabelle sind die Elemente der Eigenschaften Blätter für Computer Objekte im Active Directory Snap-in "Benutzer und Computer" aufgeführt.

## <a name="general-property-sheet"></a>Eigenschaften Blatt "Allgemein"

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen der **allgemeinen** Eigenschaften Seite aufgeführt.



| UI-Bezeichnung                         | Active Directory Domain Services-Attribut | Kommentare                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| Computer Name (Pre-Windows 2000) | sAMAccountName                             |                                                  |
| DNS-Name                         | dNSHostName                                |                                                  |
| Role                             | userAccountControl                         | Schaltet ein Bit in der userAccountControl-Bitmaske um. |
| BESCHREIBUNG                      | description                                |                                                  |
| Computer für Delegierung Vertrauen    | userAccountControl                         | Schaltet ein Bit in der userAccountControl-Bitmaske um. |



 

## <a name="location-property-sheet"></a>Speicherort-Eigenschaften Blatt

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen des Eigenschaften Blatts **Location** aufgelistet.



| UI-Bezeichnung | Active Directory Domain Services-Attribut |
|----------|--------------------------------------------|
| Standort | location                                   |



 

## <a name="member-of-property-sheet"></a>Mitglied des Eigenschaften Blatts

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen des-Elements **des** -Eigenschaften Blatts aufgeführt.



| UI-Bezeichnung          | Active Directory Domain Services-Attribut | Kommentare                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mitglied von         | memberOf                                   | Schließt alle Gruppen in der UI-Liste ein, mit Ausnahme der primären Gruppe, die in der AD durch das [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) -Attribut dargestellt wird. |
| Primäre Gruppe festlegen | primaryGroupId                             | LDAP: an [**primarygrouptoken**](/windows/desktop/ADSchema/a-primarygrouptoken) der primären Gruppe gebunden.                                                                                  |



 

## <a name="operating-system-property-sheet"></a>Betriebs System-Eigenschaften Blatt

In der folgenden Tabelle sind die Benutzeroberflächen Bezeichnungen des **Betriebs System** -Eigenschaften Blatts aufgeführt.



| UI-Bezeichnung     | Active Directory Domain Services-Attribut |
|--------------|--------------------------------------------|
| Name         | operatingSystem                            |
| Version      | operatingSystemVersion                     |
| Service Pack | operatingSystemServicePack                 |



 

 

 