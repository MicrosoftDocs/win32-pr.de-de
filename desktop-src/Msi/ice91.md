---
description: ICE91 gibt eine Warnung aus, wenn eine Datei, eine INI-Datei oder eine Verknüpfungs Datei in einem Verzeichnis pro Benutzer installiert wird.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350818"
---
# <a name="ice91"></a>ICE91

ICE91 gibt eine Warnung aus, wenn eine Datei, eine INI-Datei oder eine Verknüpfungs Datei in einem Verzeichnis pro Benutzer installiert wird. Diese Warnungen sind harmlos, wenn das Paket nur für die Installation im Einzelbenutzer- [Installations Kontext](installation-context.md) und nie für Installationen pro Computer verwendet wird.

Dateien, INI-Dateien oder Verknüpfungen in Verzeichnissen pro Benutzer werden im Profil eines bestimmten Benutzers installiert. Selbst wenn der Benutzer die Eigenschaft " [**ALLUSERS**](allusers.md) " für eine Installation pro Computer festlegt, werden Dateien, INI-Dateien oder Verknüpfungen in benutzerspezifischen Verzeichnissen nicht in das Profil "alle Benutzer" kopiert und sind anderen Benutzern nicht zur Verfügung. Die Verzeichnisse pro Benutzer sind nicht mit der Eigenschaft " **ALLUSERS** " unterschiedlich. Im folgenden finden Sie eine Liste der Verzeichnisse pro Benutzer:

-   AppDataFolder
-   FavoritesFolder
-   "Netthoodfolder"
-   PersonalFolder
-   Printhoodfolder
-   Recentfolder
-   Ordner "SendTo"
-   Mypicturesfolder
-   Localappdatafolder

## <a name="result"></a>Ergebnis

ICE91 gibt die folgenden Warnungen aus.



| ICE91-Warnung                                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Die Datei ' \[ 1 \] ' wird im pro-Benutzerverzeichnis ' \[ 2 ' installiert \] , das sich nicht basierend auf dem [**ALLUSERS**](allusers.md) -Wert unterscheidet. Diese Datei wird nicht in das Profil jedes Benutzers kopiert, auch wenn eine Installation pro Computer gewünscht ist.     | Die Datei wird in einem Verzeichnis pro Benutzer installiert. Sie wird während einer Installation pro Computer nicht in den Profilen der einzelnen Benutzer installiert.      |
| Die IniFile ' \[ 1 \] ' wird im pro-Benutzerverzeichnis ' \[ 2 ' installiert \] , das je nach Wert von [**ALLUSERS**](allusers.md) nicht unterschiedlich ist. Diese Datei wird nicht in das Profil jedes Benutzers kopiert, auch wenn eine Installation pro Computer gewünscht ist.  | Die INI-Datei wird in einem Verzeichnis pro Benutzer installiert. Sie wird während einer Installation pro Computer nicht in den Profilen der einzelnen Benutzer installiert. |
| Die Verknüpfung ' \[ 1 \] ' wird im pro-Benutzerverzeichnis ' \[ 2 ' installiert \] , das je nach Wert von [**ALLUSERS**](allusers.md) nicht variiert. Diese Datei wird nicht in das Profil jedes Benutzers kopiert, auch wenn eine Installation pro Computer gewünscht ist. | Die Verknüpfung wird in einem Verzeichnis pro Benutzer installiert. Sie wird während einer Installation pro Computer nicht in den Profilen der einzelnen Benutzer installiert.  |



 

## <a name="example"></a>Beispiel

ICE91 meldet die folgenden Warnungen für das Beispiel:

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

[Dateitabelle](file-table.md) (partiell)



| File  | Komponente\_ |
|-------|-------------|
| Datei1 | C1          |



 

[Komponenten Tabelle](component-table.md) (teilweise) (teilweise) (teilweise) (teilweise)



| Komponente | Verzeichnis\_ |
|-----------|-------------|
| C1        | "MyDir"       |



 

[INIFILE-Tabelle](inifile-table.md)



| INIFILE  | Dirproperty |
|----------|-------------|
| IniFile1 | Myinidir    |



 

[Verknüpfungs Tabelle](shortcut-table.md)



| Abkürzung  | Verzeichnis\_   |
|-----------|---------------|
| Shortcut1 | Myshortcutdir |



 

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis     | Über \_ geordnetes Verzeichnis  |
|---------------|--------------------|
| "MyDir"         | FavoritesFolder    |
| Myinidir      | Localappdatafolder |
| Myshortcutdir | PersonalFolder     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



