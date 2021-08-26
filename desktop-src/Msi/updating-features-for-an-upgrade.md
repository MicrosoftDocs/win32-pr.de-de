---
description: Im Beispiel Windows Installer-Upgradepakets werden dem ursprünglichen Produkt neue Features hinzugefügt.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Aktualisieren von Features für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a6febda0c13101cc7c0615526514ebe3fee24e2aa14bac1d07794206f2de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809906"
---
# <a name="updating-features-for-an-upgrade"></a>Aktualisieren von Features für ein Upgrade

Das Beispielupgradepaket fügt dem ursprünglichen Produkt drei neue Features hinzu:

-   Dies ist ein neues untergeordnetes Feature des Features "Sport".
-   Opera, ein neues untergeordnetes Feature des Features "Opera".
-   Dies ist ein neues untergeordnetes Feature des Gate-Features.

Verwenden Sie den Datenbank-Editor, um MNP2001.msi zu öffnen und die folgenden Daten in die [Featuretabelle](feature-table.md)einzugeben.

[Featuretabelle](feature-table.md)



| Feature    | \_Übergeordnetes Feature | Titel         | Beschreibung                | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Kunst       |                 | Kunst          | Events in Red Park.   | 18      | 3     | NOTEPADDIR  | 0          |
| Baseball   | Sport           | Baseball      | Baseball-Spiele             | 17      | 3     | SPORTDIR    | 32         |
| Konzert    | Kunst            | Konzert       | Concert events at Red Park | 19      | 3     | SIDEDIR     | 2          |
| Tanz      | Kunst            | Tanz         | Events in Red Park   | 21      | 3     | SIDEDIR     | 2          |
| Fußball   | Sport           | Fußball      | Football-Spiele             | 13      | 3     | SPORTDIR    | 2          |
| Gate       |                 | Gate          | Eintritte in Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Hilfe       | Editor         | Hilfe          | Hilfedatei.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January    | Gate            | January       | Januar-Zulassungen         | 7       | 3     | MONDIR      | 2          |
| NewYears   | January         | Neujahrstag | New Years Day Admissions   | 9       | 3     | HOLDIR      | 2          |
| Editor    |                 | Editor       | Editor Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Infodatei     | Editor         | Infodatei        | Readme-Datei                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport      |                 | Sportereignisse  | Sportereignisse im Red Park   | 12      | 3     | NOTEPADDIR  | 0          |
| Basketball | Sport           | Basketball    | Game Games           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | Kunst            | Opera         | Opera-Leistungen         | 23      | 3     | SIDEDIR     | 2          |
| Memorial   | Gate            | Memorial Day  | Memorial Day Admissions    | 11      | 3     | HOLDIR      | 2          |



 

Verwenden Sie den Datenbank-Editor, um MNP2001.msi zu öffnen und die folgenden Daten in die leere [FeatureComponents-Tabelle](featurecomponents-table.md)einzugeben.



| Feature\_  | Komponente\_ |
|------------|-------------|
| Baseball   | Baseball    |
| Konzert    | Konzert     |
| Tanz      | Tanz       |
| Fußball   | Fußball    |
| Hilfe       | Hilfe        |
| January    | January     |
| NewYears   | NewYears    |
| Editor    | Editor     |
| Infodatei     | Editor     |
| Basketball | Basketball  |
| Opera      | Opera       |
| Memorial   | Memorial    |



 

[Fortsetzen](updating-shortcuts-for-an-upgrade.md)

 

 



