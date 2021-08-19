---
description: Die Registrierungstabelle enthält die Registrierungsinformationen, die die Anwendung in der Systemregistrierung festlegen muss.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Registrierungstabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b76fbc52357cdba68dfdcdda37e6edb3032086bf101788db0cdc69c0281264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128990"
---
# <a name="registry-table"></a>Registrierungstabelle

Die Registrierungstabelle enthält die Registrierungsinformationen, die die Anwendung in der Systemregistrierung festlegen muss.

Die Tabelle Registry enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Registrierung    | [Identifier](identifier.md) | J   | N        |
| Root        | [Integer](integer.md)       | N   | N        |
| Key         | [RegPath](regpath.md)       | N   | N        |
| Name        | [Formatiert](formatted.md)   | N   | J        |
| Wert       | [Formatiert](formatted.md)   | N   | J        |
| Komponente\_ | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registrierung
</dt> <dd>

Primärschlüssel, der zum Identifizieren eines Registrierungsdatensatzes verwendet wird.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>wurzel
</dt> <dd>

Der vordefinierte Stammschlüssel für den Registrierungswert. Geben Sie in dieses Feld den Wert -1 ein, um den Stammschlüssel vom Installationstyp abhängig zu machen. Geben Sie einen der anderen Werte in der folgenden Tabelle ein, um zu erzwingen, dass der Registrierungswert unter einem bestimmten Stammschlüssel geschrieben wird.



| Konstante                          | Hexadezimal | Decimal | Stammschlüssel                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                            | \- 0x001    | –1      | Wenn es sich um eine benutzerspezifische Installation handelt, wird der Registrierungswert unter **HKEY \_ CURRENT \_ USER** geschrieben. Wenn es sich um eine Computerinstallation handelt, wird der Registrierungswert unter **HKEY \_ LOCAL \_ MACHINE** geschrieben. Beachten Sie, dass eine Installation pro Computer durch Festlegen der [**ALLUSERS-Eigenschaft**](allusers.md) auf 1 angegeben wird.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ ROOT** Das Installationsprogramm schreibt oder entfernt den Wert während der Installation im [Installationskontext](installation-context.md)pro Benutzer aus der **HKCU-Softwareklassenstruktur. \\ \\**<br/> Das Installationsprogramm schreibt oder entfernt den Wert während der Computerinstallationen aus der **\\ HKLM-Softwareklassenstruktur. \\**<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **AKTUELLER \_ \_ HKEY-BENUTZER**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ LOCAL \_ MACHINE**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **\_HKEY-BENUTZER**                                                                                                                                                                                                                                                                                                                              |



 

Beachten Sie, dass es empfohlen wird, in die **HKCU-Struktur** geschriebene Registrierungseinträge auf eine Komponente zu verweisen, für die das RegistryKeyPath-Bit in der Spalte Attribute der [Tabelle Component](component-table.md)festgelegt ist. Dadurch wird sichergestellt, dass das Installationsprogramm die erforderlichen Registrierungseinträge schreibt, wenn sich mehrere Benutzer auf demselben Computer befinden.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Schlüssel
</dt> <dd>

Der lokalisierbare Schlüssel für den Registrierungswert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Diese Spalte enthält den Registrierungswertnamen (lokalisierbar). Wenn dies NULL ist, werden die in die Spalte Wert eingegebenen Daten in den Standardregistrierungsschlüssel geschrieben.

Wenn die Value-Spalte NULL ist, haben die in der folgenden Tabelle in der Spalte Name angezeigten Zeichenfolgen eine besondere Bedeutung.



| String | Bedeutung                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | Der Schlüssel muss erstellt werden, wenn er nicht vorhanden ist, wenn die Komponente installiert wird.                                                                                                                            |
| \-     | Der Schlüssel muss bei der Deinstallation der Komponente ggf. mit allen werten und Unterschlüsseln gelöscht werden.                                                                                     |
| \*     | Der Schlüssel muss erstellt werden, wenn er nicht vorhanden ist, wenn die Komponente installiert wird. Darüber hinaus muss der Schlüssel bei der Deinstallation der Komponente mit allen Werten und Unterschlüsseln gelöscht werden, sofern vorhanden. |



 

