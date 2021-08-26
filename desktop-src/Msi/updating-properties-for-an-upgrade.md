---
description: Da das Upgrade den Namen der .msi-Datei und den Komponentencode einiger Komponenten ändert, muss der Produktcode des Upgrades von dem des ursprünglichen Produkts geändert werden.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Aktualisieren von Eigenschaften für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d340f56eaf78c585e28a52dc7b310bf1af047d7530e61b841267bc0b83251a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039180"
---
# <a name="updating-properties-for-an-upgrade"></a>Aktualisieren von Eigenschaften für ein Upgrade

Da das Upgrade den Namen der .msi-Datei und den Komponentencode einiger Komponenten ändert, muss der Produktcode des Upgrades von dem des ursprünglichen Produkts geändert werden. Eine Beschreibung der Fälle, in denen ein Upgrade erforderlich ist, um die [**ProductCode-Eigenschaft**](productcode.md) zu ändern, finden Sie unter [Ändern des Produktcodes.](changing-the-product-code.md) Ein Upgrade, das den ProductCode ändert, wird als [Hauptupgrade](major-upgrades.md)bezeichnet.

Die [**ProductName-Eigenschaft,**](productname.md) die [**ProductVersion-Eigenschaft,**](productversion.md) die [**ProductLanguage-Eigenschaft**](productlanguage.md) und die [**UpgradeCode-Eigenschaft**](upgradecode.md) des Upgradepakets können vom ursprünglichen Produkt geändert oder unverändert gelassen werden. Basierend auf den Werten dieser Eigenschaften kann Windows Installer bestimmen, ob zukünftige Upgradepakete auf das aktuelle Upgrade angewendet werden sollen.

Die in der ActionProperty -Spalte der [Upgrade-Tabelle](upgrade-table.md) angegebene Eigenschaft muss der [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md) hinzugefügt werden.

Verwenden Sie den Datenbank-Editor, um MNP2001.msi zu öffnen und die folgenden Daten in die [Tabelle Property](property-table.md)einzugeben. Die Liste enthält Links zu den Referenzthemen für integrierte Installationseigenschaften. Die Eigenschaftsnamen, bei denen es sich nicht um Links handelt, sind benutzerdefinierte Eigenschaften. Viele der Eigenschaften wurden aus Uisample.msi importiert, die im SDK enthalten sind. Weitere Informationen finden Sie unter [Importieren der Benutzeroberfläche](importing-the-user-interface.md).

[Eigenschaftentabelle](property-table.md)



| Eigenschaft                                         | Wert                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| Bannerbitmap                                     | bannrbmp                                  |
| ButtonText \_ Back                                 | < &Zurück                                |
| ButtonText \_ Browse                               | Br&owse                                   |
| ButtonText \_ Cancel                               | Abbrechen                                    |
| ButtonText \_ Exit                                 | &Beenden                                     |
| ButtonText \_ Finish                               | &Fertig stellen                                   |
| ButtonText \_ Ignore                               | &Ignorieren                                   |
| \_ButtonText-Installation                              | &Installieren                                  |
| ButtonText \_ Next                                 | &Next >                                |
| ButtonText \_ Nein                                   | &Nein                                       |
| ButtonText \_ OK                                   | OK                                        |
| ButtonText \_ Remove                               | &Entfernen                                   |
| ButtonText \_ Reset                                | &Zurücksetzen                                    |
| ButtonText \_ Resume                               | &Fortsetzen                                   |
| ButtonText \_ Retry                                | &Wiederholung                                    |
| \_ButtonText-Rückgabe                               | &Return                                   |
| ButtonText \_ Ja                                  | &Ja                                      |
| CompleteSetupIcon                                | completi                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| AusrufezeichenIcon                                  | ausrufend                                  |
| False                                            | 0                                         |
| Iagree                                           | Nein                                        |
| InfoIcon                                         | info                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Typisch                                   |
| [**Hersteller**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**Productid**](productid.md)                   | Keine                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**Productname**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progress1                                        | Installation                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| Einrichten                                            | Einrichten                                     |
| True                                             | 1                                         |
| [**Upgradecode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Assistent                                           | Setup-Assistenten                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[Fortsetzen](updating-sequence-tables-for-an-upgrade.md)

 

 



