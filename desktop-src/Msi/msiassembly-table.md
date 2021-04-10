---
description: Die MsiAssembly-Tabelle gibt Windows Installer Einstellungen für Microsoft .net Frameworkassemblys und Win32-Assemblys an Weitere Informationen finden Sie unter Installieren von Assemblys im globalen Assemblycache und Installieren von Win32-Assemblys.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: MsiAssembly-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960835"
---
# <a name="msiassembly-table"></a>MsiAssembly-Tabelle

Die MsiAssembly-Tabelle gibt Windows Installer Einstellungen für Microsoft .net Frameworkassemblys und Win32-Assemblys an Weitere Informationen finden Sie unter [Installieren von](installation-of-assemblies-to-the-global-assembly-cache.md) Assemblys im globalen Assemblycache und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.

Unter Windows XP können Windows Installer [Win32-Assemblys als parallele](side-by-side-assemblies.md)Assemblys installieren. Weitere Informationen finden Sie in der [API](../sbscs/side-by-side-assembly-api.md)für parallele Assemblys.

**Windows 2000:** Diese Funktion wird nicht unterstützt.

Die MsiAssembly-Tabelle weist die folgenden Spalten auf.



| Spalte            | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------------|------------------------------|-----|----------|
| Komponente\_       | [Bezeichner](identifier.md) | J   | N        |
| Funktion\_         | [Bezeichner](identifier.md) | N   | N        |
| Datei \_ Manifest    | [Bezeichner](identifier.md) | N   | J        |
| Datei \_ Anwendung | [Bezeichner](identifier.md) | N   | J        |
| Attribute        | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Der Schlüssel in der [Komponenten Tabelle](component-table.md) , der die Windows Installer Komponente angibt, die diese Assembly enthält.

Der Wert in diesem Feld darf nicht auf NULL festgelegt werden. Das Feld "KEYPATH" der Komponente in der [Komponenten Tabelle](component-table.md) darf nicht NULL sein.

Bei Win32-Assemblys kann der KEYPATH der Komponente nicht die im Datei Manifest angegebene Manifest-Datei sein \_ . Das Manifest kann der KEYPATH für eine .NET Framework-oder Richtlinienassembly sein.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Schlüssel in der [Featuretabelle](feature-table.md).

Wenn die Assembly durch eine Featureinstallation installiert werden muss, installiert Windows Installer das Feature, auf das dieses Feld verweist.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Datei \_ Manifest
</dt> <dd>

Ein externer Schlüssel in die [Dateitabelle](file-table.md) , der die Datei angibt, die das Manifest für eine .NET Framework Assembly oder eine Win32-Assembly enthält.

Geben Sie diese Datei für eine Win32-Assembly nicht als komponentenschlüsselpfad-Datei im KEYPATH-Feld der [Komponenten Tabelle](component-table.md)an.

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Datei \_ Anwendung
</dt> <dd>

Wenn Sie die Assembly an einem privaten Speicherort installieren möchten, geben Sie die Schlüssel Pfad Datei für die Assemblykomponente in dieses Feld ein.

Dies ist der Wert, der im Feld KEYPATH der [Komponenten Tabelle](component-table.md)angezeigt wird. Das Installationsprogramm kann dann die Assembly in der Verzeichnisstruktur der in der [Verzeichnis Tabelle](directory-table.md)angegebenen Komponente installieren. Dieses Feld muss NULL sein, wenn die Assembly im globalen Assemblycache installiert werden soll.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Geben Sie einen Wert von 1 (eins) für eine Win32-Assembly ein. Geben Sie für eine .NET Framework Assembly den Wert 0 (null) ein.

Wenn die Attribut Spalte NULL ist, behandelt das Installationsprogramm die Assembly als .NET Framework Assembly.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn mindestens ein Eintrag in der MsiAssembly-Tabelle vorhanden ist, muss die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) die [msipublishassemblyaktion](msipublishassemblies-action.md)und die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md)enthalten.

Da für-Assemblys nach dem Commit kein Rollback ausgeführt werden kann, wird in Windows Installer ein zweistufiger Installationsvorgang verwendet. Die Schnittstellen zu den Assemblys werden während der Installations Vorgänge erstellt, die von der [msipublishassemblyaktion](msipublishassemblies-action.md)generiert werden.

Die Assemblys werden erst nach erfolgreicher Ausführung der [InstallFinalize-Aktion](installfinalize-action.md)committet. Dies bedeutet Folgendes: Wenn Sie eine benutzerdefinierte Aktion oder Ressource erstellen, die von der Assembly abhängig ist, muss Sie nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden. Wenn Sie z. b. einen Dienst starten müssen, der von einer Assembly im globalen Assemblycache (GAC) abhängt, müssen Sie den Start des Dienstanbieter nach der [InstallFinalize-Aktion](installfinalize-action.md)planen. Dies bedeutet, dass Sie die [ServiceControl-Tabelle](servicecontrol-table.md) nicht verwenden können, um den Dienst zu starten. stattdessen müssen Sie eine benutzerdefinierte Aktion verwenden, die nach InstallFinalize sequenziert wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
