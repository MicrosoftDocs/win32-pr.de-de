---
description: Die Aktion "RemoveExistingProducts" durchläuft die in der Spalte "action Property" der upgradetabelle aufgeführten Produktcodes und entfernt die Produkte nacheinander, indem parallele Installationen aufgerufen werden.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: RemoveExistingProducts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351693"
---
# <a name="removeexistingproducts-action"></a>RemoveExistingProducts-Aktion

Die Aktion "RemoveExistingProducts" durchläuft die in der Spalte "action Property" der [upgradetabelle](upgrade-table.md) aufgeführten Produktcodes und entfernt die Produkte nacheinander, indem parallele Installationen aufgerufen werden. Der Installer legt für jede gleichzeitige Installation die [**ProductCode**](productcode.md) -Eigenschaft auf den Produktcode fest und legt die [**Remove**](remove.md) -Eigenschaft auf den Wert im Feld entfernen der upgradetabelle fest. Wenn das Feld entfernen leer ist, lautet der Wert standardmäßig alle, und das Installationsprogramm entfernt das gesamte Produkt.

Der Installer führt die Aktion RemoveExistingProducts nur bei der erstmaligen Installation eines Produkts aus. Die Aktion wird während einer [Wartungs Installation](maintenance-installation.md) oder-Installation nicht ausgeführt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion "RemoveExistingProducts" muss in der Aktions Sequenz an einem der folgenden Speicherorte geplant werden.

-   Zwischen der [InstallValidate-Aktion](installvalidate-action.md) und der [InstallInitialize-Aktion](installinitialize-action.md). In diesem Fall entfernt das Installationsprogramm die alten Anwendungen vollständig, bevor die neuen Anwendungen installiert werden. Dies ist eine ineffiziente Platzierung für die Aktion, da alle wiederverwendeten Dateien neu kopiert werden müssen.
-   Nach der [InstallInitialize-Aktion](installinitialize-action.md) und vor den Aktionen, mit denen Ausführungs Skript generiert wird.
-   Zwischen der [InstallExecute-Aktion](installexecute-action.md)oder der [InstallExecuteAgain](installexecuteagain-action.md)-Aktion und der [InstallFinalize](installfinalize-action.md)-Aktion. Im Allgemeinen werden die letzten drei Aktionen direkt aufeinander geplant: InstallExecute, RemoveExistingProducts und InstallFinalize. In diesem Fall werden die aktualisierten Dateien zuerst installiert, dann werden die alten Dateien entfernt. Wenn beim Entfernen der alten Anwendung jedoch ein Fehler auftritt, führt der Installer sowohl das Entfernen der alten Anwendung als auch die Installation der neuen Anwendung aus.
-   Nach der [InstallFinalize-Aktion](installfinalize-action.md). Dies ist die effizienteste Platzierung für die Aktion. In diesem Fall aktualisiert der Installer Dateien, bevor die alten Anwendungen entfernt werden. Nur die zu Aktualisier Ende Dateien werden während der Installation installiert. Wenn das Entfernen der alten Anwendung fehlschlägt, führt das Installationsprogramm nur ein Rollback für die Deinstallation der alten Anwendung aus.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Das Produkt wurde entfernt.           |



 

## <a name="remarks"></a>Bemerkungen

Windows Installer legt die [**upgradingproductcode**](upgradingproductcode.md) -Eigenschaft fest, wenn diese Aktion ausgeführt wird.

 

 



