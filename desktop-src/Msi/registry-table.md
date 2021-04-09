---
description: Die Registrierungs Tabelle enthält die Registrierungsinformationen, die von der Anwendung in der Systemregistrierung festgelegt werden müssen.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Registrierungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959656"
---
# <a name="registry-table"></a>Registrierungs Tabelle

Die Registrierungs Tabelle enthält die Registrierungsinformationen, die von der Anwendung in der Systemregistrierung festgelegt werden müssen.

Die Registrierungs Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Registrierung    | [Bezeichner](identifier.md) | J   | N        |
| Root        | [Integer](integer.md)       | N   | N        |
| Schlüssel         | [Regfad](regpath.md)       | N   | N        |
| Name        | [Großformatige](formatted.md)   | N   | J        |
| Wert       | [Großformatige](formatted.md)   | N   | J        |
| Komponente\_ | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registrierungs
</dt> <dd>

Der Primärschlüssel, der zum Identifizieren eines Registrierungsdaten Satzes verwendet wird.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Fasst
</dt> <dd>

Der vordefinierte Stamm Schlüssel für den Registrierungs Wert. Geben Sie in diesem Feld den Wert-1 ein, um den Stamm Schlüssel vom Installationstyp abhängig zu machen. Geben Sie einen der anderen Werte in der folgenden Tabelle ein, um zu erzwingen, dass der Registrierungs Wert unter einem bestimmten Stamm Schlüssel geschrieben wird.



| Konstante                          | Hexadezimal | Decimal | Stamm Schlüssel                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                            | \- 0x001    | -1      | Wenn es sich um eine benutzerspezifische Installation handelt, wird der Registrierungs Wert unter **HKEY \_ Current \_ User** geschrieben. Wenn es sich um eine Computer spezifische Installation handelt, wird der Registrierungs Wert unter **HKEY \_ local \_ Machine** geschrieben. Beachten Sie, dass eine Computer spezifische Installation durch Festlegen der [**ALLUSERS**](allusers.md) -Eigenschaft auf 1 angegeben wird.<br/>                |
| **msidbregistryrootclassesroot**  | 0x000       | 0       | **HKEY \_ Klassen \_** Stamm: das Installationsprogramm schreibt oder entfernt den Wert aus der **HKCU- \\ Software \\ Klassen** Hive während der Installation im [Installations Kontext](installation-context.md)pro Benutzer.<br/> Der Installer schreibt oder entfernt den Wert aus der **HKLM- \\ Software \\ Klassen** Struktur während der Installation pro Computer.<br/> |
| **msidbregistryrootcurrentuser**  | 0x001       | 1       | **Aktueller HKEY- \_ \_ Benutzer**                                                                                                                                                                                                                                                                                                                      |
| **msidbregistryrootlocalmachine** | 0x002       | 2       | **lokaler HKEY- \_ \_ Computer**                                                                                                                                                                                                                                                                                                                     |
| **msidbregistryrootusers**        | 0x003       | 3       | **HKEY- \_ Benutzer**                                                                                                                                                                                                                                                                                                                              |



 

Beachten Sie, dass in der **HKCU** -Hive geschriebene Registrierungseinträge auf eine Komponente verweisen, in der das registrykeypath-Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist. Dadurch wird sichergestellt, dass das Installationsprogramm die erforderlichen Registrierungseinträge schreibt, wenn sich mehrere Benutzer auf demselben Computer befinden.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen
</dt> <dd>

Der lokalisierbare Schlüssel für den Registrierungs Wert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Diese Spalte enthält den Namen des Registrierungs Werts (lokalisierbar). Wenn dieser Wert NULL ist, werden die in die Spalte Wert eingegebenen Daten in den Standard Registrierungsschlüssel geschrieben.

Wenn die Value-Spalte NULL ist, haben die Zeichen folgen, die in der folgenden Tabelle in der Spalte "Name" angezeigt werden, eine besondere Bedeutung.



| String | Bedeutung                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | Der Schlüssel muss bei der Installation der Komponente erstellt werden, falls er nicht vorhanden ist.                                                                                                                            |
| \-     | Wenn die Komponente deinstalliert wird, muss der Schlüssel ggf. mit allen zugehörigen Werten und unter Schlüsseln gelöscht werden.                                                                                     |
| \*     | Der Schlüssel muss bei der Installation der Komponente erstellt werden, falls er nicht vorhanden ist. Außerdem muss der Schlüssel bei der Deinstallation der Komponente ggf. mit allen zugehörigen Werten und unter Schlüsseln gelöscht werden. |



 

