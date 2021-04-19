---
description: Die MsiAssembly-Tabelle und die MsiAssemblyName-Tabelle geben Windows Installer Einstellungen für Common Language Runtime Assemblys und Win32-Assemblys an.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: MsiAssemblyName-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357075"
---
# <a name="msiassemblyname-table"></a>MsiAssemblyName-Tabelle

Die [MsiAssembly-Tabelle](msiassembly-table.md) und die MsiAssemblyName-Tabelle geben Windows Installer Einstellungen für Common Language Runtime Assemblys und Win32-Assemblys an. Weitere Informationen finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.

Die MsiAssemblyName-Tabelle gibt das Schema für die Elemente eines starken Assemblycache-namens für eine .NET Framework-oder Win32-Assembly an. Der Name wird erstellt, indem alle Elemente mit dem gleichen Komponenten Schlüssel angehängt werden \_ . Siehe folgendes Beispiel.

Windows Installer können Win32 [-](side-by-side-assemblies.md)Assemblys als parallele Assemblys installieren. Weitere Informationen finden Sie in der [API](../sbscs/side-by-side-assembly-api.md)für parallele Assemblys.

Die MsiAssemblyName-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Komponente\_ | [Bezeichner](identifier.md) | J   | N        |
| Name        | [Text](text.md)             | J   | N        |
| Wert       | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Der Schlüssel in die [Komponenten Tabelle](component-table.md) , der die Windows Installer Komponente angibt, die diese Assembly enthält.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der Name des Attributs, das dem in der Spalte Wert angegebenen Wert zugeordnet ist.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der Wert, der dem in der Spalte Name angegebenen Namen zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die in der MsiAssemblyName-Tabelle erstellten Informationen müssen mit den Informationen in der Manifest-Datei der Assembly identisch sein. Wenn die Informationen in der Manifest-und der MsiAssemblyName-Tabelle nicht stimmen, kann beim Entfernen der Anwendung die Assembly auf dem Computer belassen werden.

Für Win32-Assemblys muss in der Tabelle MsiAssemblyName eine Zeile für jeden der folgenden Einträge im Feld Name vorhanden sein: Type, Name, Version, Language, PublicKeyToken und ProcessorArchitecture. Der entsprechende Wert für jeden Namen kann in das Wertfeld eingegeben werden. Die Name-Wert-Paare in der MsiAssemblyName-Tabelle müssen den Attributen Type, Name, Version, Language, PublicKeyToken und ProcessorArchitecture im Manifest der Assembly entsprechen.

Für private Common Language Runtime-Assemblys (.net Frameworkversionen 1,0 und 1,1) muss die MsiAssemblyName-Tabelle eine Zeile für jeden der folgenden Einträge im Name-Feld enthalten: Name, Version und Kultur. Der entsprechende Wert für jeden Namen kann in das Wertfeld eingegeben werden.

Für globale Common Language Runtime Assemblys (.NET Framework Versionen 1,0 und 1,1) muss die MsiAssemblyName-Tabelle eine Zeile für jeden der folgenden Einträge im Feld Name enthalten: Name, Version, Kultur und PublicKeyToken. Der entsprechende Wert für jeden Namen kann in das Wertfeld eingegeben werden.

Der .NET Framework Version 1,1 ist die Mindestversion, die verwendet werden kann, um ein direktes Update einer globalen Common Language Runtime Assembly auszuführen. Sie können die Eigenschaft " [**MsiNetAssemblySupport**](msinetassemblysupport.md) " für die Version überprüfen. Die MsiAssemblyName-Tabelle muss auch ein fileversion-Feld aufweisen, da diese Art von Assemblyaktualisierung nur die Dateiversion ändert. Weitere Informationen finden Sie unter [Aktualisieren](updating-assemblies.md)von Assemblys.

Das Assemblymanifest für Componenta könnte z. b. einen assemblyIdentity-Abschnitt für eine Win32-Assembly wie folgt enthalten.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

Füllen Sie in diesem Fall die MsiAssemblyName-Tabelle wie folgt auf.



| Komponente  | Name                  | Wert             |
|------------|-----------------------|-------------------|
| Componenta | type                  | Win32             |
| Componenta | name                  | MS-sxstest-Simple |
| Componenta | version               | 1.0.0.0           |
| Componenta | language              | en                |
| Componenta | PublicKeyToken        | 1111111111222222  |
| Componenta | processorArchitecture | x86               |



 

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 
