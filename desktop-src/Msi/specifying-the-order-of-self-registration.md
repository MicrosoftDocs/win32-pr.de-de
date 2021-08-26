---
description: Beachten Sie, dass Sie mithilfe der Aktionen SelfRegModules und SelfUnRegModules nicht die Reihenfolge angeben können, in der sich das Installationsprogramm selbst registrierende DLLs registriert oder die Registrierung aufheben kann.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Angeben der Reihenfolge der Selbstregistrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb26fbebad3167fbea95679a1ea7a29c28946ae6fa2dd2b014be6ade986e28f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039680"
---
# <a name="specifying-the-order-of-self-registration"></a>Angeben der Reihenfolge der Selbstregistrierung

Beachten Sie, dass Sie mithilfe der Aktionen [SelfRegModules](selfregmodules-action.md) und [SelfUnRegModules](selfunregmodules-action.md) nicht die Reihenfolge angeben können, in der sich das Installationsprogramm selbst registrierende DLLs registriert oder die Registrierung aufheben kann. Diese Aktionen registrieren alle Module, die in der [SelfReg-Tabelle](selfreg-table.md)aufgeführt sind. Das Installationsprogramm registriert .exe Dateien nicht selbst.

Um die Reihenfolge anzugeben, in der das Installationsprogramm Module registriert oder deren Registrierung aufgehoben wird, müssen Sie zwei [benutzerdefinierte Aktionen](custom-actions.md) für jedes Modul verwenden. Eine benutzerdefinierte Aktion für DllRegisterServer und eine zweite für DllUnregisterServer. Diese benutzerdefinierten Aktionen müssen dann in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) an dem Punkt in der Sequenz erstellt werden, an dem die DLL registriert oder nicht registriert werden soll.

Im folgenden Beispiel wird veranschaulicht, wie die Datenbank erstellt wird, um die Selbstregistrierung einer DLL an einem bestimmten Punkt in der Aktionssequenz zu planen.

[Dateitabelle](file-table.md) (partiell)



| Datei  | Komponente\_ | FileName  | Sequenz |
|-------|-------------|-----------|----------|
| mydll | myComponent | Mydll.dll | 13       |



 

[Komponententabelle](component-table.md) (teilweise)



| Komponente   | Componentid | Verzeichnis\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*eine GUID*}  | Myfolder    | mydll   |



 

[Verzeichnistabelle](directory-table.md)



| Verzeichnis | \_Übergeordnetes Verzeichnis | DefaultDir          |
|-----------|-------------------|---------------------|
| Targetdir |                   | SourceDir           |
| Myfolder  | Targetdir         | myFolder \| My Folder |



 

[CustomAction-Tabelle](customaction-table.md)



| Aktion     | type | `Source`   | Ziel                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | Myfolder | " \[ SystemFolder \] msiexec" /y " \[ \# mydll \] " |
| mydllUNREG | 3170 | Myfolder | " \[ SystemFolder \] msiexec" /z " \[ \# mydll \] " |



 

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion           | Bedingung         | Sequenz |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent=2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



