---
description: Die Tabelle Verknüpfung enthält die Informationen, die die Anwendung zum Erstellen von Verknüpfungen auf dem Computer des Benutzers benötigt.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Verknüpfungstabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47a5c5843b4ad1986d968329c9df9b6d9df5e291cd4adf06bccfcfa37adb66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628420"
---
# <a name="shortcut-table"></a>Verknüpfungstabelle

Die Tabelle Verknüpfung enthält die Informationen, die die Anwendung zum Erstellen von Verknüpfungen auf dem Computer des Benutzers benötigt.

Die Tabelle Verknüpfung enthält die folgenden Spalten.



| Spalte                 | Typ                         | Key | Nullwerte zulässig |
|------------------------|------------------------------|-----|----------|
| Verknüpfung               | [Identifier](identifier.md) | J   | N        |
| Verzeichnis\_            | [Identifier](identifier.md) | N   | N        |
| Name                   | [Filename](filename.md)     | N   | N        |
| Komponente\_            | [Identifier](identifier.md) | N   | N        |
| Ziel                 | [Tastenkombination](shortcut.md)     | N   | N        |
| Argumente              | [Formatiert](formatted.md)   | N   | J        |
| BESCHREIBUNG            | [Text](text.md)             | N   | J        |
| Hotkey                 | [Integer](integer.md)       | N   | J        |
| Symbol\_                 | [Identifier](identifier.md) | N   | J        |
| IconIndex              | [Integer](integer.md)       | N   | J        |
| ShowCmd                | [Integer](integer.md)       | N   | J        |
| WkDir                  | [Identifier](identifier.md) | N   | J        |
| DisplayResourceDLL     | [Formatiert](formatted.md)   | N   | J        |
| DisplayResourceId      | [Integer](integer.md)       | N   | J        |
| DescriptionResourceDLL | [Formatiert](formatted.md)   | N   | J        |
| DescriptionResourceId  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Verknüpfung
</dt> <dd>

Der Schlüsselwert für diese Tabelle.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Verzeichnis\_
</dt> <dd>

Der externe Schlüssel in der ersten Spalte der [Directory-Tabelle.](directory-table.md) Diese Spalte gibt das Verzeichnis an, in dem die Verknüpfungsdatei erstellt wird.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Der lokalisierbare Name der zu erstellenden Verknüpfung.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Der externe Schlüssel in der ersten Spalte der [Component-Tabelle.](component-table.md) Das Installationsprogramm verwendet den Installationsstatus der in dieser Spalte angegebenen Komponente, um zu bestimmen, ob die Verknüpfung erstellt oder gelöscht wird. Diese Komponente muss über einen gültigen Schlüsselpfad verfügen, damit die Verknüpfung installiert werden kann. Wenn die Spalte Ziel den Namen eines Features enthält, ist die durch die Verknüpfung gestartete Datei die Schlüsseldatei der in dieser Spalte aufgeführten Komponente.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Ziel
</dt> <dd>

Das Kontextziel.

Für eine angekündigte Verknüpfung muss diese Spalte ein externer Schlüssel in der ersten Spalte der [Featuretabelle](feature-table.md)sein. Das Installationsprogramm wertet den Eintrag im Feld Ziel als [Bezeichner](identifier.md) aus, und der Eintrag muss ein gültiger Fremdschlüssel in der [Featuretabelle](feature-table.md)sein. Die datei, die in diesem Fall durch die Verknüpfung gestartet wird, ist die Schlüsseldatei der Komponente, die in der Spalte Komponente aufgeführt \_ ist. Wenn die Verknüpfung aktiviert ist, überprüft das Installationsprogramm, ob alle Komponenten in der Funktion installiert sind, bevor diese Datei gestartet wird.

Für eine nicht angekündigte Verknüpfung wertet das Installationsprogramm dieses Feld als [formatierte](formatted.md) Zeichenfolge aus. Das Feld sollte einen Eigenschaftenbezeichner enthalten, der in eckige Klammern () eingeschlossen ist und \[ \] in die Datei oder einen Ordner erweitert wird, auf den durch die Verknüpfung verwiesen wird. Weitere Informationen finden Sie unter der [CreateShortcuts-Aktion.](createshortcuts-action.md)

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumente
</dt> <dd>

Die Befehlszeilenargumente für die Verknüpfung.

Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argumente eingeschränkt ist. Eine Eigenschaft, die in diesem Feld als Eigenschaft formatiert \[  \] ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits über den beabsichtigten Wert verfügt, wenn die Komponente installiert wird, die die Verknüpfung besitzt. Um beispielsweise zum richtigen Wert für das Argument " \[ \#MyDoc.doc" \] aufzulösen, muss derselbe Prozess die Datei MyDoc.doc und die Komponente installieren, die die Verknüpfung besitzt.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die lokalisierbare Beschreibung der Verknüpfung.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey
</dt> <dd>

Der Hotkey für die Verknüpfung. Das Low-Order-Byte enthält den Code des virtuellen Schlüssels für den Schlüssel, und das High-Order-Byte enthält Modifiziererflags. Dies muss eine nicht negative Zahl sein. Autoren von Installationspaketen wird im Allgemeinen empfohlen, diese Option nicht festzulegen, da die Einstellung dieser Option dem Desktop eines Benutzers doppelte Hotkeys hinzufügen kann. Darüber hinaus kann die Vorgehensweise zum Zuweisen von Hotkeys zu Verknüpfungen für Benutzer problematisch sein, die Hotkeys für [die Barrierefreiheit](accessibility.md)verwenden.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Symbol\_
</dt> <dd>

Der externe Schlüssel für die Spalte einer der [Symboltabellen.](icon-table.md)

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Der Symbolindex für die Verknüpfung. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