Beachten Sie, dass die [Tabelle removeregistry](removeregistry-table.md) verwendet werden muss, wenn ein installierter Registrierungsschlüssel mit seinen Werten und unter Schlüsseln gelöscht werden soll, wenn die Komponente installiert ist.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Diese Spalte ist der lokalisierbare Registrierungs Wert. Das Feld ist [formatiert](formatted.md). Wenn der Wert einem der folgenden Präfixe (d. h. Wert) angefügt wird, \# % wird der Wert wie in der Tabelle beschrieben interpretiert. Beachten Sie, dass jedes Präfix mit einem Nummern Zeichen ( \# ) beginnt. Wenn der Wert mit zwei oder mehr aufeinander folgenden Nummern Zeichen ( \# ) beginnt, wird der erste \# ignoriert, und der Wert wird als Zeichenfolge interpretiert und gespeichert.



| Präfix | Bedeutung                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#Stuben    | Der Wert wird interpretiert und als Hexadezimalwert (reg \_ Binary) gespeichert.      |
| \#%    | Der Wert wird interpretiert und als erweiterbare Zeichenfolge (reg \_ Expand \_ SZ) gespeichert. |
| \#     | Der Wert wird interpretiert und als ganze Zahl gespeichert (reg \_ DWORD).                |



 

-   Wenn der Wert die Sequenz Tilde enthält \[ ~ \] , wird der Wert als eine durch Null getrennte Liste von Zeichen folgen (reg \_ \_ MultiSZ) interpretiert. Um z. b. eine Liste anzugeben, die die drei Zeichen folgen a, b und c enthält, verwenden Sie "a \[ ~ \] b \[ ~ \] c".
-   Die Sequenz \[ ~ \] innerhalb des Werts trennt die einzelnen Zeichen folgen und wird als NULL-Zeichen interpretiert und gespeichert.
-   Wenn eine \[ ~ \] der Zeichen folgen Liste vorangestellt ist, werden die Zeichen folgen an alle vorhandenen Registrierungs Wert Zeichenfolgen angehängt. Wenn bereits eine Anfüge Zeichenfolge im Registrierungs Wert vorhanden ist, wird das ursprüngliche Vorkommen der Zeichenfolge entfernt.
-   Wenn ein \[ ~ \] auf das Ende der Zeichen folgen Liste folgt, werden die Zeichen folgen allen vorhandenen Registrierungs Wert Zeichenfolgen vorangestellt. Wenn bereits eine ausstehende Zeichenfolge im Registrierungs Wert vorhanden ist, wird das ursprüngliche Vorkommen der Zeichenfolge entfernt.
-   Wenn ein \[ ~ \] sowohl am Anfang als auch am Ende oder weder am Anfang noch am Ende der Zeichen folgen Liste vorhanden ist, müssen die Zeichen folgen vorhandene Registrierungs Wert Zeichenfolgen ersetzen.
-   Andernfalls wird der Wert interpretiert und als Zeichenfolge (reg \_ SZ) gespeichert.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, mit der die Installation des Registrierungs Werts gesteuert wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Aktionen " [schreiteregistryvalues](writeregistryvalues-action.md) " und " [removeregistryvalues](removeregistryvalues-action.md) " in [*Sequenz Tabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

Die Registrierungsinformationen werden in die Systemregistrierung geschrieben, wenn die entsprechende Komponente für die lokale Installation ausgewählt oder von der Quelle aus ausgeführt wurde.

Beachten Sie, dass das Installationsprogramm einen Registrierungsschlüssel entfernt, nachdem der letzte Wert oder Unterschlüssel unter dem Schlüssel entfernt wurde. Um zu verhindern, dass ein leerer Registrierungsschlüssel beim Deinstallieren von entfernt wird, schreiben Sie einen Dummy-Wert unter dem Schlüssel, den Sie aufbewahren müssen, und geben Sie in der Spalte Name den Wert + ein. Wenn \* in der Spalte Name ist, wird der Schlüssel mit allen zugehörigen Werten und unter Schlüsseln gelöscht, wenn die Komponente entfernt wird.

Eine benutzerdefinierte Aktion kann verwendet werden, um der Registrierungs Tabelle während einer Installation, einer Neuinstallation oder einer Reparatur Transaktion Zeilen hinzuzufügen. Diese Zeilen bleiben in der Registrierungs Tabelle nicht erhalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar. Die benutzerdefinierte Aktion muss daher bei jeder Installation, deinstalstallation oder Reparatur Transaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen benötigt. Die benutzerdefinierte Aktion muss vor den Aktionen [removeregistryvalues](removeregistryvalues-action.md) und [schreiteregistryvalues](writeregistryvalues-action.md) in der Aktions Sequenz erfolgen.

Informationen zum Sichern eines Registrierungsschlüssels finden Sie in der Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) " und in der [Tabelle "lockberechtigungs](lockpermissions-table.md)Tabelle".

## <a name="validation"></a>Überprüfen

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE49](ice49.md)  
[ICE53](ice53.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE70](ice70.md)  
[ICE80](ice80.md)  
</dl>

 

 




