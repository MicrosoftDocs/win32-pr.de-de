---
description: Im folgenden finden Sie ein Beispiel für eine Sequenz Tabelle.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Beispiel für eine detaillierte Sequenz Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352766"
---
# <a name="sequence-table-detailed-example"></a>Beispiel für eine detaillierte Sequenz Tabelle

Im folgenden finden Sie ein Beispiel für eine Sequenz Tabelle.



| Aktion                                          | Bedingung                                                       | Sequenz |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [Ccpsearch](ccpsearch-action.md)               | CCP- \_ Test                                                       | 300      |
| Ccpdialog                                       | kein \_ CCP- \_ Erfolg                                               | 400      |
| Mycustomconfig                                  | Nicht [ **installiert**](installed.md)                              | 500      |
| [Costinitialize](costinitialize-action.md)     |                                                                 | 600      |
| [Datei Kosten](filecost-action.md)                 |                                                                 | 700      |
| [Costfinalize](costfinalize-action.md)         |                                                                 | 800      |
| Installdialog                                   | Nicht [ **installiert**](installed.md)                              | 900      |
| Maintenancedialog                               | [**Installiert**](installed.md) Und nicht [  fortsetzen](resume.md) | 1000     |
| Aktions Dialogfeld                                    |                                                                 | 1100     |
| [Register Product](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1500     |
| [InstallFinalize wurde](installfinalize-action.md)   |                                                                 | 1600     |



 

Die folgenden Aktionen in dieser Sequenz Tabelle werden vom Installer definiert und sind Beispiele für Standard Aktionen:

[LaunchConditions](launchconditions-action.md)

 

[AppSearch](appsearch-action.md)

 

[Ccpsearch](ccpsearch-action.md)

 

[Costinitialize](costinitialize-action.md)

 

[Datei Kosten](filecost-action.md)

 

[Costfinalize](costfinalize-action.md)

 

[Register Product](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

Die folgenden Aktionen wurden vom Autor der Tabelle definiert und sind Beispiele für [benutzerdefinierte Aktionen](custom-actions.md) . Sie müssen in der [Tabelle CustomAction](customaction-table.md)aufgeführt werden:

Mycustomconfig

 

MyCustomAction

Die verbleibenden Einträge im Feld "Aktion" sind Fremdschlüssel in der [Dialog Tabelle](dialog-table.md). Sie geben die Namen von Dialogfeldern an, die angezeigt werden, wenn das Bedingungs Feld als true ausgewertet wird.

Ccpdialog

 

Installdialog

 

Maintenancedialog

 

Aktions Dialogfeld

Die Spalte Bedingung bewirkt, dass die Aktion vom Installer übersprungen wird, wenn die Eigenschaft oder der Ausdruck in diesem Feld den Wert false hat. Die [**installierte**](installed.md) Eigenschaft und die [**Resume**](resume.md) -Eigenschaft sind Beispiele für Eigenschaften, die vom Installationsprogramm festgelegt werden. Die [**installierte**](installed.md) Eigenschaft ist auf true festgelegt, wenn das Produkt bereits installiert ist, und die Eigenschaft [**wieder aufnehmen**](resume.md) festgelegt wird, wenn eine angehaltene Installation fortgesetzt wird. Die Eigenschaften "CCP \_ -Test" und "Not \_ CCP \_ Success" sind Beispiele für Eigenschaften, die von dem Benutzer, der die Anwendung installiert, an der Befehlszeile festgelegt werden kann.

Alle Aktionen werden nacheinander mit den folgenden Bedingungs Schritten ausgeführt:

-   Die cppsearch wird nur ausgeführt, wenn der CCP- \_ Test festgelegt ist.
-   Ccpdialog wird nur ausgeführt, wenn kein \_ CCP- \_ Erfolg festgelegt wurde.
-   Maintenancedialog wird nur ausgeführt, wenn dieses Produkt bereits installiert ist, und wenn es sich nicht um eine Installation handelt, die nach dem aussetzen fortgesetzt wird.
-   "MyCustomAction" wird nur ausgeführt, wenn der Ausdruck in der Spalte Bedingung "true" ist. Der Ausdruck $MyComponent > 2 bezieht sich auf den Aktionszustand der Komponente namens MyComponent. Diese Bedingung gibt an, dass "MyCustomAction" nur ausgeführt werden soll, wenn "MyComponent" als installiert festgelegt ist. Weitere Informationen zu Aktions Zuständen und Auswahl Zuständen finden Sie unter der [**featurerequeststate**](session-featurerequeststate.md) -Eigenschaft, der [Feature-Tabelle](feature-table.md)und der [InstallFiles-Aktion](installfiles-action.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Syntax der bedingten Anweisung](conditional-statement-syntax.md)
</dt> </dl>

 

 



