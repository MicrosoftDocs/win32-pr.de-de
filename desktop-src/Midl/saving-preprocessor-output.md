---
title: Speichern der Präprozessorausgabe
description: Das Anzeigen der Präprozessorausgabe kann eine effektive Methode zur Problembehandlung sein, z. b. Wenn eine ungültige IDL-, c-oder c-präprozessorsyntax auftritt oder wenn gefälschte-D-Werte in der Mittell-Befehlszeile zu einem Fehler in der Mittell melden.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- Mittlerer l-compilermittell, Speichern der Präprozessorausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388424"
---
# <a name="saving-preprocessor-output"></a>Speichern der Präprozessorausgabe

Das Anzeigen der Präprozessorausgabe kann eine effektive Methode zur Problembehandlung sein, z. b. Wenn eine ungültige IDL-, c-oder c-präprozessorsyntax auftritt oder wenn gefälschte-D-Werte in der Mittell-Befehlszeile zu einem Fehler in der Mittell melden. Entwickler können auch die Präprozessorausgabe überprüfen, um zu bestimmen, welche Dateien und Definitionen im compilereingabestream vorhanden waren, z. b. Wenn ein schwieriger Fall des Konflikts mit der Typneudefinition aufgelöst werden muss. Oder seltener möchten bestimmte Entwickler möglicherweise private Switches für den Präprozessor mit [**/cpp \_ opt**](-cpp-opt.md)erzwingen, oder Sie möchten sehen, wie die Switches funktionieren.

Die einfachste und am wenigsten verborgene Methode zum Abrufen der vorverarbeiteten Dateien aus einer Mittell-Kompilierung ist die Verwendung des Schalters " [**-savepp**](-savepp.md) ". Mit dem Schalter " **-savepp** " wird verhindert, dass die temporären Dateien, die vom Präprozessor an die mittlere Zeit zurückgeleitet werden, von der Mitte gelöscht werden Beachten Sie Folgendes:

**Mittel l-savepp-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1-Oicf-ERV Win32 Stub. idl**

Diese Direktive kompiliert Stub. idl, behält aber alle präprozessordateien bei.

> [!Note]  
> In mittlerer l werden separate präprozessorausführungen für die IDL-und ACF-Datei (falls vorhanden) sowie für jede importierte Datei ausgeführt.

 

Bei einer DCOM-Kompilierung werden in der Regel mehrere präprozessordateien erstellt, auch wenn Sie von der mittleren l als virtueller zusammenhängender Eingabedaten Strom verarbeitet werden. In einer typischen Windows-Programmierumgebung befinden sich die temporären Dateien im temporären Verzeichnis als Dateinamen wie z \* . b. Mid. tmp. Wenn Sie die Präprozessorausgabe beibehalten, empfiehlt es sich, die aktuellen Dateien im Temp-Verzeichnis zu überwachen, um zu ermitteln, welche Dateien mit welcher präprozessorlaufzeit verknüpft sind.

In einfachen Fällen, z. b. wenn die kompilierte IDL-Datei keine anderen Dateien direkt oder indirekt importiert oder wenn die Datei der obersten Ebene untersucht wird, kann der Präprozessor direkt aufgerufen werden. Wenn Sie den C/C++-Präprozessor direkt ausführen, können Fehler angezeigt werden, die durch die mittlere Die folgenden beiden präprozessorbefehlszeilen können z. b. für die oben genannte Mittel l-Zeile verwendet werden:

**cl/E/nologo-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1 Stub. idl > Stub. PP**

**cl/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1 Stub. idl**

In den ersten beiden Beispielen sind **/E** [**/nologo**](-nologo.md) die Schalter, die von der mittleren l beim Aufrufen des Präprozessors hinzugefügt werden. Die Präprozessorausgabe wird an stdout (der Bildschirm) gesendet und erfordert daher eine Umleitung zu einer Datei zur Überprüfung. Im zweiten dieser Beispiele weist **/P** den Präprozessor an, die Ausgabe an eine. i-Datei umzuleiten. \* in diesem Fall würde eine Datei "Stub. i" im aktuellen Verzeichnis erstellt.

Der Schalter " [**/cpp \_ opt**](-cpp-opt.md) " kann auch verwendet werden, um eine vorverarbeitete Datei abzurufen, aber die zuvor erwähnten Methoden sind schwierig und untergeordnet. Im folgenden Beispiel wird auch eine Stub. i-Datei erstellt, wie im vorherigen Beispiel gezeigt. Die Anführungszeichen im folgenden Beispiel sind erforderlich:

**Mittel l-Oicf-Win32-cpp \_ Opt "/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1" Stub. idl**

 

 




