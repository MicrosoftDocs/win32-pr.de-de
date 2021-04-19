---
description: Windows Installer Eigenschaften sind globale Variablen, die vom Installationsprogramm während einer Installation verwendet werden.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Angeben von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd4294f35595e723491398172dc4c73337a1416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349156"
---
# <a name="specifying-properties"></a>Angeben von Eigenschaften

Windows Installer Eigenschaften sind globale Variablen, die vom Installationsprogramm während einer Installation verwendet werden. Weitere Informationen finden Sie in den Abschnitten unter [Eigenschaften](properties.md). Wenn Sie im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md) , die Sie uisample.msi aus dem Windows Installer SDK verwendet haben, die Eigenschaften [Tabelle](property-table.md) in Ihrer Kopie von MNP2000.msi bereits viele Eigenschaften enthält, die von der Benutzeroberfläche verwendet werden. In diesem Abschnitt fügen Sie der Eigenschaften Tabelle, die für die Installation des Notepad-Beispiels spezifisch ist, zusätzliche Informationen hinzu. Weitere Informationen finden Sie auch in der [Gruppe Programm Informationstabellen](program-information-tables-group.md).

In jedem Installationspaket sind fünf Eigenschaften erforderlich, die für das Notepad-Beispiel in der [Eigenschaften Tabelle](property-table.md) MNP2000.msi aktualisiert werden müssen:

-   [**ProductCode**](productcode.md)
-   [**Productlanguage**](productlanguage.md)
-   [**Hersteller**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**ProductName**](productname.md)

Obwohl Sie nicht für alle Installationspakete erforderlich sind, sollten Anwendungen, die in Zukunft ein Upgrade erhalten, auch über eine [**UpgradeCode**](upgradecode.md) -Eigenschaft verfügen. Weitere [wichtige Upgrades finden Sie unter Vorbereiten einer Anwendung](preparing-an-application-for-future-major-upgrades.md).

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Eigenschaften Tabelle ein. Die Liste enthält Links zu den Referenz Themen für integrierte Installer-Eigenschaften. Die Eigenschaftsnamen, die keine Verknüpfungen sind, sind vom Autor definierte Eigenschaften. Viele der aus uisample.msi importierten Eigenschaften gelten für die Beispiel Benutzeroberfläche. Der spätere Abschnitt Benutzeroberfläche für das Installations Beispiel erläutert die Benutzeroberfläche.

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
| [**ProductCode**](productcode.md)               | {18a9233c-0b34-4127-a966-c257386270bc}    |
| [**ProductID**](productid.md)                   | none                                      |
| [**Productlanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progress1                                        | Installation                                |
| Progress2                                        | installs                                  |
| [**Promptrollbackcost**](promptrollbackcost.md) | P                                         |
| Removeicon                                       | removico                                  |
| Repairicon                                       | repairic                                  |
| Setup                                            | Setup                                     |
| True                                             | 1                                         |
| [**UpgradeCode auch**](upgradecode.md)               | {908e378a-9551-4772-BF1D-5cfaf6fd9cb4}    |
| Assistent                                           | Setup-Assistenten                              |



 

[Fortsetzen](importing-the-installexecutesequence.md)

 

 



