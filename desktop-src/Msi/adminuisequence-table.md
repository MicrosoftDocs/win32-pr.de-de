---
description: In der Tabelle AdminUISequence werden Aktionen aufgeführt, die das Installationsprogramm nacheinander aufruft, wenn die ADMIN-Aktion der obersten Ebene ausgeführt wird und die interne Benutzeroberflächenebene auf vollständige Benutzeroberfläche oder eingeschränkte Benutzeroberfläche festgelegt ist.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: AdminUISequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12feb7080d6d97ee86456bee694cdad57eee9873c9c7f64aecf0f4bd05817cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381698"
---
# <a name="adminuisequence-table"></a>AdminUISequence-Tabelle

In der Tabelle AdminUISequence werden Aktionen aufgeführt, die [](admin-action.md) das Installationsprogramm nacheinander aufruft, wenn die ADMIN-Aktion der obersten Ebene ausgeführt wird und die interne Benutzeroberflächenebene auf vollständige Benutzeroberfläche oder eingeschränkte Benutzeroberfläche festgelegt ist. Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächenebene auf einfache Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist. Weitere [Informationen finden Sie Benutzeroberfläche](about-the-user-interface.md).

ADMIN-Aktionen in der Installationssequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und alle Beendigungsdialogfelder befinden sich in der Tabelle AdminUISequence. Alle Aktionen von InstallValidate bis zum Ende der Installationssequenz befinden sich in der [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md). Da die AdminExecuteSequence-Tabelle allein stehen muss, enthält sie auch alle erforderlichen Initialisierungsaktionen wie [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)und [CostFinalize.](costfinalize-action.md) Sie verfügt auch über die [ExecuteAction-Aktion](executeaction-action.md).

Die Spalten sind mit denen der [InstallUISequence-Tabelle identisch.](installuisequence-table.md) Die Tabelle AdminUISequence enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Identifier](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Name der auszuführenden Aktion. Dies ist entweder eine Standardaktion, ein Benutzeroberflächen-Assistent oder eine benutzerdefinierte Aktion, die in der [CustomAction-Tabelle aufgeführt ist.](customaction-table.md)

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Logischer Ausdruck. Wenn der Ausdruck zu FALSE ausgewertet wird, wird die Aktion übersprungen. Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesBadActionData zurück. Informationen zur Syntax von bedingten Anweisungen finden Sie unter [Syntax für bedingte Anweisungen.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Ein positiver Wert gibt die Sequenzposition der Aktion an. Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das Beendigungsflag zurückgibt. Jedes Beendigungsflag (negativer Wert) kann mit nicht mehr als einer Aktion verwendet werden. Mehrere Aktionen können Beendigungsflags haben, müssen jedoch unterschiedliche Flags sein. Beendigungsflags (negative Werte) werden in der Regel mit [Dialogfeldern verwendet.](dialog-boxes.md)



| Beendigungsflag          | Wert | BESCHREIBUNG                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | –1    | Erfolgreicher Abschluss. Wird mit [Exitdialogfeldern](exit-dialog.md) verwendet.               |
| msiDoActionStatusUserExit | –2    | Der Benutzer beendet die Installation. Wird mit [UserExit-Dialogfeldern](userexit-dialog.md) verwendet.     |
| msiDoActionStatusFailure  | -3    | Schwerwiegendes Beenden wird beendet. Wird mit einem [FatalError-Dialogfeld](fatalerror-dialog.md) verwendet. |
| msiDoActionStatusSuspend  | –4    | Die Installation wurde angehalten.                                                                |



 

Null, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie aufgerufen wird.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE75](ice75.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICE96](ice96.md)  
[ICEM04](icem04.md)  
</dl>

 

 



