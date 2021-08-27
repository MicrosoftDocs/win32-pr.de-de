---
description: ICE88 überprüft, ob das Verzeichnis, auf das in der DirProperty-Spalte der Tabelle IniFile verwiesen wird, im paket Windows Installer vorhanden ist.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb49ce6cb4363cfe89879f6e72b7ce801c063ea2b278c03dacf5cbadacddce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105220"
---
# <a name="ice88"></a>ICE88

ICE88 überprüft, ob das Verzeichnis, auf das in der DirProperty -Spalte der [IniFile-Tabelle](inifile-table.md) verwiesen wird, im paket Windows Installer vorhanden ist. ICE88 gibt eine Warnung aus, wenn der DirProperty-Wert keine Eigenschaft in den Tabellen Directory, AppSearch oder Property, bestimmte [Systemordnereigenschaften](property-reference.md)oder eine eigenschaft darstellt, die durch eine benutzerdefinierte Aktion vom Typ 51 festgelegt wurde.

ICE88 scannt die folgenden Tabellen und Eigenschaften.

-   [Verzeichnistabelle](directory-table.md)
-   [AppSearch-Tabelle](appsearch-table.md)
-   [Eigenschaftentabelle](property-table.md)
-   [Tabelle "CustomAction",](customaction-table.md) wobei die benutzerdefinierte Aktion ein [benutzerdefinierter Aktionstyp 51](custom-action-type-51.md) ist
-   [**ProgramFilesFolder-Eigenschaft**](programfilesfolder.md)
-   [**CommonFilesFolder-Eigenschaft**](commonfilesfolder.md)
-   [**SystemFolder-Eigenschaft**](systemfolder.md)
-   [**ProgramFiles64Folder-Eigenschaft**](programfiles64folder.md)
-   [**CommonFiles64Folder-Eigenschaft**](commonfiles64folder.md)
-   [**System64Folder-Eigenschaft**](system64folder.md)

## <a name="result"></a>Ergebnis

ICE88 gibt die folgende Warnung aus.



| ICE88-Warnung                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Im Tabelleneintrag IniFile (IniFile=) \[ 3 \] befindet sich DirProperty= \[ 1 nicht in den Tabellen \] Directory/Property/AppSearch/CA-Type51 und ist keine der Installereigenschaften. | Für jeden Datensatz in der Tabelle IniFile liest ICE88 den Wert in der DirProperty-Spalte. ICE88 sucht nach dem Wert in der [Verzeichnistabelle,](directory-table.md) [der AppSearch-Tabelle](appsearch-table.md)und der [Eigenschaftentabelle](property-table.md) und überprüft auch die Liste der Eigenschaften, die vom Installationsprogramm festgelegt wurden. ICE88 gibt diese Warnung aus, wenn der Wert im Scan nicht gefunden werden kann. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



