---
description: Das Beispiel Windows Installer Upgradepaket fügt dem ursprünglichen Produkt neue Features hinzu.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Aktualisieren von Features für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af072618bd0a2ba16a7f098d6b1129ba17c27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349528"
---
# <a name="updating-features-for-an-upgrade"></a>Aktualisieren von Features für ein Upgrade

Das Beispiel Aktualisierungs Paket fügt dem ursprünglichen Produkt drei neue Features hinzu:

-   Basketball, ein neues untergeordnetes Feature des Sport Features.
-   Opera, ein neues untergeordnetes Feature des Arts-Features.
-   Memorial, ein neues untergeordnetes Feature der Gate-Funktion.

Öffnen Sie MNP2001.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die [Funktions Tabelle](feature-table.md)ein.

[Funktions Tabelle](feature-table.md)



| Funktion    | Über \_ geordnetes Element | Titel         | BESCHREIBUNG                | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Grafiken       |                 | Grafiken          | Kunstveranstaltungen im red Park.   | 18      | 3     | Notepaddir  | 0          |
| Ball   | Sport           | Ball      | Baseball Spiele             | 17      | 3     | Sportdir    | 32         |
| Konzert    | Grafiken            | Konzert       | Konzertveranstaltungen im roten Park | 19      | 3     | Argsdir     | 2          |
| Abhängigkeit      | Grafiken            | Abhängigkeit         | Tanz Ereignisse im red Park   | 21      | 3     | Argsdir     | 2          |
| Verbandes   | Sport           | Verbandes      | Fußballspiele             | 13      | 3     | Sportdir    | 2          |
| Tors       |                 | Tors          | Zulassung von Red Park      | 6       | 3     | Notepaddir  | 0          |
| Hilfe       | Editor         | Hilfe          | Hilfedatei.                 | 5       | 3     | Notepaddir  | 1          |
| January    | Tors            | January       | Januar-Zuweisungen         | 7       | 3     | Mondir      | 2          |
| Newyears   | January         | Neuer Arbeitstag | Eintritts Zeit für neue Jahre   | 9       | 3     | Holdir      | 2          |
| Editor    |                 | Editor       | Editor für Notepad             | 1       | 3     | Notepaddir  | 0          |
| Infodatei     | Editor         | Infodatei        | Infodatei                | 3       | 3     | Notepaddir  | 0          |
| Sport      |                 | Sport Veranstaltungen  | Sport Veranstaltungen im roten Park   | 12      | 3     | Notepaddir  | 0          |
| Erinnen | Sport           | Erinnen    | Basketball Spiele           | 15      | 3     | Sportdir    | 2          |
| Opera      | Grafiken            | Opera         | Opernaufführungen         | 23      | 3     | Argsdir     | 2          |
| Denkmals   | Tors            | Gedenktag  | Eintrittstage für Gedenktage    | 11      | 3     | Holdir      | 2          |



 

Öffnen Sie MNP2001.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die leere [FeatureComponents-Tabelle](featurecomponents-table.md)ein.



| Funktion\_  | Komponente\_ |
|------------|-------------|
| Ball   | Ball    |
| Konzert    | Konzert     |
| Abhängigkeit      | Abhängigkeit       |
| Verbandes   | Verbandes    |
| Hilfe       | Hilfe        |
| January    | January     |
| Newyears   | Newyears    |
| Editor    | Editor     |
| Infodatei     | Editor     |
| Erinnen | Erinnen  |
| Opera      | Opera       |
| Denkmals   | Denkmals    |



 

[Fortsetzen](updating-shortcuts-for-an-upgrade.md)

 

 



