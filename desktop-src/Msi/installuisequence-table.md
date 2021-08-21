---
description: In der Tabelle InstallUISequence werden Aktionen aufgeführt, die ausgeführt werden, wenn die INSTALL-Aktion der obersten Ebene ausgeführt wird und die interne Benutzeroberflächenebene auf vollständige benutzeroberfläche oder reduzierte Benutzeroberfläche festgelegt ist.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: InstallUISequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2234ddcad587a495eceb79cc4511100f483bcfd96b388164f6e3c2d6a39eca3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013248"
---
# <a name="installuisequence-table"></a>InstallUISequence-Tabelle

In der Tabelle InstallUISequence werden Aktionen aufgeführt, die ausgeführt werden, wenn die [INSTALL-Aktion](install-action.md) der obersten Ebene ausgeführt wird und die interne Benutzeroberflächenebene auf vollständige Benutzeroberfläche oder eingeschränkte Benutzeroberfläche festgelegt ist. Das Installationsprogramm überspringt die Aktionen in dieser Tabelle, wenn die Benutzeroberflächenebene auf einfache Benutzeroberfläche oder keine Benutzeroberfläche festgelegt ist. Weitere [Informationen finden Sie Benutzeroberfläche](about-the-user-interface.md).

Aktionen in der Installationssequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und den Exitdialogfeldern befinden sich in der Tabelle InstallUISequence. Alle Aktionen von InstallValidate bis zum Ende der Installationssequenz befinden sich in der [Tabelle InstallExecuteSequence.](installexecutesequence-table.md) Da die Tabelle InstallExecuteSequence allein stehen muss, verfügt sie über alle erforderlichen Initialisierungsaktionen wie [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)und die [Aktion CostFinalize](costfinalize-action.md)und [ExecuteAction.](executeaction-action.md)

Die Tabelle InstallUISequence enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Identifier](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Name der auszuführenden Aktion. Dies ist entweder eine integrierte Aktion, eine benutzerdefinierte Aktion oder ein Benutzeroberflächen-Assistent.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Dieses Feld enthält einen bedingten Ausdruck. Wenn der Ausdruck falseausgewertet wird, wird die Aktion übersprungen. Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesBadActionData zurück. Informationen zur Syntax von bedingten Anweisungen finden Sie unter [Syntax für bedingte Anweisungen.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Nummer in dieser Spalte bestimmt die Sequenzposition, an der diese Aktion ausgeführt wird.

Ein positiver Wert stellt die Sequenzposition dar. Ein NULL-Wert gibt an, dass die Aktion nie ausgeführt wird. Die folgenden negativen Werte geben an, dass diese Aktion ausgeführt wird, wenn das Installationsprogramm das zugeordnete Beendigungsflag zurückgibt. Jedes Beendigungsflag (negativer Wert) kann mit nicht mehr als einer Aktion verwendet werden. Mehrere Aktionen können Beendigungsflags haben, müssen jedoch unterschiedliche Flags sein. Beendigungsflags (negative Werte) werden in der Regel mit [Dialogfeldern verwendet.](dialog-boxes.md)



| Beendigungsflag          | Wert | BESCHREIBUNG                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | –1    | Erfolgreicher Abschluss. Wird mit [Exitdialogfeldern](exit-dialog.md) verwendet.               |
| msiDoActionStatusUserExit | –2    | Der Benutzer beendet die Installation. Wird mit [UserExit-Dialogfeldern](userexit-dialog.md) verwendet.     |
| msiDoActionStatusFailure  | -3    | Schwerwiegendes Beenden wird beendet. Wird mit einem [FatalError-Dialogfeld](fatalerror-dialog.md) verwendet. |
| msiDoActionStatusSuspend  | –4    | Die Installation wurde angehalten.                                                                |



 

Null, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie ausgeführt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Zugeordneter lokalisierter Text für die Statusanzeige oder -protokollierung wird in der [ActionText-Tabelle angegeben.](actiontext-table.md)

Ein Beispiel für eine Sequenztabelle finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

## <a name="validation"></a>Überprüfung

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
[ICE86](ice86.md)  
</dl>

 

 



