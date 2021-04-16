---
description: Beachten Sie, dass Sie nicht die Reihenfolge angeben können, in der der Installer mithilfe der SelfRegModules-und selfunregmodules-Aktionen selbst registrierte DLLs registriert bzw. die Registrierung aufheben kann.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Angeben der Reihenfolge der Selbstregistrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485379"
---
# <a name="specifying-the-order-of-self-registration"></a>Angeben der Reihenfolge der Selbstregistrierung

Beachten Sie, dass Sie nicht die Reihenfolge angeben können, in der der Installer mithilfe der [SelfRegModules](selfregmodules-action.md) -und [selfunregmodules](selfunregmodules-action.md) -Aktionen selbst registrierte DLLs registriert bzw. die Registrierung aufheben kann. Diese Aktionen registrieren alle in der [Tabelle selfreg](selfreg-table.md)aufgeführten Module. Der Installer führt keine Selbstregistrierung von exe-Dateien durch.

Um die Reihenfolge anzugeben, in der das Installationsprogramm Module registriert oder die Registrierung der Module aufgehoben wird, müssen Sie für jedes Modul zwei [benutzerdefinierte Aktionen](custom-actions.md) verwenden. Eine benutzerdefinierte Aktion für "DllRegisterServer" und eine zweite für "DllUnregisterServer". Diese benutzerdefinierten Aktionen müssen dann in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) an dem Punkt in der Sequenz erstellt werden, wo die dll registriert oder die Registrierung aufgehoben werden soll.

Im folgenden Beispiel wird veranschaulicht, wie die-Datenbank erstellt wird, um die Selbstregistrierung einer DLL an einem bestimmten Punkt in der Aktions Sequenz zu planen.

[Dateitabelle](file-table.md) (partiell)



| File  | Komponente\_ | FileName  | Sequenz |
|-------|-------------|-----------|----------|
| Datei "mydll | MyComponent | Mydll.dll | 13       |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente   | ComponentID | Verzeichnis\_ | KEYPATH |
|-------------|-------------|-------------|---------|
| MyComponent | {*GUID*}  | myFolder    | Datei "mydll   |



 

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis | Über \_ geordnetes Verzeichnis | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| myFolder  | TARGETDIR         | Ordner "MyFolder" \| |



 

[Tabelle "CustomAction"](customaction-table.md)



| Aktion     | type | `Source`   | Ziel                                     |
|------------|------|----------|--------------------------------------------|
| mydllreg   | 3170 | myFolder | " \[ System Folder \] msiexec"/y " \[ \# Datei" myDll \] " |
| mydllunreg | 3170 | myFolder | " \[ System Folder \] msiexec" "/z" \[ \# Datei "myDll \] " |



 

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion           | Bedingung         | Sequenz |
|------------------|-------------------|----------|
| Selfunregmodules |                   | 2200     |
| mydllunreg       | $MyComponent = 2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllreg         | $MyComponent>2 | 6501     |



 

 

 



