---
description: Die RemoveExistingProducts-Aktion durchläuft die in der Spalte ActionProperty der Tabelle Upgrade aufgeführten Produktcodes und entfernt die Produkte nacheinander, indem gleichzeitige Installationen aufrufen.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: RemoveExistingProducts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3118ebd01aa39b0d9a5dad29ad1c3563c869ed5e0ebc8dfefd5ecd5c89301f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810930"
---
# <a name="removeexistingproducts-action"></a>RemoveExistingProducts-Aktion

Die RemoveExistingProducts-Aktion durchläuft die in der Spalte ActionProperty der [Tabelle Upgrade](upgrade-table.md) aufgeführten Produktcodes und entfernt die Produkte nacheinander, indem gleichzeitige Installationen aufrufen. Für jede gleichzeitige Installation legt das Installationsprogramm die [**ProductCode-Eigenschaft**](productcode.md) auf den Produktcode und die [**REMOVE-Eigenschaft**](remove.md) auf den Wert im Feld Entfernen der Tabelle Upgrade fest. Wenn das Feld Entfernen leer ist, wird der Wert standardmäßig auf ALL festgelegt, und das Installationsprogramm entfernt das gesamte Produkt.

Das Installationsprogramm führt die RemoveExistingProducts-Aktion nur bei der ersten Installation eines Produkts aus. Die Aktion wird während einer Wartungsinstallation [oder Deinstallation](maintenance-installation.md) nicht ausgeführt.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RemoveExistingProducts-Aktion muss in der Aktionssequenz an einem der folgenden Speicherorte geplant werden.

-   Zwischen der [InstallValidate-Aktion](installvalidate-action.md) und der [InstallInitialize-Aktion](installinitialize-action.md). In diesem Fall entfernt das Installationsprogramm die alten Anwendungen vollständig, bevor die neuen Anwendungen installiert werden. Dies ist eine ineffiziente Platzierung für die Aktion, da alle wiederverwendeten Dateien erneut kopiert werden müssen.
-   Nach der [InstallInitialize-Aktion](installinitialize-action.md) und vor allen Aktionen, die ein Ausführungsskript generieren.
-   Zwischen der [InstallExecute-Aktion](installexecute-action.md)oder der [InstallExecuteExecuteExecin-Aktion](installexecuteagain-action.md)und der [InstallFinalize-Aktion](installfinalize-action.md). Im Allgemeinen werden die letzten drei Aktionen direkt nacheinander geplant: InstallExecute, RemoveExistingProducts und InstallFinalize. In diesem Fall werden zuerst die aktualisierten Dateien installiert, und dann werden die alten Dateien entfernt. Wenn das Entfernen der alten Anwendung jedoch fehlschlägt, führt das Installationsprogramm ein Rollback sowohl für die Entfernung der alten Anwendung als auch für die Installation der neuen Anwendung aus.
-   Nach der [InstallFinalize-Aktion](installfinalize-action.md). Dies ist die effizienteste Platzierung für die Aktion. In diesem Fall aktualisiert das Installationsprogramm Dateien, bevor die alten Anwendungen entfernt werden. Nur die Dateien, die aktualisiert werden, werden während der Installation installiert. Wenn beim Entfernen der alten Anwendung ein Fehler auftritt, führt das Installationsprogramm nur ein Rollback für die Deinstallation der alten Anwendung aus.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Produkt entfernt.           |



 

## <a name="remarks"></a>Hinweise

Windows Das Installationsprogramm legt die [**UPGRADINGPRODUCTCODE-Eigenschaft**](upgradingproductcode.md) fest, wenn diese Aktion ausgeführt wird.

 

 



