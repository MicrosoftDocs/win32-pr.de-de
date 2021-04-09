---
description: Die Verknüpfungs Tabelle enthält die Informationen, die die Anwendung benötigt, um Verknüpfungen auf dem Computer des Benutzers zu erstellen.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Verknüpfungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866283"
---
# <a name="shortcut-table"></a>Verknüpfungs Tabelle

Die Verknüpfungs Tabelle enthält die Informationen, die die Anwendung benötigt, um Verknüpfungen auf dem Computer des Benutzers zu erstellen.

Die Verknüpfungs Tabelle enthält die folgenden Spalten.



| Spalte                 | Typ                         | Schlüssel | Nullwerte zulässig |
|------------------------|------------------------------|-----|----------|
| Abkürzung               | [Bezeichner](identifier.md) | J   | N        |
| Verzeichnis\_            | [Bezeichner](identifier.md) | N   | N        |
| Name                   | [Filename](filename.md)     | N   | N        |
| Komponente\_            | [Bezeichner](identifier.md) | N   | N        |
| Ziel                 | [Tastenkombination](shortcut.md)     | N   | N        |
| Argumente              | [Großformatige](formatted.md)   | N   | J        |
| BESCHREIBUNG            | [Text](text.md)             | N   | J        |
| Hotkey                 | [Integer](integer.md)       | N   | J        |
| Symbol\_                 | [Bezeichner](identifier.md) | N   | J        |
| IconIndex              | [Integer](integer.md)       | N   | J        |
| ShowCmd                | [Integer](integer.md)       | N   | J        |
| Wkdir                  | [Bezeichner](identifier.md) | N   | J        |
| Displayresourcedll     | [Großformatige](formatted.md)   | N   | J        |
| Displayresourceid      | [Integer](integer.md)       | N   | J        |
| Deskriptionresourcedll | [Großformatige](formatted.md)   | N   | J        |
| Deskriptionresourceid  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Kontext
</dt> <dd>

Der Schlüsselwert für diese Tabelle.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_
</dt> <dd>

Der externe Schlüssel in die erste Spalte der [Verzeichnis Tabelle](directory-table.md). Diese Spalte gibt das Verzeichnis an, in dem die Verknüpfungs Datei erstellt wird.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der lokalisierbare Name der zu erstellenden Verknüpfung.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Der externe Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md). Das Installationsprogramm verwendet den Installationsstatus der in dieser Spalte angegebenen Komponente, um zu bestimmen, ob die Verknüpfung erstellt oder gelöscht wird. Diese Komponente muss über einen gültigen Schlüssel Pfad für die zu installierende Verknüpfung verfügen. Wenn die Ziel Spalte den Namen einer Funktion enthält, ist die von der Verknüpfung gestartete Datei die Schlüsseldatei der in dieser Spalte aufgeführten Komponente.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar
</dt> <dd>

Das Verknüpfungs Ziel.

Bei einer angekündigten Verknüpfung muss es sich bei dieser Spalte um einen externen Schlüssel in der ersten Spalte der [Funktions Tabelle](feature-table.md)handeln. Das Installationsprogramm wertet den Eintrag im Zielfeld als [Bezeichner](identifier.md) aus, und der Eintrag muss ein gültiger Fremdschlüssel in der [Featuretabelle](feature-table.md)sein. Die von der Verknüpfung gestartete Datei ist in diesem Fall die Schlüsseldatei der Komponente, die in der Spalte Komponente aufgeführt ist \_ . Wenn die Verknüpfung aktiviert ist, überprüft das Installationsprogramm, ob alle Komponenten in der Funktion installiert sind, bevor diese Datei gestartet wird.

Bei einer nicht angekündigten Verknüpfung wertet das Installationsprogramm dieses Feld als [formatierte](formatted.md) Zeichenfolge aus. Das Feld muss einen Eigenschafts Bezeichner enthalten, der durch eckige Klammern ( \[ \] ) eingeschlossen ist, die in die Datei oder einen Ordner, auf den die Verknüpfung zeigt, erweitert wird. Weitere Informationen finden Sie unter der Aktion "" für " [kreateshortcuts](createshortcuts-action.md)".

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentation
</dt> <dd>

Die Befehlszeilenargumente für die Verknüpfung.

Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argumente eingeschränkt ist. Eine Eigenschaft, die als \[ *Eigenschaft* \] in diesem Feld formatiert ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits über den vorgesehenen Wert verfügt, wenn die Komponente, die die Verknüpfung besitzt, installiert ist. Um beispielsweise den richtigen Wert für das Argument " \[ \#MyDoc.doc\] " aufzulösen, muss der gleiche Prozess die Datei MyDoc.doc und die Komponente, die die Verknüpfung besitzt, installieren.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die lokalisierbare Beschreibung der Verknüpfung.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey
</dt> <dd>

Der Hotkey für die Verknüpfung. Das nieder wertige Byte enthält den Code des virtuellen Schlüssels für den Schlüssel, und das hochwertige Byte enthält Modifiziererflags. Dabei muss es sich um eine nicht negative Zahl handeln. In der Regel wird empfohlen, diese Option nicht festzulegen, da die Einstellung dieser Option dem Desktop eines Benutzers doppelte Hotkeys hinzufügen kann. Außerdem kann das Zuweisen von Hotkeys zu Verknüpfungen für Benutzer problematisch sein, die Hotkeys für [Barrierefreiheit](accessibility.md)verwenden.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Angezeigt\_
</dt> <dd>

