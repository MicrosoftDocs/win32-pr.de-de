---
description: ICE88 überprüft, ob das Verzeichnis, auf das in der dirproperty-Spalte der IniFile-Tabelle verwiesen wird, im Windows Installer Paket vorhanden ist.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867687"
---
# <a name="ice88"></a>ICE88

ICE88 überprüft, ob das Verzeichnis, auf das in der dirproperty-Spalte der [IniFile-Tabelle](inifile-table.md) verwiesen wird, im Windows Installer Paket vorhanden ist. ICE88 gibt eine Warnung aus, wenn der dirproperty-Wert keine Eigenschaft in den Verzeichnis-, AppSearch-oder Eigenschafts Tabellen, bestimmten [Systemordner Eigenschaften](property-reference.md)oder einer Eigenschaft darstellt, die durch eine benutzerdefinierte Aktion vom Typ 51 festgelegt wird.

ICE88 scannt die folgenden Tabellen und Eigenschaften.

-   [Verzeichnis Tabelle](directory-table.md)
-   [AppSearch-Tabelle](appsearch-table.md)
-   [Eigenschaften Tabelle](property-table.md)
-   [CustomAction-Tabelle](customaction-table.md) , in der die benutzerdefinierte Aktion ein [benutzerdefinierter Aktionstyp 51](custom-action-type-51.md) ist
-   [**ProgramFilesFolder (Eigenschaft)**](programfilesfolder.md)
-   [**CommonFilesFolder (Eigenschaft)**](commonfilesfolder.md)
-   [**SystemFolder-Eigenschaft**](systemfolder.md)
-   [**ProgramFiles64Folder-Eigenschaft**](programfiles64folder.md)
-   [**CommonFiles64Folder-Eigenschaft**](commonfiles64folder.md)
-   [**System64Folder-Eigenschaft**](system64folder.md)

## <a name="result"></a>Ergebnis

ICE88 gibt die folgende Warnung aus.



| ICE88-Warnung                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Im IniFile-Tabelleneintrag (iniFile =) \[ 3 wurde \] dirproperty = \[ 1 \] nicht in den Tabellen Directory/Property/AppSearch/ca-Type51 gefunden, und es handelt sich nicht um eine der Installer-Eigenschaften. | Für jeden Datensatz in der Tabelle "inifile" liest ICE88 den Wert in der dirproperty-Spalte. ICE88 scannt den Wert in der [Verzeichnis Tabelle](directory-table.md), der [AppSearch-Tabelle](appsearch-table.md)und der Eigenschaften [Tabelle](property-table.md) und scannt außerdem die Liste der Eigenschaften, die vom Installationsprogramm festgelegt werden. ICE88 gibt diese Warnung aus, wenn der Wert im Scan nicht gefunden werden kann. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



