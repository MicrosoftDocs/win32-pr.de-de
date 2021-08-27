---
description: Die Tabelle AdminExecuteSequence listet Aktionen auf, die das Installationsprogramm nacheinander aufruft, wenn die ADMIN-Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: AdminExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eed182f5a27b357ecd546003cbfd7c68728d41c4018442b23bbf834ac8a796a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046000"
---
# <a name="adminexecutesequence-table"></a>AdminExecuteSequence-Tabelle

Die Tabelle AdminExecuteSequence listet Aktionen auf, die das Installationsprogramm nacheinander aufruft, wenn die [ADMIN-Aktion](admin-action.md) der obersten Ebene ausgeführt wird.

ADMIN-Aktionen in der Installationssequenz bis zur [InstallValidate-Aktion](installvalidate-action.md) und allen Exitdialogfeldern befinden sich in der [Tabelle AdminUISequence.](adminuisequence-table.md)

ADMIN-Aktionen von der InstallValidate-Aktion bis zum Ende der Installationssequenz befinden sich in der Tabelle AdminExecuteSequence. Da die Tabelle AdminExecuteSequence eigenständig sein muss, enthält sie auch alle erforderlichen Initialisierungsaktionen wie [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)und [CostFinalize.](costfinalize-action.md)

[Benutzerdefinierte Aktionen,](custom-actions.md) die eine Benutzeroberfläche erfordern, sollten [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anstelle von erstellten Dialogfeldern verwenden, die mit der [Dialogtabelle](dialog-table.md)erstellt wurden.

Die Spalten sind mit denen der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)identisch. Die Tabelle AdminExecuteSequence enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Identifier](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Name der auszuführende Aktion. Dies ist entweder eine Standardaktion oder eine benutzerdefinierte Aktion, die in der [Tabelle CustomAction](customaction-table.md)aufgeführt ist.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Logischer Ausdruck. Wenn der Ausdruck als FALSE ausgewertet wird, wird die Aktion übersprungen. Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesBadActionData zurück. Informationen zur Syntax von bedingten Anweisungen finden Sie unter [Conditional Statement Syntax](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Ein positiver Wert gibt die Sequenzposition der Aktion an. Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das Beendigungsflag zurückgibt. Jedes Beendigungsflag (negativer Wert) kann mit nicht mehr als einer Aktion verwendet werden. Mehrere Aktionen können Beendigungsflags aufweisen, müssen jedoch unterschiedliche Flags sein. Beendigungsflags (negative Werte) werden in der Regel mit [Dialogfeldern](dialog-boxes.md)verwendet.



| Beendigungsflag          | Wert | BESCHREIBUNG                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | –1    | Erfolgreicher Abschluss. Wird mit den Dialogfeldern [Beenden](exit-dialog.md) verwendet.               |
| msiDoActionStatusUserExit | –2    | Der Benutzer beendet die Installation. Wird mit [UserExit-Dialogfeldern](userexit-dialog.md) verwendet.     |
| msiDoActionStatusFailure  | -3    | Schwerwiegender Exit wird beendet. Wird mit einem [FatalError-Dialogfeld](fatalerror-dialog.md) verwendet. |
| msiDoActionStatusSuspend  | –4    | Installation wird angehalten.                                                                |



 

Null, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie aufgerufen wird.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



