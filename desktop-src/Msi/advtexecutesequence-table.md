---
description: Die AdvtExecuteSequence-Tabelle listet Aktionen auf, die das Installationsprogramm aufruft, wenn die Ankündigungs Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: AdvtExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864504"
---
# <a name="advtexecutesequence-table"></a>AdvtExecuteSequence-Tabelle

Die AdvtExecuteSequence-Tabelle listet Aktionen auf, die das Installationsprogramm aufruft, wenn die Ankündigungs [Aktion](advertise-action.md) der obersten Ebene ausgeführt wird.

In der AdvtExecuteSequence-Tabelle können nur die folgenden Aktionen verwendet werden. Benutzerdefinierte Aktionen können in dieser Tabelle nicht verwendet werden.

[Costfinalize](costfinalize-action.md)

[Costinitialize](costinitialize-action.md)

["Kreateshortcuts"](createshortcuts-action.md)

[InstallFinalize wurde](installfinalize-action.md)

[Installinitialisieren](installinitialize-action.md)

[InstallValidate](installvalidate-action.md)

[Msipublishassemblys](msipublishassemblies-action.md)

[PublishComponents](publishcomponents-action.md)

[Publishfeatures](publishfeatures-action.md)

[Publishproduct](publishproduct-action.md)

[RegisterClassInfo](registerclassinfo-action.md)

[RegisterExtensionInfo](registerextensioninfo-action.md)

[Registermimeinfo](registermimeinfo-action.md)

[Registerprogidinfo](registerprogidinfo-action.md)

Die Spalten sind identisch mit denen der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md). Die AdvtExecuteSequence-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Bezeichner](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Der Name der [Standardaktion](standard-actions.md) , die vom Installationsprogramm ausgeführt werden soll. Dies ist der Primärschlüssel der Tabelle.

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
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE72](ice72.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



