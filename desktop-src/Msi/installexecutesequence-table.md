---
description: Die Tabelle InstallExecuteSequence listet Aktionen auf, die ausgeführt werden, wenn die Installations Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: InstallExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862343"
---
# <a name="installexecutesequence-table"></a>InstallExecuteSequence-Tabelle

Die Tabelle InstallExecuteSequence listet Aktionen auf, die ausgeführt werden, wenn die [Installations Aktion](install-action.md) der obersten Ebene ausgeführt wird.

Aktionen in der Installations Sequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und alle Beendigungs Dialogfelder befinden sich in der [Tabelle InstallUISequence](installuisequence-table.md). Alle Aktionen von InstallValidate bis zum Ende der Installations Sequenz befinden sich in der InstallExecuteSequence-Tabelle. Da die InstallExecuteSequence-Tabelle eigenständig sein muss, sind alle erforderlichen Initialisierungs Aktionen wie z. b. die [LaunchConditions](launchconditions-action.md)-, [costinitialize](costinitialize-action.md)-, [filecost](filecost-action.md)-und [costfinalize](costfinalize-action.md) -Aktionen erforderlich.

[Benutzerdefinierte Aktionen](custom-actions.md) , für die eine Benutzeroberfläche erforderlich ist, sollten [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anstelle von erstellten Dialogfeldern verwenden, die mithilfe der [Dialogfeld Tabelle](dialog-table.md)erstellt wurden

Die InstallExecuteSequence-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Bezeichner](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Der Name der auszuführenden Aktion. Dabei handelt es sich entweder um eine integrierte Aktion oder um eine benutzerdefinierte Aktion.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Dieses Feld enthält einen bedingten Ausdruck. Wenn der Ausdruck zu false ausgewertet wird, wird die Aktion übersprungen. Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesbadaktiondata zurück. Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Zahl, die die Sequenz Position bestimmt, in der diese Aktion ausgeführt werden soll.

Ein positiver Wert stellt die Sequenz Position dar. Ein NULL-Wert gibt an, dass die Aktion nicht ausgeführt wird. Die folgenden negativen Werte geben an, dass diese Aktion ausgeführt werden soll, wenn das Installationsprogramm das zugehörige Beendigungs Flag zurückgibt. Jedes terminierungsflag (negativer Wert) kann mit nur einer Aktion verwendet werden. Mehrere Aktionen können über Beendigungs Flags verfügen, müssen jedoch unterschiedliche Flags aufweisen. Beendigungs Flags (negative Werte) werden in der Regel in [Dialog Feldern](dialog-boxes.md)verwendet.



| Beendigungs Flag          | Wert | BESCHREIBUNG                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msidoaktionstatus-Erfolg  | -1    | Erfolgreicher Abschluss. Wird mit den Dialogfeldern " [Beenden](exit-dialog.md) " verwendet.               |
| msidoaktionstatus ususerexit | -2    | Der Benutzer beendet die Installation. Wird mit [Userexit](userexit-dialog.md) -Dialogfeldern verwendet.     |
| msidoaktionstatus-Fehler  | -3    | Schwerwiegender Exit wird beendet. Wird mit den Dialogfeldern " [FatalError](fatalerror-dialog.md) " verwendet. |
| msidoaktionstatus-Suspend  | –4    | Die Installation wurde angehalten.                                                                |



 

NULL, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie ausgeführt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der lokalisierte Text für die Fortschrittsanzeige oder die Protokollierung wird in der [Tabelle "aktiontext](actiontext-table.md)" angegeben.

Ein Beispiel für eine Sequenz Tabelle finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
</dl>

 

 