Beachten Sie, dass die [RemoveRegistry-Tabelle](removeregistry-table.md) verwendet werden muss, wenn ein installierter Registrierungsschlüssel mit ihren Werten und Unterschlüsseln gelöscht werden soll, wenn die Komponente installiert wird.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Diese Spalte ist der lokalisierbare Registrierungswert. Das Feld ist [formatiert.](formatted.md) Wenn der Wert an eines der folgenden Präfixe (d. h. \# % *value)* angefügt ist, wird der Wert wie in der Tabelle beschrieben interpretiert. Beachten Sie, dass jedes Präfix mit einem Nummernzeichen beginnt ( \# ). Wenn der Wert mit zwei oder mehr aufeinander folgenden Nummernzeichen () beginnt, \# wird der erste ignoriert, und der Wert \# wird als Zeichenfolge interpretiert und gespeichert.



| Präfix | Bedeutung                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#x    | Der Wert wird als Hexadezimalwert (REG BINARY) interpretiert und \_ gespeichert.      |
| \#%    | Der Wert wird als erweiterbare Zeichenfolge interpretiert und gespeichert (REG \_ EXPAND \_ SZ). |
| \#     | Der Wert wird als ganze Zahl (REG DWORD) interpretiert und \_ gespeichert.                |



 

-   Wenn der Wert die Sequenzkachel \[ ~ \] enthält, wird der Wert als durch NULL getrennte Liste von Zeichenfolgen (REG \_ MULTI \_ SZ) interpretiert. Um beispielsweise eine Liste mit den drei Zeichenfolgen a, b und c anzugeben, verwenden Sie "a \[ ~ \] b \[ ~ \] c".
-   Die Sequenz \[ ~ \] innerhalb des Werts trennt die einzelnen Zeichenfolgen und wird als NULL-Zeichen interpretiert und gespeichert.
-   Wenn ein \[ ~ \] der Zeichenfolgenliste vorangestellt ist, müssen die Zeichenfolgen an alle vorhandenen Registrierungswertzeichenfolgen angefügt werden. Wenn bereits eine Anfügezeichenfolge im Registrierungswert vorhanden ist, wird das ursprüngliche Vorkommen der Zeichenfolge entfernt.
-   Wenn ein \[ ~ \] auf das Ende der Zeichenfolgenliste folgt, müssen die Zeichenfolgen allen vorhandenen Registrierungswertzeichenfolgen voranzugeht werden. Wenn bereits eine vorausstehende Zeichenfolge im Registrierungswert auftritt, wird das ursprüngliche Vorkommen der Zeichenfolge entfernt.
-   Wenn sich sowohl am Anfang als auch am Ende oder weder am Anfang noch am Ende der Zeichenfolgenliste befindet, ersetzen die Zeichenfolgen alle vorhandenen \[ ~ \] Registrierungswertzeichenfolgen.
-   Andernfalls wird der Wert interpretiert und als Zeichenfolge (REG \_ SZ) gespeichert.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Tabelle Komponente,](component-table.md) die auf die Komponente verweisen, die die Installation des Registrierungswerts steuert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [WriteRegistryValues-](writeregistryvalues-action.md) [und RemoveRegistryValues-Aktionen](removeregistryvalues-action.md) in [*Sequenztabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen finden* Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

Die Registrierungsinformationen werden in die Systemregistrierung geschrieben, wenn die entsprechende Komponente ausgewählt wurde, um lokal installiert oder aus der Quelle ausgeführt zu werden.

Beachten Sie, dass das Installationsprogramm einen Registrierungsschlüssel entfernt, nachdem der letzte Wert oder Unterschlüssel unter dem Schlüssel entfernt wurde. Um zu verhindern, dass ein leerer Registrierungsschlüssel bei der Deinstallation entfernt wird, schreiben Sie einen Dummywert unter dem Schlüssel, den Sie behalten müssen, und geben Sie + in die Spalte Name ein. Wenn sich in der Spalte Name befindet, wird der Schlüssel mit allen Werten und \* Unterschlüsseln gelöscht, wenn die Komponente entfernt wird.

Eine benutzerdefinierte Aktion kann verwendet werden, um der Registrierungstabelle während einer Installation, Deinstallation oder Reparaturtransaktion Zeilen hinzuzufügen. Diese Zeilen werden in der Registrierungstabelle nicht beibehalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar. Die benutzerdefinierte Aktion muss daher in jeder Installations-, Deinstallations- oder Reparaturtransaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen erfordert. Die benutzerdefinierte Aktion muss vor den [Aktionen RemoveRegistryValues](removeregistryvalues-action.md) und [WriteRegistryValues](writeregistryvalues-action.md) in der Aktionssequenz ausgeführt werden.

Informationen zum Schützen eines Registrierungsschlüssels finden Sie in der [MsiLockPermissionsEx-Tabelle](msilockpermissionsex-table.md) und [der LockPermissions-Tabelle.](lockpermissions-table.md)

## <a name="validation"></a>Überprüfung

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

 

 




