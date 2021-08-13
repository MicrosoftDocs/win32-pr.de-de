---
description: ICE57 überprüft, ob einzelne Komponenten nicht computer- und benutzerspezifische Daten mischen. Diese benutzerdefinierte ICE-Aktion überprüft Registrierungseinträge, Dateien, Verzeichnisschlüsselpfade und nicht angekündigte Verknüpfungen.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d875264ed1fbc0f7dedac863c21801e5180ae879c9c255af7cf4b36e5d402970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635161"
---
# <a name="ice57"></a>ICE57

ICE57 überprüft, ob einzelne Komponenten nicht computer- und benutzerspezifische Daten mischen. Diese benutzerdefinierte ICE-Aktion überprüft Registrierungseinträge, Dateien, Verzeichnisschlüsselpfade und nicht angekündigte Verknüpfungen.

Das Kombinieren von Benutzer- und Computerdaten in derselben Komponente kann zu einer nur teilweisen Installation der Komponente für einige Benutzer in einer Umgebung mit mehreren Benutzern führen.

Weitere Informationen finden Sie in der [**ALLUSERS-Eigenschaft.**](allusers.md)

## <a name="result"></a>Ergebnis

ICE57 gibt einen Fehler aus, wenn eine Komponente gefunden wird, die sowohl Computer- als auch Benutzerregistrierungseinträge, Dateien, Verzeichnisschlüsselpfade oder nicht angekündigte Verknüpfungen enthält.

## <a name="example"></a>Beispiel

ICE57 gibt die folgenden Fehler für das gezeigte Beispiel an.

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

[Komponententabelle](component-table.md) (teilweise)



| Komponente  | Verzeichnis  | Attribute | KeyPath |
|------------|------------|------------|---------|
| Komponente1 | DirectoryA | 0          | Filea   |
| Component2 | DirectoryA | 4          | RegKeyB |
| Component3 | DirectoryA | 0          | FileC   |
| Komponente4 | DirectoryA | 4          | RegKeyD |



 

[Registrierungstabelle](registry-table.md) (partiell)



| Registrierung | Root | Komponente\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Komponente1  |
| RegKeyB  | 1    | Component2  |
| RegKeyC  | -1   | Component3  |
| RegKeyD  | -1   | Komponente4  |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | Komponente\_ |
|-------|-------------|
| Filea | Komponente1  |
| Fileb | Component2  |
| FileC | Component3  |
| Abgelegt | Komponente4  |



 

[Verzeichnistabelle](directory-table.md)



| Verzeichnis  | \_Übergeordnetes Verzeichnis | DefaultDir |
|------------|-------------------|------------|
| Targetdir  |                   | SourceDir  |
| DirectoryA | Targetdir         | DirectoryA |



 

Um die Fehler zu beheben, organisieren Sie die Anwendung so, dass jede Komponente nur Benutzer- oder Computerressourcen und nicht beide enthält.

Die erste Fehlermeldung wird gesendet, da Component1 FileA (pro Computer) und den HKCU-Registrierungsschlüssel RegKeyA (pro Benutzer) enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



