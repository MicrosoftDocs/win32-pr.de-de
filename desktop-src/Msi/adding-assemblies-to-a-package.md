---
description: Windows Installer-Entwickler können die Richtlinien in diesem Thema verwenden, um Windows Installer-Pakete zu erstellen, die Assemblys enthalten.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Hinzufügen von Assemblys zu einem Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a96c1b8c8d9b73fedf03fceeb82be62b8457556da02334ed7a224aefc2202a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534870"
---
# <a name="adding-assemblies-to-a-package"></a>Hinzufügen von Assemblys zu einem Paket

Windows Installer-Entwickler können die Richtlinien in diesem Thema verwenden, um Windows Installer-Pakete zu erstellen, die Assemblys enthalten.

Die folgenden Richtlinien gelten für Win32-Assemblys und -Assemblys, die von der Common Language Runtime des Microsoft-.NET Framework werden.

-   Eine Windows Installer-Komponente sollte nicht mehr als eine Assembly enthalten.
-   Alle Dateien in der Assembly sollten in einer einzelnen Komponente enthalten sein.
-   Jede Komponente, die eine Assembly enthält, sollte über einen Eintrag in der [MsiAssembly-Tabelle](msiassembly-table.md) verfügen.
-   Der starke Assemblycachename jeder Assembly sollte in der [MsiAssemblyName-Tabelle erstellt](msiassemblyname-table.md) werden.
-   Verwenden Sie [die Tabelle Registry](registry-table.md) anstelle der Tabelle [Class,](class-table.md) wenn Sie COM Interop für eine Assembly registrieren.
-   Assemblys mit demselben starken Namen sind dieselbe Assembly. Wenn dieselbe Assembly von verschiedenen Anwendungen installiert wird, sollten die Komponenten, die die Assembly enthalten, den gleichen Wert für componentId in ihren [Komponententabellen](component-table.md) verwenden.

> [!Note]  
> Produktanzeigen identifizieren Assemblys, die von verschiedenen Anwendungen installiert und verwendet werden können. Produktan ankündigungen identifizieren keine privaten Assemblys.

 

## <a name="adding-win32-assemblies"></a>Hinzufügen von Win32-Assemblys

Befolgen Sie die folgenden Richtlinien, wenn Sie Win32-Assemblys verwenden:

-   Der KeyPath-Wert in der [Component-Tabelle](component-table.md) für eine Komponente, die eine Win32-Assembly enthält, sollte nicht NULL sein.
-   Der KeyPath-Wert in der [Component-Tabelle](component-table.md) für eine Komponente, die eine Win32-Richtlinien-Assembly enthält, sollte die Manifestdatei sein.
-   Der KeyPath-Wert in der [Component-Tabelle](component-table.md) für eine Komponente, die eine Win32-Assembly enthält, die keine Richtlinien-Assembly ist, darf nicht die Manifestdatei oder Katalogdatei sein. Es sollte eine andere Datei in der Assembly sein.
-   Fügen Sie der [Tabelle MsiAssemblyName](msiassemblyname-table.md) für jedes Name-Wert-Paar, das im Abschnitt **assemblyIdentity** des Manifests der Win32-Assembly aufgeführt ist, eine Zeile hinzu.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Hinzufügen von Assemblys, die mit dem -.NET Framework

Verwenden Sie die folgenden Richtlinien, wenn Sie Assemblys, die von der Common Language Runtime des -.NET Framework verwendet werden, verwenden.

-   Der KeyPath-Wert in der [Component-Tabelle](component-table.md) für eine Komponente, die die Assembly enthält, sollte nicht NULL sein.
-   Wenn Sie eine von der Common Language Runtime verwendete Assembly im globalen Assemblycache installieren, muss der Wert in der Spalte Dateianwendung der \_ MsiAssembly-Tabelle NULL sein.
-   Fügen Sie der [Tabelle MsiAssemblyName](msiassemblyname-table.md) für jedes Attribut des starken Namens der Assembly eine Zeile hinzu. Alle Assemblys müssen über die Attribute Name, Version und Culture verfügen, die in der MsiAssemblyName-Tabelle angegeben sind. Für eine globale Assembly ist ein publicKeyToken-Attribut erforderlich. Die folgende Tabelle ist ein Beispiel für die MsiAssemblyName-Tabelle für eine globale Assembly zur Verwendung durch die Common Language Runtime.

[MsiAssemblyName-Tabelle](msiassemblyname-table.md)



| Komponente  | Name           | Wert            |
|------------|----------------|------------------|
| ComponentA | Name           | Einfach           |
| ComponentA | version        | 1.0.0.0          |
| ComponentA | culture        | Neutral          |
| ComponentA | Publickeytoken | 9d1ec8380f483f5a |



 

 

 