Der externe Schlüssel für die Spalte einer der [Symboltabellen](icon-table.md).

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Der Symbol Index für die Verknüpfung. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

Der Show-Befehl für das Anwendungsfenster.

Die folgenden Werte können verwendet werden. Die Werte sind für die Windows-API-Funktion ShowWindow definiert.



| Wert | Bedeutung             |
|-------|---------------------|
| 1     | SW \_ Show normal      |
| 3     | SW \_ showmaximized   |
| 7     | SW \_ showminnoactive |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>Wkdir
</dt> <dd>

Der Name der Eigenschaft, die den Pfad des Arbeitsverzeichnisses für die Verknüpfung enthält. Der Wert kann das Windows-Format verwenden, um auf Umgebungsvariablen zu verweisen, z. b .% User Profile%. Die Verweise werden in einen tatsächlichen Pfad aufgelöst, wenn das Installationsprogramm das Arbeitsverzeichnis auflöst, um die Verknüpfung zu erstellen.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>Displayresourcedll
</dt> <dd>

Dieses Feld enthält einen [formatierten](formatted.md) Zeichen folgen Wert für den vollständigen Pfad zur sprach neutralen portablen ausführbaren Datei (LN-Datei), in der die Daten der Ressourcen Konfiguration (RC config) enthalten sind. Die formatierte Zeichenfolge kann die \[ \# filekey- \] Konvention verwenden. Wenn dieses Feld einen Wert enthält, wird die Spalte Name ignoriert. Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert in der Spalte Name. Wenn dieses Feld einen Wert enthält, muss auch das Feld **displayresourceid** einen Wert enthalten, sonst tritt bei der Installation ein Fehler auf.

Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird. Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.

Weitere Informationen zum Hinzufügen von Verknüpfungen zur Verknüpfungs Tabelle für die Verwendung mit MUI-Ressourcen finden Sie unter [Beispiel für eine MUI-Verknüpfung](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>Displayresourceid
</dt> <dd>

Der Anzeige Namensindex für die Verknüpfung. Dabei muss es sich um eine nicht negative Zahl handeln. Wenn dieses Feld einen Wert enthält, muss das Feld **displayresourcedll** ebenfalls einen Wert enthalten, da die Installation nicht erfolgreich ist.

Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird. Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>Deskriptionresourcedll
</dt> <dd>

Dieses Feld enthält einen [formatierten](formatted.md) Zeichen folgen Wert für den vollständigen Pfad zur sprach neutralen portablen ausführbaren Datei (LN-Datei), in der die Daten der Ressourcen Konfiguration (RC config) enthalten sind. Die formatierte Zeichenfolge kann die \[ \# filekey- \] Konvention verwenden. Wenn dieses Feld einen Wert enthält, wird die Spalte Name ignoriert. Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert in der Spalte Beschreibung. Wenn dieses Feld einen Wert enthält, muss auch das Feld **descriptionresourceid** einen Wert enthalten, sonst tritt bei der Installation ein Fehler auf.

Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird. Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.

Weitere Informationen zum Hinzufügen von Verknüpfungen zur Verknüpfungs Tabelle für die Verwendung mit MUI-Ressourcen finden Sie unter [Beispiel für eine MUI-Verknüpfung](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>Deskriptionresourceid
</dt> <dd>

Der Beschreibungs Name Index für die Verknüpfung. Dabei muss es sich um eine nicht negative Zahl handeln. Wenn dieses Feld einen Wert enthält, muss das Feld **descriptionresourcedll** ebenfalls einen Wert enthalten, da die Installation nicht erfolgreich ist.

Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird. Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Durch die Aktivierung einer Funktion wird nur dann eine angekündigte Verknüpfung erstellt, wenn die IShellLink-Schnittstelle des Systems die Installation des Installationsprogramm Deskriptors unterstützt. Dies wird von Microsoft Windows 2000 und Systemen unterstützt, die Microsoft Internet Explorer 4,01 ausführen. Wenn dies nicht unterstützt wird, erstellt das Installationsprogramm bei der Installation der featurekomponente eine nicht angekündigte Verknüpfung, entweder lokal oder über die Quelle auszuführen.

Beachten Sie, dass angekündigte Verknüpfungen immer auf eine bestimmte Anwendung verweisen, die durch einen [**ProductCode**](productcode.md)gekennzeichnet ist und nicht von Anwendungen gemeinsam verwendet werden sollte. Angekündigte Verknüpfungen funktionieren nur für die zuletzt installierte Anwendung und werden entfernt, wenn diese Anwendung entfernt wird.

Diese Tabelle wird verwendet, wenn die Aktion " [kreateshortcuts](createshortcuts-action.md) " und die [removeshortcuts-Aktion](removeshortcuts-action.md) ausgeführt werden.

Siehe auch die [**disableadvtverknüpfungs**](disableadvtshortcuts.md) -Eigenschaft.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE94](ice94.md)  
</dl>

 

 



