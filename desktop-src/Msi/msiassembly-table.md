---
description: Die MsiAssembly-Tabelle gibt Windows Installer-Einstellungen für Microsoft .NET Framework Assemblys und Win32-Assemblys an. Weitere Informationen finden Sie unter Installation von Assemblys im globalen Assemblycache und Installation von Win32-Assemblys.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: MsiAssembly-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda246bd6baba75d0f7e8d53f515a25abb0c163c2d3ef0b1b9705c123b8e69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381380"
---
# <a name="msiassembly-table"></a>MsiAssembly-Tabelle

Die MsiAssembly-Tabelle gibt Windows Installer-Einstellungen für Microsoft .NET Framework Assemblys und Win32-Assemblys an. Weitere Informationen finden Sie unter [Installation von Assemblys im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installation von Win32-Assemblys.](installation-of-win32-assemblies.md)

Auf Windows XP kann Windows Installer Win32-Assemblys als [side-by-side-Assemblys installieren.](side-by-side-assemblies.md) Weitere Informationen finden Sie unter [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).

**Windows 2000:** Dieses Feature wird nicht unterstützt.

Die MsiAssembly-Tabelle enthält die folgenden Spalten.



| Spalte            | Typ                         | Key | Nullwerte zulässig |
|-------------------|------------------------------|-----|----------|
| Komponente\_       | [Identifier](identifier.md) | J   | N        |
| Komponente\_         | [Identifier](identifier.md) | N   | N        |
| \_Dateimanifest    | [Identifier](identifier.md) | N   | J        |
| \_Dateianwendung | [Identifier](identifier.md) | N   | J        |
| Attribute        | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Der Schlüssel in der [Komponententabelle,](component-table.md) der die Windows Installer-Komponente angibt, die diese Assembly enthält.

Der Wert in diesem Feld darf nicht auf NULL festgelegt werden. Das KeyPath-Feld der Komponente in der [Komponententabelle](component-table.md) darf nicht NULL sein.

Bei Win32-Assemblys kann die Komponente KeyPath nicht die Manifestdatei sein, die im Dateimanifest angegeben \_ ist. Das Manifest kann der Schlüsselpfad für eine .NET Framework- oder Richtlinien-Assembly sein.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_
</dt> <dd>

Geben Sie den Schlüssel in [die Featuretabelle ein.](feature-table.md)

Wenn die Assembly von einer Featureinstallation installiert werden muss, installiert Windows Installer das Feature, auf das dieses Feld verweist.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>\_Dateimanifest
</dt> <dd>

Ein externer Schlüssel in der [Dateitabelle,](file-table.md) der die Datei angibt, die das Manifest für eine .NET Framework oder Win32-Assembly enthält.

Geben Sie für eine Win32-Assembly diese Datei nicht als Komponentenschlüsselpfaddatei im Feld KeyPath der [Komponententabelle an.](component-table.md)

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>\_Dateianwendung
</dt> <dd>

Um die Assembly an einem privaten Speicherort zu installieren, geben Sie die Schlüsselpfaddatei für die Assemblykomponente in dieses Feld ein.

Dies ist der Wert, der im Feld KeyPath der [Komponententabelle angezeigt wird.](component-table.md) Der Installer kann dann die Assembly in der Verzeichnisstruktur der Komponente installieren, die in der [Verzeichnistabelle angegeben ist.](directory-table.md) Dieses Feld muss NULL sein, wenn die Assembly im globalen Assemblycache installiert werden soll.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Geben Sie den Wert 1 (eins) für eine Win32-Assembly ein. Geben Sie den Wert 0 (null) für eine .NET Framework ein.

Wenn die Spalte Attribute NULL ist, behandelt der Installer die Assembly als .NET Framework Assembly.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn mindestens ein Eintrag in der MsiAssembly-Tabelle enthalten ist, muss die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) die [MsiPublishAssemblies-Aktion](msipublishassemblies-action.md)und die [MsiUnpublishAssemblies-Aktion enthalten.](msiunpublishassemblies-action.md)

Da assemblys nach dem Ausführen eines Committeds kein Rollback ausführen können, verwendet Windows Installer einen zweistufigen Installationsvorgang. Die Schnittstellen zu den Assemblys werden während der Installationsvorgänge erstellt, die von der [MsiPublishAssemblies-Aktion generiert werden.](msipublishassemblies-action.md)

Für die Assemblys wird erst dann ein Committed ausgeführt, wenn die [InstallFinalize-Aktion erfolgreich ausgeführt wurde.](installfinalize-action.md) Wenn Sie also eine benutzerdefinierte Aktion oder Ressource erstellen, die auf der Assembly basiert, muss sie nach der [InstallFinalize-Aktion sequenziert werden.](installfinalize-action.md) Wenn Sie beispielsweise einen Dienst starten müssen, der von einer Assembly im globalen Assemblycache (GAC) abhängt, müssen Sie den Start dieses Diensts nach der [InstallFinalize-Aktion planen.](installfinalize-action.md) Dies bedeutet, dass Sie die [ServiceControl-Tabelle](servicecontrol-table.md) nicht verwenden können, um den Dienst zu starten. Stattdessen müssen Sie eine benutzerdefinierte Aktion verwenden, die nach InstallFinalize sequenziert wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
