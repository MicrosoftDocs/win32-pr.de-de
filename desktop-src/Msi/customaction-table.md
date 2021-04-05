---
description: Die Tabelle CustomAction bietet die Möglichkeit, benutzerdefinierten Code und Daten in die Installation zu integrieren. Die Quelle des ausgeführten Codes kann ein in der Datenbank enthaltener Stream, eine zuletzt installierte Datei oder eine vorhandene ausführbare Datei sein.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabelle "CustomAction"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752321"
---
# <a name="customaction-table"></a>Tabelle "CustomAction"

Die Tabelle CustomAction bietet die Möglichkeit, benutzerdefinierten Code und Daten in die Installation zu integrieren. Die Quelle des ausgeführten Codes kann ein in der Datenbank enthaltener Stream, eine zuletzt installierte Datei oder eine vorhandene ausführbare Datei sein.

Die CustomAction-Tabelle weist die folgenden Spalten auf.



| Spalte       | Typ                               | Schlüssel | Nullwerte zulässig |
|--------------|------------------------------------|-----|----------|
| Aktion       | [Bezeichner](identifier.md)       | J   | N        |
| type         | [Integer](integer.md)             | N   | N        |
| `Source`       | [CustomSource](customsource.md)   | N   | J        |
| Ziel       | [Großformatige](formatted.md)         | N   | J        |
| ExtendedType | [Doubleiteger](doubleinteger.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Name der Aktion. Die Aktion wird normalerweise in einer Sequenz Tabelle angezeigt, sofern Sie nicht von einer anderen benutzerdefinierten Aktion aufgerufen wird. Wenn der Name mit einer integrierten Aktion übereinstimmt, wird die benutzerdefinierte Aktion nie aufgerufen.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Ein Feld mit Flagbits, das den Basistyp der benutzerdefinierten Aktion und Optionen angibt. Eine Liste der grundlegenden Typen finden Sie [in der Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) . Weitere Informationen finden Sie unter [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md), Optionen für die [Ausführung von benutzerdefinierten](custom-action-execution-scheduling-options.md)Aktionen, ausgeblendete [Ziel](custom-action-hidden-target-option.md)Optionen und [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md)

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Ausgangs
</dt> <dd>

Ein Eigenschaftsname oder ein externer Schlüssel in einer anderen Tabelle. Eine Erläuterung der möglichen benutzerdefinierten Aktions Quellen finden Sie unter [benutzerdefinierte Aktions Quellen](custom-action-sources.md) und [in der Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md). Die Quell Spalte kann z. b. einen externen Schlüssel in die erste Spalte einer der folgenden Tabellen enthalten, die die Quelle des benutzerdefinierten Aktionscodes enthält.

[Verzeichnis Tabelle](directory-table.md) zum Aufrufen vorhandener ausführbarer Dateien.

[Dateitabelle](file-table.md) zum Aufrufen von ausführbaren Dateien und DLLs, die soeben installiert wurden.

[Binäre Tabelle](binary-table.md) zum Aufrufen von ausführbaren Dateien, DLLs und Daten, die in der Datenbank gespeichert sind.

[Eigenschaften Tabelle](property-table.md) zum Aufrufen von ausführbaren Dateien, deren Pfade von einer Eigenschaft aufbewahrt werden.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar
</dt> <dd>

Ein Ausführungs Parameter, der vom Basistyp der benutzerdefinierten Aktion abhängig ist. In der [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) finden Sie eine Beschreibung der Informationen, die in diesem Feld für die einzelnen Typen von benutzerdefinierten Aktionen eingegeben werden müssen. Beispielsweise kann dieses Feld abhängig von der benutzerdefinierten Aktion Folgendes enthalten.



| Ziel                                    | Benutzerdefinierte Aktion                         |
|-------------------------------------------|---------------------------------------|
| Einstiegspunkt (erforderlich)                    | Aufrufen einer DLL.                        |
| Name der ausführbaren Datei mit Argumenten (erforderlich) | Aufrufen einer vorhandenen ausführbaren Datei.       |
| Befehlszeilenargumente (optional)         | Aufrufen einer soeben installierten ausführbaren Datei. |
| Ziel Dateiname (erforderlich)               | Erstellen einer Datei aus benutzerdefinierten Daten.     |
| Null                                      | Ausführen von Skriptcode.                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

Geben Sie in diesem Feld den **msidbcustomaction typepatchuninstall** -Wert ein, um eine benutzerdefinierte Aktion mit der [Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md)anzugeben.

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. Diese Option ist ab Windows Installer 4,5 verfügbar.

</dd> </dl>

Weitere Informationen finden Sie in den Themen unter [benutzerdefinierte Aktionen](custom-actions.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE68](ice68.md)  
[ICE72](ice72.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE80](ice80.md)  
[ICE88](ice88.md)  
[ICE93](ice93.md)  
</dl>

 

 



