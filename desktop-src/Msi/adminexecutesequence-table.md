---
description: Die Tabelle AdminExecuteSequence listet Aktionen auf, die der Installer nacheinander aufruft, wenn die Administrator Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: AdminExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357524"
---
# <a name="adminexecutesequence-table"></a>AdminExecuteSequence-Tabelle

Die Tabelle AdminExecuteSequence listet Aktionen auf, die der Installer nacheinander aufruft, wenn die [Administrator Aktion](admin-action.md) der obersten Ebene ausgeführt wird.

Administrator Aktionen in der Installations Sequenz, bis zur [InstallValidate-Aktion](installvalidate-action.md) und zu beliebigen Beendigungs Dialogfeldern, befinden sich in der [Tabelle AdminUISequence](adminuisequence-table.md).

Administrator Aktionen aus der InstallValidate-Aktion bis zum Ende der Installations Sequenz befinden sich in der AdminExecuteSequence-Tabelle. Da die AdminExecuteSequence-Tabelle eigenständig sein muss, enthält Sie auch alle notwendigen Initialisierungs Aktionen wie [LaunchConditions](launchconditions-action.md), [costinitialize](costinitialize-action.md), [filecost](filecost-action.md)und [costfinalize](costfinalize-action.md).

[Benutzerdefinierte Aktionen](custom-actions.md) , für die eine Benutzeroberfläche erforderlich ist, sollten [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anstelle von erstellten Dialogfeldern verwenden, die mithilfe der [Dialogfeld Tabelle](dialog-table.md)erstellt wurden

Die Spalten sind identisch mit denen der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md). Die AdminExecuteSequence-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Bezeichner](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Der Name der auszuführenden Aktion. Dabei handelt es sich entweder um eine Standardaktion oder eine benutzerdefinierte Aktion, die in der [Tabelle CustomAction](customaction-table.md)aufgeführt ist.

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

 

 