Der Befehl Anzeigen für das Anwendungsfenster.

Die folgenden Werte können verwendet werden. Die Werte sind für die Windows-API-Funktion ShowWindow definiert.



| Wert | Bedeutung             |
|-------|---------------------|
| 1     | SW \_ SHOWNORMAL      |
| 3     | SW \_ SHOWMAXIMIZED   |
| 7     | SW \_ SHOWMINNOACTIVE |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

Der Name der Eigenschaft, die über den Pfad des Arbeitsverzeichnisses für die Verknüpfung verfügt. Der Wert kann das Windows Format verwenden, um auf Umgebungsvariablen zu verweisen, z. B. %USERPROFILE%. Die Verweise werden in einen tatsächlichen Pfad aufgelöst, wenn das Installationsprogramm das Arbeitsverzeichnis auflöste, um die Verknüpfung zu erstellen.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

Dieses Feld enthält einen [Formatierten](formatted.md) Zeichenfolgenwert für den vollständigen Pfad zur sprachneutralen portierbaren ausführbaren Datei (LN-Datei), die die Daten der Ressourcenkonfiguration (RC-Konfiguration) enthält. Die formatierte Zeichenfolge kann die \[ \# \] FileKey-Konvention verwenden. Wenn dieses Feld einen Wert enthält, wird die Spalte Name ignoriert. Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert in der Spalte Name. Wenn dieses Feld einen Wert enthält, muss auch das Feld **DisplayResourceId** einen Wert enthalten, oder die Installation schlägt fehl.

Diese Spalte der Verknüpfungstabelle wird nur verwendet, wenn sie auf Windows Vista oder Windows Server 2008 ausgeführt wird. Andernfalls wird sie ignoriert. Diese Spalte ist mit Versionen verfügbar, die nicht älter als Windows Installer 4.0 sind.

Informationen zum Hinzufügen von Verknüpfungen zur Verknüpfungstabelle für die Verwendung mitHILFE VON RESSOURCEN finden Sie unter [A SHORTCUT Example](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

Der Anzeigenamenindex für die Verknüpfung. Dies muss eine nicht negative Zahl sein. Wenn dieses Feld einen Wert enthält, muss das Feld **DisplayResourceDLL** auch einen Wert enthalten, oder die Installation schlägt fehl.

Diese Spalte der Verknüpfungstabelle wird nur verwendet, wenn sie auf Windows Vista oder Windows Server 2008 ausgeführt wird. Andernfalls wird sie ignoriert. Diese Spalte ist mit Versionen verfügbar, die nicht älter als Windows Installer 4.0 sind.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL
</dt> <dd>

Dieses Feld enthält einen [Formatierten](formatted.md) Zeichenfolgenwert für den vollständigen Pfad zur sprachneutralen portierbaren ausführbaren Datei (LN-Datei), die die Daten der Ressourcenkonfiguration (RC-Konfiguration) enthält. Die formatierte Zeichenfolge kann die \[ \# \] FileKey-Konvention verwenden. Wenn dieses Feld einen Wert enthält, wird die Spalte Name ignoriert. Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert in der Spalte Beschreibung. Wenn dieses Feld einen Wert enthält, muss auch das Feld **DescriptionResourceId** einen Wert enthalten, oder die Installation schlägt fehl.

Diese Spalte der Verknüpfungstabelle wird nur verwendet, wenn sie auf Windows Vista oder Windows Server 2008 ausgeführt wird. Andernfalls wird sie ignoriert. Diese Spalte ist mit Versionen verfügbar, die nicht älter als Windows Installer 4.0 sind.

Informationen zum Hinzufügen von Verknüpfungen zur Verknüpfungstabelle für die Verwendung mitHILFE VON RESSOURCEN finden Sie unter [A SHORTCUT Example](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

Der Beschreibungsnamenindex für die Verknüpfung. Dies muss eine nicht negative Zahl sein. Wenn dieses Feld einen Wert enthält, muss das Feld **DescriptionResourceDLL** auch einen Wert enthalten, oder die Installation schlägt fehl.

Diese Spalte der Verknüpfungstabelle wird nur verwendet, wenn sie auf Windows Vista oder Windows Server 2008 ausgeführt wird. Andernfalls wird sie ignoriert. Diese Spalte ist mit Versionen verfügbar, die nicht älter als Windows Installer 4.0 sind.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Aktivierung eines Features erstellt nur dann eine angekündigte Verknüpfung, wenn die IShellLink-Schnittstelle des Systems die Auflösung des Installerdeskriptors unterstützt. Dies wird von Microsoft Windows 2000 und Systemen unterstützt, auf denen Microsoft Internet Explorer 4.01 ausgeführt wird. Wenn dies nicht unterstützt wird, erstellt das Installationsprogramm bei der Installation der Komponente des Features eine nicht angekündigte Verknüpfung, entweder lokal oder aus der Quelle ausgeführt.

Beachten Sie, dass angekündigte Verknüpfungen immer auf eine bestimmte Anwendung zeigen, die durch einen [**ProductCode**](productcode.md)identifiziert wird und nicht von Anwendungen gemeinsam genutzt werden sollte. Angekündigte Verknüpfungen funktionieren nur für die zuletzt installierte Anwendung und werden entfernt, wenn diese Anwendung entfernt wird.

Auf diese Tabelle wird verwiesen, wenn die [Aktion CreateShortcuts](createshortcuts-action.md) und die [RemoveShortcuts-Aktion](removeshortcuts-action.md) ausgeführt werden.

Siehe auch die [**DISABLEADVTSHORTCUTS-Eigenschaft.**](disableadvtshortcuts.md)

## <a name="validation"></a>Überprüfung

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

 

 



