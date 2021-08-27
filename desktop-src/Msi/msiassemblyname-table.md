---
description: Die Tabellen MsiAssembly und MsiAssemblyName geben Windows Installer-Einstellungen für Common Language Runtime-Assemblys und Win32-Assemblys an.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: MsiAssemblyName-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62c494f9669ad2c119606f3950a0ec34b6bfd6ba78ad7a965c45398a71ebafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129250"
---
# <a name="msiassemblyname-table"></a>MsiAssemblyName-Tabelle

Die [MsiAssembly-Tabelle](msiassembly-table.md) und die MsiAssemblyName-Tabelle geben Windows Installer-Einstellungen für Common Language Runtime-Assemblys und Win32-Assemblys an. Weitere Informationen finden Sie [unter Installation von Assemblys im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installation von Win32-Assemblys.](installation-of-win32-assemblies.md)

Die Tabelle MsiAssemblyName gibt das Schema für die Elemente eines starken Assemblycachenamens für eine .NET Framework oder Win32-Assembly an. Der Name wird erstellt, indem alle Elemente mit demselben Komponentenschlüssel angefügt \_ werden. Siehe folgendes Beispiel.

Windows Das Installationsprogramm kann Win32-Assemblys [als nebeneinander seitige Assemblys installieren.](side-by-side-assemblies.md) Weitere Informationen finden Sie unter [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).

Die Tabelle MsiAssemblyName enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Komponente\_ | [Identifier](identifier.md) | J   | N        |
| Name        | [Text](text.md)             | J   | N        |
| Wert       | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Geben Sie den Schlüssel in [die Komponententabelle ein,](component-table.md) der die Windows Installer-Komponente angibt, die diese Assembly enthält.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Name des Attributs, das dem in der Spalte Wert angegebenen Wert zugeordnet ist.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der Wert, der dem in der Spalte Name angegebenen Namen zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die in der MsiAssemblyName-Tabelle erstellten Informationen müssen mit den Informationen in der Manifestdatei der Assembly übereinstimmen. Wenn die Informationen im Manifest und in der MsiAssemblyName-Tabelle nicht übereinstimmen, kann das Entfernen der Anwendung die Assembly auf dem Computer verlassen.

Für Win32-Assemblys muss in der Tabelle MsiAssemblyName für jeden der folgenden Einträge im Feld Name eine Zeile enthalten sein: type, name, version, language, publicKeyToken und processorArchitecture. Der entsprechende Wert für jeden Namen kann in das Feld Wert eingegeben werden. Die Name-Wert-Paare in der MsiAssemblyName-Tabelle müssen mit den Attributen typ, name, version, language, publicKeyToken und processorArchitecture im Manifest der Assembly übereinstimmen.

Für private Common Language Runtime-Assemblys (.NET FrameworkVersions 1.0 und 1.1) muss die MsiAssemblyName-Tabelle eine Zeile für jeden der folgenden Einträge im Feld Name enthalten: Name, Version und Kultur. Der entsprechende Wert für jeden Namen kann in das Feld Wert eingegeben werden.

Für globale Common Language Runtime-Assemblys (.NET Framework Versionen 1.0 und 1.1) muss die Tabelle MsiAssemblyName eine Zeile für jeden der folgenden Einträge im Feld Name enthalten: Name, Version, Culture und PublicKeyToken. Der entsprechende Wert für jeden Namen kann in das Feld Wert eingegeben werden.

Die .NET Framework Version 1.1 ist die Mindestversion, die verwendet werden kann, um eine aktuelle Aktualisierung einer globalen Common Language Runtime-Assembly durchzuführen. Sie können die [**MsiNetAssemblySupport-Eigenschaft**](msinetassemblysupport.md) auf die Version überprüfen. Die Tabelle MsiAssemblyName muss auch über ein FileVersion-Feld verfügen, da diese Art von Assemblyupdate nur die FileVersion ändert. Weitere Informationen finden Sie unter [Aktualisieren von Assemblys.](updating-assemblies.md)

Beispielsweise kann das Assemblymanifest für ComponentA den Abschnitt assemblyIdentity wie folgt für eine Win32-Assembly enthalten.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

Füllen Sie in diesem Fall die Tabelle MsiAssemblyName wie folgt auf.



| Komponente  | Name                  | Wert             |
|------------|-----------------------|-------------------|
| ComponentA | Type                  | win32             |
| ComponentA | name                  | ms-sxstest-simple |
| ComponentA | version               | 1.0.0.0           |
| ComponentA | language              | en                |
| ComponentA | Publickeytoken        | 1111111111222222  |
| ComponentA | processorArchitecture | x86               |



 

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 
