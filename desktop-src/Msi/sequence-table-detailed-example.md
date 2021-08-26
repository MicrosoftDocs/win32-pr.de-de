---
description: Hier sehen Sie ein Beispiel für eine Sequenztabelle.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Detailliertes Beispiel für die Sequenztabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc6e9715850d05231080cd8cd832ac7f39c1e3044628bb307afb51bf92c2210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040190"
---
# <a name="sequence-table-detailed-example"></a>Detailliertes Beispiel für die Sequenztabelle

Hier sehen Sie ein Beispiel für eine Sequenztabelle.



| Aktion                                          | Bedingung                                                       | Sequenz |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | \_CCM-TEST                                                       | 300      |
| UEDialog                                       | NOT \_ CCP \_ SUCCESS                                               | 400      |
| MyCustomConfig                                  | NICHT [ **installiert**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [FileCost](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize](costfinalize-action.md)         |                                                                 | 800      |
| InstallDialog                                   | NICHT [ **installiert**](installed.md)                              | 900      |
| MaintenanceDialog                               | [**Installiert**](installed.md) AND NOT [ **Resume**](resume.md) | 1000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1600     |



 

Die folgenden Aktionen in dieser Sequenztabelle werden vom Installationsprogramm definiert und sind Beispiele für Standardaktionen:

[LaunchConditions](launchconditions-action.md)

 

[AppSearch](appsearch-action.md)

 

[CCPSearch](ccpsearch-action.md)

 

[CostInitialize](costinitialize-action.md)

 

[FileCost](filecost-action.md)

 

[CostFinalize](costfinalize-action.md)

 

[RegisterProduct](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

Die folgenden Aktionen wurden vom Autor der Tabelle definiert und sind Beispiele für [benutzerdefinierte Aktionen](custom-actions.md) und müssen in der [Tabelle CustomAction](customaction-table.md)aufgeführt werden:

MyCustomConfig

 

MyCustomAction

Die übrigen Einträge im Feld Aktion sind Fremdschlüssel in der [Dialogtabelle](dialog-table.md). Sie geben die Namen der Dialogfelder an, die angezeigt werden, wenn das Bedingungsfeld zu True ausgewertet wird.

UEDialog

 

InstallDialog

 

MaintenanceDialog

 

ActionDialog

Die Spalte Bedingung bewirkt, dass das Installationsprogramm die Aktion überspringt, wenn die Eigenschaft oder der Ausdruck in diesem Feld False ist. Die [**Installed-Eigenschaft**](installed.md) und die [**RESUME-Eigenschaft**](resume.md) sind Beispiele für Eigenschaften, die vom Installationsprogramm festgelegt werden. Die [**Installed-Eigenschaft**](installed.md) wird auf TRUE festgelegt, wenn das Produkt bereits installiert ist, und die [**RESUME-Eigenschaft**](resume.md) wird festgelegt, wenn eine angehaltene Installation fortgesetzt wird. Die Eigenschaften CCP \_ TEST und \_ NOTPC SUCCESS sind Beispiele für \_ Eigenschaften, die vom Benutzer, der die Anwendung installiert, in der Befehlszeile festgelegt werden können.

Alle Aktionen werden nacheinander mit den folgenden bedingten Schritten ausgeführt:

-   Die CPPSearch-Datei wird nur ausgeführt, wenn \_ KPCH TEST festgelegt ist.
-   CABDialog wird nur ausgeführt, wenn NOT \_ CCP \_ SUCCESS festgelegt ist.
-   MaintenanceDialog wird nur ausgeführt, wenn dieses Produkt bereits installiert ist und wenn es sich nicht um eine Installation handelt, die nach dem Anhalten fortgesetzt wird.
-   MyCustomAction wird nur ausgeführt, wenn der Ausdruck in der Spalte Bedingung true ist. Der Ausdruck $MyComponent > 2 bezieht sich auf den Aktionszustand der Komponente namens MyComponent. Diese Bedingung gibt an, dass MyCustomAction nur ausgeführt werden soll, wenn MyComponent auf die Installation festgelegt ist. Weitere Informationen zu Aktionszuständen und Auswahlzuständen finden Sie unter der [**FeatureRequestState-Eigenschaft,**](session-featurerequeststate.md) der [Featuretabelle](feature-table.md)und der [InstallFiles-Aktion](installfiles-action.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Syntax der bedingten Anweisung](conditional-statement-syntax.md)
</dt> </dl>

 

 



