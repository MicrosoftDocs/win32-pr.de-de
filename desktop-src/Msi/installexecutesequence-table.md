---
description: In der Tabelle InstallExecuteSequence werden Aktionen aufgeführt, die ausgeführt werden, wenn die INSTALL-Aktion der obersten Ebene ausgeführt wird.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: InstallExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d48fb83bd8f3c947feb81ab95df490572ba1ee68d423957759a95c323005070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142165"
---
# <a name="installexecutesequence-table"></a>InstallExecuteSequence-Tabelle

In der Tabelle InstallExecuteSequence werden Aktionen aufgeführt, die ausgeführt werden, wenn die [INSTALL-Aktion der obersten](install-action.md) Ebene ausgeführt wird.

Aktionen in der Installationssequenz bis zur [InstallValidate-Aktion](installvalidate-action.md)und alle Beendigungsdialogfelder befinden sich in der [InstallUISequence-Tabelle](installuisequence-table.md). Alle Aktionen von InstallValidate bis zum Ende der Installationssequenz befinden sich in der Tabelle InstallExecuteSequence. Da die Tabelle InstallExecuteSequence allein stehen muss, verfügt sie über alle erforderlichen Initialisierungsaktionen, z. B. die [Aktionen LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)und [CostFinalize.](costfinalize-action.md)

[Benutzerdefinierte Aktionen,](custom-actions.md) die eine Benutzeroberfläche erfordern, sollten [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anstelle von erstellten Dialogfeldern verwenden, die mithilfe der [Dialogtabelle erstellt wurden.](dialog-table.md)

Die Tabelle InstallExecuteSequence enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Identifier](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Name der auszuführenden Aktion. Dies ist entweder eine integrierte Aktion oder eine benutzerdefinierte Aktion.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Dieses Feld enthält einen bedingten Ausdruck. Wenn der Ausdruck falseausgewertet wird, wird die Aktion übersprungen. Wenn die Ausdruckssyntax ungültig ist, wird die Sequenz beendet und gibt iesBadActionData zurück. Informationen zur Syntax von bedingten Anweisungen finden Sie unter [Syntax für bedingte Anweisungen.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Zahl, die die Sequenzposition bestimmt, an der diese Aktion ausgeführt werden soll.

Ein positiver Wert stellt die Sequenzposition dar. Ein NULL-Wert gibt an, dass die Aktion nicht ausgeführt wird. Die folgenden negativen Werte geben an, dass diese Aktion ausgeführt werden soll, wenn das Installationsprogramm das zugeordnete Beendigungsflag zurückgibt. Jedes Beendigungsflag (negativer Wert) kann mit nicht mehr als einer Aktion verwendet werden. Mehrere Aktionen können Beendigungsflags haben, müssen jedoch unterschiedliche Flags sein. Beendigungsflags (negative Werte) werden in der Regel mit [Dialogfeldern verwendet.](dialog-boxes.md)



| Beendigungsflag          | Wert | Beschreibung                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | –1    | Erfolgreicher Abschluss. Wird mit [Exitdialogfeldern](exit-dialog.md) verwendet.               |
| msiDoActionStatusUserExit | –2    | Der Benutzer beendet die Installation. Wird mit [UserExit-Dialogfeldern](userexit-dialog.md) verwendet.     |
| msiDoActionStatusFailure  | -3    | Schwerwiegendes Beenden wird beendet. Wird mit einem [FatalError-Dialogfeld](fatalerror-dialog.md) verwendet. |
| msiDoActionStatusSuspend  | –4    | Die Installation wurde angehalten.                                                                |



 

Null, alle anderen negativen Zahlen oder ein NULL-Wert geben an, dass die Aktion nie ausgeführt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Lokalisierter Text für die Statusanzeige oder -protokollierung wird in der [ActionText-Tabelle angegeben.](actiontext-table.md)

Ein Beispiel für eine Sequenztabelle finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

## <a name="validation"></a>Überprüfung

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

 

 



