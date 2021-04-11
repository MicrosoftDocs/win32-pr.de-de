---
description: In der Komponenten Tabelle sind die Komponenten und die folgenden Spalten aufgeführt.
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: Komponenten Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b721996767fa98209f0e13530f8f1bb1ba8cca07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214956"
---
# <a name="component-table"></a>Komponenten Tabelle

In der Komponenten Tabelle sind die Komponenten und die folgenden Spalten aufgeführt.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Komponente   | [Bezeichner](identifier.md) | J   | N        |
| ComponentID | [GUID](guid.md)             | N   | J        |
| Verzeichnis\_ | [Bezeichner](identifier.md) | N   | N        |
| Attribute  | [Integer](integer.md)       | N   | N        |
| Bedingung   | [Condition](condition.md)   | N   | J        |
| KEYPATH     | [Bezeichner](identifier.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Zulieferern
</dt> <dd>

Identifiziert den Komponenten Daten Satz.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentID
</dt> <dd>

Eine Zeichen folgen-GUID, die für diese Komponente, Version und Sprache eindeutig ist.

Beachten Sie, dass die Buchstaben dieser GUIDs Großbuchstaben sein müssen. Dienstprogramme wie GUIDGEN können GUIDs generieren, die Kleinbuchstaben enthalten. Die Kleinbuchstaben müssen in Großbuchstaben geändert werden, um diese gültigen Komponenten Code-GUIDs zu erstellen.

Wenn diese Spalte NULL ist, registriert der Installer die Komponente nicht, und die Komponente kann vom Installationsprogramm nicht entfernt oder repariert werden. Dies kann absichtlich erfolgen, wenn die Komponente nur während der Installation benötigt wird, z. b. eine benutzerdefinierte Aktion, die temporäre Dateien bereinigt oder ein altes Produkt entfernt. Dies kann auch hilfreich sein, wenn Sie Datendateien auf den Computer eines Benutzers kopieren, der nicht registriert werden muss.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_
</dt> <dd>

Externer Schlüssel eines Eintrags in der [Verzeichnis Tabelle](directory-table.md). Dies ist ein Eigenschaftsname, dessen Wert den tatsächlichen Pfad enthält. dieser kann entweder durch die [AppSearch-Aktion](appsearch-action.md) oder durch die Standardeinstellung aus der Verzeichnis Tabelle festgelegt werden.

Entwickler müssen die Erstellung von Komponenten vermeiden, die Dateien in einem der Benutzerprofil Ordner platzieren. Diese Dateien sind nicht für alle Benutzer in mehr Benutzer Situationen verfügbar und können dazu führen, dass das Installationsprogramm die Komponente dauerhaft als Reparaturvorgang anfordert.

Externer Schlüssel für Spalte 1 der Verzeichnis Tabelle.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Diese Spalte enthält ein Bitflag, das Optionen für die Remote Ausführung angibt. Fügen Sie das angegeben Bit zum Gesamtwert in der Spalte hinzu, um eine Option einzuschließen.

> [!Note]  
> Im Fall einer MSI-Datei, die von einem Webspeicherort heruntergeladen wird, sollten die Attributflags nicht so festgelegt werden, dass eine Komponente von der Quelle aus ausgeführt werden kann. Dies ist eine Einschränkung des Windows Installer und kann den Funktionsstatus von InstallState \_ badconfig zurückgeben.

 



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Bitflag</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>msidbcomponentattributeslocalonly</strong></dt> <dt>0</dt> <dt>0x0000</dt> </dl> Die Komponente kann nicht aus der Quelle ausgeführt werden. Legen Sie dieses Bit für alle Komponenten fest, die zu einem Feature gehören, um zu verhindern, dass die Funktion aus dem Netzwerk oder aus der Quelle ausgeführt wird. Beachten Sie Folgendes: Wenn eine Funktion keine Komponenten aufweist, zeigt die Funktion immer "Run-From-Source" und "Run-From-My-Computer" als gültige Optionen an.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbcomponentattributessourceonly</strong></dt> <dt>1</dt> <dt>0x0001</dt> </dl> Die Komponente kann nur über die Quelle ausgeführt werden. Legen Sie dieses Bit für alle Komponenten fest, die zu einem Feature gehören, um zu verhindern, dass die Funktion von-My-Computer ausgeführt wird. Beachten Sie Folgendes: Wenn eine Funktion keine Komponenten aufweist, zeigt die Funktion immer "Run-From-Source" und "Run-From-My-Computer" als gültige Optionen an.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbcomponentattributesoptional</strong></dt> <dt>2</dt> <dt>0x0002</dt> </dl> Die Komponente kann lokal oder über die Quelle ausgeführt werden.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbcomponentattributesregistrykeypath</strong></dt> <dt>4</dt> <dt>0x0004</dt> </dl> Wenn dieses Bit festgelegt ist, wird der Wert in der KEYPATH-Spalte als Schlüssel in der <a href="registry-table.md">Registrierungs Tabelle</a>verwendet. Wenn das Wertfeld des entsprechenden Datensatzes in der Registrierungs Tabelle NULL ist, darf das Namensfeld in diesem Datensatz nicht &quot; + &quot; , &quot; - &quot; oder enthalten &quot; * &quot; . Weitere Informationen finden Sie in der Beschreibung des Namens Felds in der <a href="registry-table.md">Registrierungs Tabelle</a>.<br/> Das Festlegen dieses Bits wird für Registrierungseinträge empfohlen, die in HKCU Hive geschrieben werden. Dadurch wird sichergestellt, dass das Installationsprogramm die erforderlichen HKCU-Registrierungseinträge schreibt, wenn sich mehrere Benutzer auf demselben Computer befinden.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbcomponentattributesshareddllref count</strong></dt> <dt>8</dt> <dt>0x0008</dt> </dl> Wenn dieses Bit festgelegt ist, erhöht das Installationsprogramm den Verweis Zähler in der freigegebenen DLL-Registrierung der Schlüsseldatei der Komponente. Wenn dieses Bit nicht festgelegt ist, erhöht das Installationsprogramm den Verweis Zähler nur, wenn der Verweis Zähler bereits vorhanden ist.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbcomponentattributespermanent</strong></dt> <dt>16</dt> <dt>0x0010</dt> </dl> Wenn dieses Bit festgelegt ist, entfernt das Installationsprogramm die Komponente nicht während einer Deinstallation. Der Installer registriert einen zusätzlichen System Client für die Komponente in den Windows Installer Registrierungs Einstellungen.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbcomponentattributesodbcdatasource</strong></dt> <dt>32</dt> <dt>0x0020</dt> </dl> Wenn dieses Bit festgelegt ist, ist der Wert in der KEYPATH-Spalte ein Schlüssel in der <a href="odbcdatasource-table.md">ODBCDatasource-Tabelle</a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbcomponentattributestransitive</strong></dt> <dt>64</dt> <dt>0x0040</dt> </dl> Wenn dieses Bit festgelegt ist, wertet das Installationsprogramm den Wert der Anweisung in der Spalte Bedingung bei einer erneuten Installation erneut aus. Wenn der Wert zuvor false war und in true geändert wurde, installiert der Installer die Komponente. Wenn der Wert zuvor true war und in false geändert wurde, entfernt das Installationsprogramm die Komponente, auch wenn die Komponente andere Produkte als Clients hat.<br/> Dieses Bit sollte nur für transitiv Komponenten festgelegt werden. Weitere Informationen finden <a href="using-transitive-components.md">Sie unter Verwenden transitiv Komponenten</a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbcomponentattributesneverüberschreibung</strong></dt> <dt>128</dt> <dt>0x0080</dt> </dl> Wenn dieses Bit festgelegt ist, installiert oder installiert das Installationsprogramm die Komponente nicht, wenn eine Schlüssel Pfad Datei oder ein Schlüssel Pfad-Registrierungs Eintrag für die Komponente bereits vorhanden ist. Die Anwendung registriert sich selbst als Client der-Komponente.<br/> Verwenden Sie dieses Flag nur für Komponenten, die von der Registrierungs Tabelle registriert werden. Verwenden Sie dieses Flag nicht für Komponenten, die von den Tabellen <a href="appid-table.md">AppID</a>, <a href="class-table.md">Class</a>, <a href="extension-table.md">Extension</a>, <a href="progid-table.md">ProgID</a>, <a href="mime-table.md">MIME</a>und <a href="verb-table.md">Verb</a>registriert werden.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributes64bit</strong></dt> <dt>256</dt> <dt>0x0100</dt> </dl> Legen Sie dieses Bit fest, um dies als 64-Bit-Komponente zu markieren. Dieses Attribut vereinfacht die Installation von Paketen, die sowohl 32-Bit-als auch 64-Bit-Komponenten enthalten. Wenn dieses Bit nicht festgelegt ist, wird die Komponente als 32-Bit-Komponente registriert.<br/> Wenn es sich um eine 64-Bit-Komponente handelt, die eine 32-Bit-Komponente ersetzt, legen Sie dieses Bit fest, und weisen Sie in der Spalte ComponentID eine neue GUID zu.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbcomponentattributesdisableregistryreflection</strong></dt> <dt>512</dt> <dt>0x0200</dt> </dl> Legen Sie dieses Bit fest, um die Überprüfung der <a href="/windows/desktop/WinProg64/registry-reflection">Registrierung</a> für alle vorhandenen und neuen Registrierungsschlüssel, die von dieser Komponente betroffen sind Wenn dieses Bit festgelegt ist, ruft der Windows Installer den <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>regdisablereflectionkey</strong></a> für jeden Schlüssel auf, auf den die Komponente zugreift. Dieses Bit ist in Windows Installer Version 4,0 verfügbar. Dieses Bit wird auf 32-Bit-Systemen ignoriert. Dieses Bit wird in den 64-Bit-Versionen von Windows XP ignoriert.<br/>
<blockquote>
[!Note]<br />
32-Bit-Windows-Anwendungen, die auf dem 64-Bit-Windows-Emulator (WOW64) ausgeführt werden, verweisen auf eine andere Ansicht der Registrierung als 64-Bit-Anwendungen. Die Registrierungs Reflektion kopiert einige Registrierungs Werte zwischen diesen beiden Registrierungs Sichten.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbcomponentattributesuninstallonablösung</strong></dt> <dt>1024</dt> <dt>0x0400</dt> </dl> Legen Sie dieses Bit für eine Komponente in einem Patchpaket fest, um zu verhindern, dass verwaiste Komponenten auf dem Computer belassen werden. Wenn ein späterer Patch installiert wird, der mit dem <strong>msidbpatchsequencesupersedefrüher</strong> -Wert in der <a href="msipatchsequence-table.md">msipatchsequence</a> -Tabelle gekennzeichnet ist, um den ersten Patch zu ersetzen, können Windows Installer 4,5 und höher die Registrierung aufheben und Komponenten deinstallieren, die mit dem Wert " <strong>msidbcomponentattributesuninstallonablösung</strong> " gekennzeichnet sind. Wenn die Komponente nicht mit diesem Bit markiert ist, kann die Installation eines abersetzenden Patches hinter einer nicht verwendeten Komponente auf dem Computer belassen.<br/> Das Festlegen der <strong>msiuninstallablösung dedcomponents</strong> -Eigenschaft hat dieselbe Auswirkung wie das Festlegen dieses Bits für alle Komponenten.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 und früher</a>:</strong> der <strong>msidbcomponentattributesuninstallonablösung</strong> -Wert wird nicht unterstützt und wird ignoriert.<br/> <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbcomponentattributesshared</strong></dt> <dt>2048</dt> <dt>0x0800</dt> </dl> Wenn eine Komponente mit diesem Attribut Wert in mindestens einem Paket gekennzeichnet ist, das auf dem System installiert ist, wird die Komponente vom Installationsprogramm in allen Paketen als markiert behandelt. Wenn ein Paket, das die markierte Komponente freigibt, deinstalliert wird, kann Windows Installer 4,5 weiterhin die höchste Version der Komponente auf dem System freigeben, auch wenn die höchste Version von dem Paket installiert wurde, das deinstalliert wird. <br/> Wenn die disablesharedcomponent-Richtlinie auf 1 festgelegt ist, ruft kein Paket die Funktionalität der freigegebenen Komponente ab, die von diesem Bit aktiviert wird.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 und früher</a>:</strong> der <strong>msidbcomponentattributesshared</strong> -Wert wird nicht unterstützt und wird ignoriert.<br/> <br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Diese Spalte enthält eine Bedingungs Anweisung, mit der gesteuert werden kann, ob eine Komponente installiert ist. Wenn die Bedingung NULL ist oder als true ausgewertet wird, ist die Komponente aktiviert. Wenn die Bedingung zu false ausgewertet wird, wird die Komponente deaktiviert und ist nicht installiert.

Das Bedingungs Feld aktiviert oder deaktiviert eine Komponente nur während der [costfinalize-Aktion](costfinalize-action.md). Zum Aktivieren oder Deaktivieren einer Komponente nach "costfinalize" müssen Sie eine benutzerdefinierte Aktion oder das [doaction-ControlEvent](doaction-controlevent.md) zum Aufrufen von " [**msisetcomponentstate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)" verwenden.

Beachten Sie Folgendes: es sei denn, das transitive Bit in der Spalte Attribute ist für eine Komponente festgelegt, die Komponente bleibt nach der Installation auch dann aktiviert, wenn die bedingte Anweisung in der Spalte Bedingung später in einer nachfolgenden Wartungs Installation des Produkts zu false ausgewertet wird.

Die Spalte Bedingung in der Component-Tabelle akzeptiert bedingte Ausdrücke, die Verweise auf die installierten Status von Features und Komponenten enthalten. Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.

</dd> <dt>

<span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KEYPATH
</dt> <dd>

Dieser Wert verweist auf eine Datei oder einen Ordner, der zu der Komponente gehört, die vom Installationsprogramm zum Erkennen der Komponente verwendet wird. Zwei Komponenten können nicht denselben Schlüssel Pfad Wert verwenden. Der Wert in dieser Spalte ist auch der Pfad, der von der [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) -Funktion zurückgegeben wird.

Wenn der Wert nicht NULL ist, ist KEYPATH abhängig vom Attribut Wert entweder ein Primärschlüssel in der [Registrierung](registry-table.md), in der [ODBCDatasource](odbcdatasource-table.md)oder in den [Datei Tabellen](file-table.md) . Wenn KEYPATH NULL ist, wird der Ordner der Verzeichnis \_ Spalte als Schlüssel Pfad verwendet.

Da Ordner, die vom Installationsprogramm erstellt werden, gelöscht werden, wenn Sie leer sind, müssen Sie einen Eintrag in der Tabelle "| [atefolder](createfolder-table.md) " erstellen, um eine Komponente zu installieren, die aus einem leeren Ordner besteht.

Beachten Sie Folgendes: Wenn eine Windows Installer Komponente eine Datei oder einen Registrierungsschlüssel enthält, die durch [Windows-Ressourcenschutz](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) oder eine durch den Windows-Datei Schutz (WFP) geschützte Datei geschützt ist, muss diese Ressource als KEYPATH für die Komponente verwendet werden. In diesem Fall wird die Komponente von Windows Installer nicht installiert, aktualisiert oder entfernt. Sie sollten keine geschützten Ressourcen in ein Installationspaket einschließen. Verwenden Sie stattdessen die [unterstützten Mechanismen zur Ressourcen Ersetzung](/windows/desktop/Wfp/supported-file-replacement-mechanisms) für Windows-Ressourcenschutz. Weitere Informationen finden Sie unter [Verwenden von Windows Installer und Windows-Ressourcenschutz](windows-resource-protection-on-windows-vista.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung der Beziehung zwischen Komponenten und Features finden Sie unter [Funktions Tabelle](feature-table.md).

Das Installationsprogramm speichert freigegebene DLLs unabhängig vom Verweis Zähler der freigegebenen DLL in der Registrierung. Wenn in der Registrierung ein Verweis Zähler für eine freigegebene DLL vorhanden ist, erhöht der Installer immer die Anzahl, wenn die Datei installiert wird, und dekreliert diese, wenn Sie deinstalliert wird. Wenn **msidbcomponentattributesshareddllref count** nicht festgelegt ist und der Verweis Zähler nicht bereits vorhanden ist, erstellt das Installationsprogramm keine. Beachten Sie, dass der Verweis Zähler für SharedDLLs in der Registrierung für alle Dateien, die im System Ordner installiert sind, inkrementiert wird.

Wenn **msidbcomponentattributesshareddllrefcount** nicht festgelegt ist, kann eine andere Anwendung die Komponente entfernen, auch wenn Sie noch benötigt wird. Betrachten Sie das folgende Szenario, um zu sehen, wie dies passieren könnte:

-   Eine Anwendung, die das Installationsprogramm verwendet, installiert eine freigegebene Komponente.
-   Das **msidbcomponentattributesshareddllref count** -Bit ist nicht festgelegt, und es gibt keinen Verweis Zähler. Daher beginnt der Installer nicht mit einem Verweis Zähler.
-   Eine ältere Anwendung, die diese Komponente freigibt und den Installer nicht verwendet, ist installiert.
-   Die Legacy Anwendung erstellt und erhöht den Verweis Zähler für die freigegebene Komponente.
-   Die Legacy Anwendung wird deinstalliert.
-   Der Verweis Zähler für die freigegebene Komponente wird auf 0 (null) dekrementiert, und die Komponente wird entfernt.
-   Die Anwendung, die das Installationsprogramm verwendet, hat keinen Zugriff mehr auf die Komponente.

Um dieses Verhalten zu vermeiden, legen Sie **msidbcomponentattributesshareddllrefcount** fest.

Beachten Sie, dass die Systemdienst Komponenten nicht als "Run-From-Source" angegeben werden sollten, ohne speziell für solche Zwecke entworfen zu werden. Weitere Informationen finden Sie in der [Tabelle servicabstall](serviceinstall-table.md) .

Beachten Sie, dass Attribute, die die Installation von "Run-From-Source" aktivieren, nie für Komponenten festgelegt werden dürfen, die Dynamic Link-Bibliotheken enthalten, die in den Systemordner Der Grund hierfür ist, dass bei nachfolgenden Aufrufen von LoadLibrary in der dll ein Fehler bei nachfolgenden Aufrufen von **LoadLibrary** auf der dll auftreten würde, wenn der Installationsstatus der Komponente auf "Run-From-Source" festgelegt wird, indem Sie einer Funktion folgt

Siehe auch, [Steuern von Funktionsauswahl Zuständen](controlling-feature-selection-states.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE08](ice08.md)  
[ICE09](ice09.md)  
[ICE18](ice18.md)  
[ICE19](ice19.md)  
[ICE21](ice21.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE38](ice38.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE54](ice54.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE76](ice76.md)  
[ICE79](ice79.md)  
[ICE80](ice80.md)  
[ICE83](ice83.md)  
[ICE86](ice86.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE92](ice92.md)  
[ICE97](ice97.md)  
</dl>

