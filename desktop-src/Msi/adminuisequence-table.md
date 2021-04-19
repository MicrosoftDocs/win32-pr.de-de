---
description: In der Tabelle AdminUISequence sind Aktionen aufgeführt, die vom Installationsprogramm nacheinander aufgerufen werden, wenn die Administrator Aktion der obersten Ebene ausgeführt wird und die interne Benutzeroberflächen Ebene auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: AdminUISequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356115"
---
# <a name="adminuisequence-table"></a>AdminUISequence-Tabelle

In der Tabelle AdminUISequence sind Aktionen aufgeführt, die vom Installationsprogramm nacheinander aufgerufen werden, wenn die [Administrator Aktion](admin-action.md) der obersten Ebene ausgeführt wird und die interne Benutzeroberflächen Ebene auf vollständige Benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist. Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächen Ebene auf grundlegende Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist. Weitere [Informationen finden Sie unter Informationen zur Benutzeroberfläche](about-the-user-interface.md).

Administrator Aktionen in der Installations Sequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und alle Beendigungs Dialogfelder befinden sich in der Tabelle AdminUISequence. Alle Aktionen von InstallValidate bis zum Ende der Installations Sequenz befinden sich in der [Tabelle "AdminExecuteSequence](adminexecutesequence-table.md)". Da die AdminExecuteSequence-Tabelle eigenständig sein muss, enthält Sie auch alle notwendigen Initialisierungs Aktionen wie [LaunchConditions](launchconditions-action.md), [costinitialize](costinitialize-action.md), [filecost](filecost-action.md)und [costfinalize](costfinalize-action.md). Es verfügt auch über die [ExecuteAction-Aktion](executeaction-action.md).

Die Spalten sind identisch mit denen der [Tabelle InstallUISequence](installuisequence-table.md). Die AdminUISequence-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Bezeichner](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Der Name der auszuführenden Aktion. Dabei handelt es sich entweder um eine Standardaktion, einen Assistenten für die Benutzeroberfläche oder um eine benutzerdefinierte Aktion, die in der [Tabelle CustomAction](customaction-table.md)aufgeführt ist.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Logischer Ausdruck. Wenn der Ausdruck zu false ausgewertet wird, wird die Aktion übersprungen. Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesbadaktiondata zurück. Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Ein positiver Wert gibt die Sequenz Position der Aktion an. Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das terminierungsflag zurückgibt. Jedes terminierungsflag (negativer Wert) kann mit nur einer Aktion verwendet werden. Mehrere Aktionen können über Beendigungs Flags verfügen, müssen jedoch unterschiedliche Flags aufweisen. Beendigungs Flags (negative Werte) werden in der Regel in [Dialog Feldern](dialog-boxes.md)verwendet.



| Beendigungs Flag          | Wert | BESCHREIBUNG                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msidoaktionstatus-Erfolg  | -1    | Erfolgreicher Abschluss. Wird mit den Dialogfeldern " [Beenden](exit-dialog.md) " verwendet.               |
| msidoaktionstatus ususerexit | -2    | Der Benutzer beendet die Installation. Wird mit [Userexit](userexit-dialog.md) -Dialogfeldern verwendet.     |
| msidoaktionstatus-Fehler  | -3    | Schwerwiegender Exit wird beendet. Wird mit den Dialogfeldern " [FatalError](fatalerror-dialog.md) " verwendet. |
| msidoaktionstatus-Suspend  | –4    | Die Installation wurde angehalten.                                                                |



 

NULL, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie aufgerufen wird.

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

 

 



