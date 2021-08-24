---
description: Windows Installereigenschaften sind globale Variablen, die das Installationsprogramm während einer Installation verwendet.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Angeben von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f538bb354ef793a54f3eb60ddfe7b75b2aa96310abdd8a7331813d887433816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627800"
---
# <a name="specifying-properties"></a>Angeben von Eigenschaften

Windows Installereigenschaften sind globale Variablen, die das Installationsprogramm während einer Installation verwendet. Weitere Informationen finden Sie in den Abschnitten unter [Eigenschaften.](properties.md) Wenn Sie [](importing-a-blank-database.md) im Abschnitt Importieren einer leeren Datenbank uisample.msi aus dem Windows Installer SDK verwendet haben, enthält die Tabelle [Eigenschaft](property-table.md) in Ihrer Kopie von MNP2000.msi bereits viele Eigenschaften, die von der Benutzeroberfläche verwendet werden. In diesem Abschnitt fügen Sie der Tabelle Eigenschaft zusätzliche Informationen hinzu, die für die Installation des Beispiels Editor sind. Weitere Informationen finden Sie [auch in der Gruppe "Program Information Tables".](program-information-tables-group.md)

Es gibt fünf Eigenschaften, die in jedem Installationspaket erforderlich sind. Diese müssen für das Editor-Beispiel in der [Tabelle Eigenschaft](property-table.md) des MNP2000.msi:

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**Hersteller**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**Productname**](productname.md)

Obwohl dies nicht für alle Installationspakete erforderlich ist, sollten Anwendungen, die in Zukunft möglicherweise ein Upgrade erhalten, auch eine [**UpgradeCode-Eigenschaft**](upgradecode.md) haben. Weitere Informationen finden Sie unter Preparing an Application for Future Major Upgrades (Vorbereiten einer Anwendung [für zukünftige Hauptupgrades).](preparing-an-application-for-future-major-upgrades.md)

Verwenden Sie ihren Datenbank-Editor, um MNP2000.msi, und geben Sie die folgenden Daten in die Tabelle Eigenschaft ein. Die Liste enthält Links zu den Referenzthemen für integrierte Installereigenschaften. Die Eigenschaftsnamen, die keine Links sind, sind vom Autor definierte Eigenschaften. Viele der eigenschaften, die aus uisample.msi importiert werden, sind für die Beispiel-Benutzeroberfläche. Im späteren Abschnitt Benutzeroberfläche für das Installationsbeispiel wird die Benutzeroberfläche erläutert.

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
| ButtonText \_ Install                              | &Installieren                                  |
| ButtonText \_ Next                                 | &nächste >                                |
| ButtonText \_ Nein                                   | &Nein                                       |
| ButtonText \_ OK                                   | OK                                        |
| ButtonText \_ Remove                               | &Entfernen                                   |
| ButtonText \_ Reset                                | &Zurücksetzen                                    |
| ButtonText \_ Resume                               | &Fortsetzen                                   |
| ButtonText \_ Retry                                | &Wiederholen                                    |
| ButtonText \_ Return                               | &Return                                   |
| ButtonText \_ Ja                                  | &Ja                                      |
| CompleteSetupIcon                                | completi                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | cus wie                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| AusrufezeichenIcon                                  | Ausrufezeichen                                  |
| False                                            | 0                                         |
| Iagree                                           | Nein                                        |
| InfoIcon                                         | info                                      |
| InstallerIcon                                    | ins wie                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Typisch                                   |
| [**Hersteller**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**Productid**](productid.md)                   | Keine                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**Productname**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progress1                                        | Installation                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| Einrichten                                            | Einrichten                                     |
| True                                             | 1                                         |
| [**Upgradecode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Assistent                                           | Setup-Assistenten                              |



 

[Fortsetzen](importing-the-installexecutesequence.md)

 

 



