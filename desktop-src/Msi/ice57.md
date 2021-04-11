---
description: ICE57 überprüft, ob einzelne Komponenten nicht Computer-und benutzerspezifische Daten kombinieren. Diese benutzerdefinierte Ice-Aktion überprüft Registrierungseinträge, Dateien, Verzeichnis Schlüssel Pfade und nicht angekündigte Verknüpfungen.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217351"
---
# <a name="ice57"></a>ICE57

ICE57 überprüft, ob einzelne Komponenten nicht Computer-und benutzerspezifische Daten kombinieren. Diese benutzerdefinierte Ice-Aktion überprüft Registrierungseinträge, Dateien, Verzeichnis Schlüssel Pfade und nicht angekündigte Verknüpfungen.

Das Kombinieren von Benutzer-und computerspezifischen Daten in der gleichen Komponente kann dazu führen, dass die Komponente für einige Benutzer in einer Umgebung mit mehreren Benutzern nur teilweise installiert wird.

Siehe die Eigenschaft " [**ALLUSERS**](allusers.md) ".

## <a name="result"></a>Ergebnis

ICE57 gibt einen Fehler aus, wenn eine Komponente gefunden wird, die sowohl Computer-als auch benutzerspezifische Registrierungseinträge, Dateien, Verzeichnis Schlüssel Pfade oder nicht angekündigte Verknüpfungen enthält.

## <a name="example"></a>Beispiel

ICE57reports die folgenden Fehler für das gezeigte Beispiel.

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

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | Verzeichnis  | Attribute | KEYPATH |
|------------|------------|------------|---------|
| Component1 | Directoren | 0          | Mit der   |
| Component2 | Directoren | 4          | Regkeyb |
| Component3 | Directoren | 0          | Filec   |
| Component4 | Directoren | 4          | Regkeyd |



 

[Registrierungs Tabelle](registry-table.md) (partiell)



| Registrierung | Root | Komponente\_ |
|----------|------|-------------|
| Regkeya  | 1    | Component1  |
| Regkeyb  | 1    | Component2  |
| Regkeyc  | -1   | Component3  |
| Regkeyd  | -1   | Component4  |



 

[Dateitabelle](file-table.md) (partiell)



| File  | Komponente\_ |
|-------|-------------|
| Mit der | Component1  |
| FileB | Component2  |
| Filec | Component3  |
| Fassung | Component4  |



 

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis  | Über \_ geordnetes Verzeichnis | DefaultDir |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| Directoren | TARGETDIR         | Directoren |



 

Um die Fehler zu beheben, müssen Sie die Anwendung so neu organisieren, dass jede Komponente nur Benutzer-oder Computer spezifische Ressourcen und nicht beides enthält.

Die erste Fehlermeldung wird gepostet, weil Component1 die Datei (pro Computer) und den HKCU-Registrierungsschlüssel regkeya (pro Benutzer) enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



