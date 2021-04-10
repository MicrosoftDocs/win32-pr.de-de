---
description: Windows Installer Entwickler die Richtlinien in diesem Thema verwenden können, um Windows Installer Pakete zu erstellen, die Assemblys enthalten.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Hinzufügen von Assemblys zu Paketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215727"
---
# <a name="adding-assemblies-to-a-package"></a>Hinzufügen von Assemblys zu Paketen

Windows Installer Entwickler die Richtlinien in diesem Thema verwenden können, um Windows Installer Pakete zu erstellen, die Assemblys enthalten.

Die folgenden Richtlinien gelten für Win32-Assemblys und Assemblys, die die Common Language Runtime des Microsoft .NET Frameworks verwendet.

-   Eine Windows Installer Komponente sollte nicht mehr als eine Assembly enthalten.
-   Alle Dateien in der Assembly sollten sich in einer einzelnen Komponente befinden.
-   Jede Komponente, die eine Assembly enthält, muss über einen Eintrag in der [MsiAssembly](msiassembly-table.md) -Tabelle verfügen.
-   Der Name der starken Assemblycaches der einzelnen Assemblys sollte in der [MsiAssemblyName](msiassemblyname-table.md) -Tabelle erstellt werden.
-   Verwenden Sie die [Registrierungs](registry-table.md) Tabelle anstelle der [Klassen](class-table.md) Tabelle, wenn Sie COM-Interop für eine Assembly registrieren.
-   Assemblys mit demselben starken Namen sind dieselbe Assembly. Wenn dieselbe Assembly von verschiedenen Anwendungen installiert wird, sollten die Komponenten, die die Assembly enthalten, den gleichen Wert für die ComponentID in Ihren [Komponenten](component-table.md) Tabellen verwenden.

> [!Note]  
> Produktankündigungen identifizieren Assemblys, die von verschiedenen Anwendungen installiert und verwendet werden können. Produktankündigungen identifizieren keine privaten Assemblys.

 

## <a name="adding-win32-assemblies"></a>Win32-Assemblys

Beachten Sie beim Einschließen von Win32-Assemblys die folgenden Richtlinien:

-   Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die eine Win32-Assembly enthält, darf nicht NULL sein.
-   Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die eine Win32-Richtlinienassembly enthält, sollte die Manifest-Datei sein.
-   Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die eine Win32-Assembly enthält, bei der es sich nicht um eine Richtlinienassembly handelt, sollte nicht die Manifestressource oder die Katalog Datei sein Dies sollte eine andere Datei in der Assembly sein.
-   Fügen Sie der [MsiAssemblyName](msiassemblyname-table.md) -Tabelle für jedes Name-Wert-Paar, das im Abschnitt " **assemblyIdentity" des Win32-Assemblymanifests** aufgeführt ist, eine Zeile hinzu.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Hinzufügen von mit dem .NET Framework verwendeten Assemblys

Verwenden Sie die folgenden Richtlinien, wenn Sie Assemblys einschließen, die die Common Language Runtime des .NET Framework verwendet.

-   Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die die Assembly enthält, darf nicht NULL sein.
-   Wenn Sie eine vom Common Language Runtime verwendete Assembly in den globalen Assemblycache installieren, muss der Wert in der Datei \_ Anwendungs Spalte der MsiAssembly-Tabelle den Wert NULL aufweisen.
-   Fügen Sie der Tabelle [MsiAssemblyName](msiassemblyname-table.md) für jedes Attribut des starken Namens der Assembly eine Zeile hinzu. Alle Assemblys müssen über die Attribute Name, Version und Culture verfügen, die in der Tabelle MsiAssemblyName angegeben sind. Ein PublicKeyToken-Attribut ist für eine globale Assembly erforderlich. Die folgende Tabelle ist ein Beispiel für die MsiAssemblyName-Tabelle für eine globale Assembly, die von der Common Language Runtime verwendet werden kann.

[MsiAssemblyName-Tabelle](msiassemblyname-table.md)



| Komponente  | Name           | Wert            |
|------------|----------------|------------------|
| Componenta | Name           | Einfach           |
| Componenta | version        | 1.0.0.0          |
| Componenta | Kultur        | Neutral          |
| Componenta | PublicKeyToken | 9d1ec8380b483-Dienst |



 

 

 



