---
description: Die Tabelle AdvtExecuteSequence listet Aktionen auf, die das Installationsprogramm aufruft, wenn die AKTION "ADVERTISE" der obersten Ebene ausgeführt wird.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabelle "AdvtExecuteSequence"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed9a566b721be1065e825cbf7cd6650a52c83ace653dc2730f1fcf7785d125c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381589"
---
# <a name="advtexecutesequence-table"></a>Tabelle "AdvtExecuteSequence"

Die Tabelle AdvtExecuteSequence listet Aktionen auf, die das Installationsprogramm aufruft, wenn die [AKTION "ADVERTISE"](advertise-action.md) der obersten Ebene ausgeführt wird.

In der Tabelle AdvtExecuteSequence können nur die folgenden Aktionen verwendet werden. Benutzerdefinierte Aktionen können in dieser Tabelle nicht verwendet werden.

[CostFinalize](costfinalize-action.md)

[CostInitialize](costinitialize-action.md)

[CreateShortcuts](createshortcuts-action.md)

[InstallFinalize](installfinalize-action.md)

[InstallInitialize](installinitialize-action.md)

[InstallValidate](installvalidate-action.md)

[MsiPublishAssemblies](msipublishassemblies-action.md)

[PublishComponents](publishcomponents-action.md)

[PublishFeatures](publishfeatures-action.md)

[PublishProduct](publishproduct-action.md)

[RegisterClassInfo](registerclassinfo-action.md)

[RegisterExtensionInfo](registerextensioninfo-action.md)

[RegisterMIMEInfo](registermimeinfo-action.md)

[RegisterProgIdInfo](registerprogidinfo-action.md)

Die Spalten sind mit denen der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)identisch. Die Tabelle AdvtExecuteSequence weist die folgenden Spalten auf.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Aktion    | [Identifier](identifier.md) | J   | N        |
| Bedingung | [Condition](condition.md)   | N   | J        |
| Sequenz  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Name der [Standardaktion,](standard-actions.md) die das Installationsprogramm ausführen soll. Dies ist der Primärschlüssel der Tabelle.

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

 

 



