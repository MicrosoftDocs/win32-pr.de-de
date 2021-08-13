---
title: Speichern der Präprozessorausgabe
description: Das Anzeigen der Präprozessorausgabe kann eine effektive Problembehandlungsmethode sein, z. B. wenn eine ungültige IDL-, C- oder C-Präprozessorsyntax auftritt oder wenn falsche -D-Werte in der MIDL-Befehlszeile dazu führen, dass MIDL arcane Fehler meldet.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL-Compiler MIDL, Speichern der Präprozessorausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f016885ac4d669d7b62eaf3ff1d5ee3154f03d5eae64fca5f63c6111dff4c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641375"
---
# <a name="saving-preprocessor-output"></a>Speichern der Präprozessorausgabe

Das Anzeigen der Präprozessorausgabe kann eine effektive Problembehandlungsmethode sein, z. B. wenn eine ungültige IDL-, C- oder C-Präprozessorsyntax auftritt oder wenn falsche -D-Werte in der MIDL-Befehlszeile dazu führen, dass MIDL arcane Fehler meldet. Entwickler möchten möglicherweise auch die Präprozessorausgabe untersuchen, um zu bestimmen, welche Dateien und Definitionen im Compilereingabestream vorhanden waren, z. B. wenn ein schwieriger Fall von Typredefinitionskonflikt gelöst werden muss. Oder weniger häufig möchten bestimmte Entwickler private Switches auf dem Präprozessor mit [**/cpp \_ opt**](-cpp-opt.md)erzwingen, oder sie möchten sehen, wie die Switches funktionieren.

Die einfachste und am wenigsten obtrusive Möglichkeit, die vorverarbeiteten Dateien aus einer MIDL-Kompilierungslauf abzurufen, ist die Verwendung des Schalters [**-savePP.**](-savepp.md) Der Schalter **-savePP** verhindert einfach, dass MIDL die temporären Dateien löscht, die der Präprozessor an MIDL zurückgibt. Beachten Sie Folgendes:

**midl -savePP -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 -Oicf -env win32 stub.idl**

Diese Anweisung kompiliert Stub.idl, behält jedoch alle Präprozessordateien bei.

> [!Note]  
> MIDL führt separate Präprozessorläufe für IDL- und ACF-Dateien (sofern vorhanden) sowie für jede importierte Datei aus.

 

Bei einer DCOM-Kompilierung werden in der Regel mehrere Präprozessordateien erstellt, obwohl sie von MIDL als virtueller zusammenhängender Eingabestream verarbeitet werden. In einer typischen Windows Programmierumgebung befinden sich die temporären Dateien im Verzeichnis Temp als Dateinamen wie MID \* .tmp. Wenn Sie die Präprozessorausgabe beibehalten, sollten Sie im Verzeichnis Temp nach zuletzt verwendeten Dateien suchen, um zu ermitteln, welche Dateien welchem Präprozessor zugeordnet sind.

In einfachen Fällen, z. B. wenn die kompilierte IDL-Datei keine anderen Dateien direkt oder indirekt importiert, oder wenn die Datei der obersten Ebene untersucht wird, kann der Präprozessor direkt aufgerufen werden. Die direkte Ausführung des C/C++-Präprozessors kann Fehler erkennen, die von MIDL maskiert oder verwechselt werden. Beispielsweise können die folgenden beiden Präprozessorbefehlszeilen für die zuvor in Anführungszeichen angegebene MIDL-Zeile verwendet werden:

**cl /E /nologo -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 stub.idl > stub.pp**

**cl /E /P -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1 stub.idl**

Im ersten dieser beiden Beispiele sind **/E** [**/nologo**](-nologo.md) die Schalter, die MIDL beim Aufrufen des Präprozessors hinzufügt. Die Präprozessorausgabe wird an stdout (der Bildschirm) gesendet und erfordert daher eine Umleitung zu einer Datei zur Untersuchung. Im zweiten dieser Beispiele weist **/P** den Präprozessor an, die Ausgabe an eine \* .i-Datei umzuleiten. In diesem Fall wird eine Stub.i-Datei im aktuellen Verzeichnis erstellt.

Der [**/cpp \_ opt-Schalter**](-cpp-opt.md) kann auch verwendet werden, um eine vorverarbeitete Datei abzurufen, ist jedoch schwierig und für die zuvor erwähnten Methoden schwierig und schwierig. Im folgenden Beispiel wird auch eine Stub.i-Datei erstellt, wie im vorherigen Beispiel. Die Anführungszeichen im folgenden Beispiel sind von entscheidender Bedeutung:

**Midl -Oicf -win32 -cpp \_ opt "/E /P -Id: \\ nt public sdk inc \\ \\ \\ -DNTENV=1" stub.idl**

 

 




