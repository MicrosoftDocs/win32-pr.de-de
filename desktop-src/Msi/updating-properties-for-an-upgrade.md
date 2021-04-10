---
description: Da beim Upgrade der Name der MSI-Datei geändert und der Komponenten Code einiger Komponenten geändert wird, muss der Produktcode des Upgrades von dem des ursprünglichen Produkts geändert werden.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Aktualisieren von Eigenschaften für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750c30a75650ff4009dda799b0542f41f535481f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050479"
---
# <a name="updating-properties-for-an-upgrade"></a>Aktualisieren von Eigenschaften für ein Upgrade

Da beim Upgrade der Name der MSI-Datei geändert und der Komponenten Code einiger Komponenten geändert wird, muss der Produktcode des Upgrades von dem des ursprünglichen Produkts geändert werden. Eine Beschreibung der Fälle, in denen ein Upgrade erforderlich ist, um die [**ProductCode**](productcode.md) -Eigenschaft zu ändern, finden Sie unter [Ändern des Produktcodes](changing-the-product-code.md). Ein Upgrade, bei dem der ProductCode geändert wird, wird als [Haupt Upgrade](major-upgrades.md)bezeichnet.

Die [**ProductName**](productname.md) -Eigenschaft, die [**ProductVersion**](productversion.md) -Eigenschaft, die [**productlanguage**](productlanguage.md) -Eigenschaft und die [**UpgradeCode-Eigenschaft des upgradepakets**](upgradecode.md) können vom ursprünglichen Produkt geändert oder unverändert bleiben. Basierend auf den Werten dieser Eigenschaften können Windows Installer bestimmen, ob zukünftige Upgradepakete auf das aktuelle Upgrade angewendet werden sollen.

Die in der Spalte "Aktion" der [upgradetabelle](upgrade-table.md) angegebene Eigenschaft muss der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft hinzugefügt werden.

Öffnen Sie MNP2001.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die [Eigenschaften Tabelle](property-table.md)ein. Die Liste enthält Links zu den Referenz Themen für integrierte Installer-Eigenschaften. Die Eigenschaftsnamen, die keine Verknüpfungen sind, sind vom Autor definierte Eigenschaften. Viele der Eigenschaften wurden aus Uisample.msi importiert, die im SDK verfügbar ist. Weitere Informationen finden Sie unter [Importieren der Benutzeroberfläche](importing-the-user-interface.md).

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft                                         | Wert                                     |
|--------------------------------------------------|-------------------------------------------|
| [**Arphelplink**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ zurück                                 | < &zurück                                |
| ButtonText \_ Durchsuchen                               | BR&owse                                   |
| ButtonText \_ Abbrechen                               | Abbrechen                                    |
| ButtonText \_ Beenden                                 | &beenden                                     |
| ButtonText- \_ Fertigstellen                               | &Fertigstellen                                   |
| ButtonText \_ ignorieren                               | &ignorieren                                   |
| ButtonText- \_ Installation                              | &Installation                                  |
| ButtonText \_ Next                                 | &nächsten >                                |
| ButtonText \_ Nein                                   | &Nein                                       |
| ButtonText \_ OK                                   | OK                                        |
| ButtonText \_ Entfernen                               | &entfernen                                   |
| ButtonText \_ Reset                                | &zurücksetzen                                    |
| Fortsetzen von \_ ButtonText                               | &fortsetzen                                   |
| ButtonText- \_ Wiederholung                                | &Wiederholung                                    |
| ButtonText- \_ Rückgabe                               | &Rückgabe                                   |
| ButtonText \_ Ja                                  | &ja                                      |
| Completesetupicon                                | completi                                  |
| Componentdownload                                | ftp://anonymous@microsoft.com/components/ |
| Customsetupicon                                  | custicon                                  |
| [**Defaultuifont**](defaultuifont.md)           | DlgFont8                                  |
| Dialogbitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | Errordlg                                  |
| Exclamationicon                                  | exclamic                                  |
| False                                            | 0                                         |
| Izustimmung                                           | Nein                                        |
| Infoicon                                         | info                                      |
| Installericon                                    | Initiator                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Typisch                                   |
| [**Hersteller**](manufacturer.md)             | Microsoft                                 |
| [**Pidtemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {34cf587c-1d8f-4dd5-adfe-440f4b593987}    |
| [**ProductID**](productid.md)                   | none                                      |
| [**Productlanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progress1                                        | Installation                                |
| Progress2                                        | installs                                  |
| [**Promptrollbackcost**](promptrollbackcost.md) | P                                         |
| Removeicon                                       | removico                                  |
| Repairicon                                       | repairic                                  |
| Setup                                            | Setup                                     |
| True                                             | 1                                         |
| [**UpgradeCode auch**](upgradecode.md)               | {908e378a-9551-4772-BF1D-5cfaf6fd9cb4}    |
| Assistent                                           | Setup-Assistenten                              |
| Securecustomproperties                           | Oldappfound                               |



 

[Fortsetzen](updating-sequence-tables-for-an-upgrade.md)

 

 



