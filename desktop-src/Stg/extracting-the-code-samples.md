---
title: Extrahieren der Code Beispiele
description: Obwohl die Codebeispiele in eine Reihe von Tutorial-Lektionen aufgeteilt sind, können die entsprechenden Beispiel Gruppierungen problemlos aus der Auflistung extrahiert werden.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388176"
---
# <a name="extracting-the-code-samples"></a>Extrahieren der Code Beispiele

Obwohl die Codebeispiele in eine Reihe von Tutorial-Lektionen aufgeteilt sind, können die entsprechenden Beispiel Gruppierungen problemlos aus der Auflistung extrahiert werden. Die meisten der einzelnen Beispiel Verzeichnisse sind so konzipiert, dass Sie in Verbindung mit mindestens einem anderen Beispiel Verzeichnis funktionieren. Die Komponenten bezogenen Beispiele bestehen aus einem Client-und einem Server Paar, wobei der Server die Verwendung des Register Sample Utility erfordert. Im folgenden finden Sie eine Zusammenfassung der Beispiel Gruppierungen und die Vorgehensweise zum Extrahieren der einzelnen Gruppen als Erstell Bare Einheit. Kopieren Sie für jede Beispiel Gruppierung den Inhalt der angezeigten Verzeichnisse. Das \[ angezeigte übergeordnete Ziel \] Verzeichnis erfordert keinen Inhalt aus der Samples-Verzweigung. In den Menüs "Hilfe" in den laufenden Beispielen wird jedoch davon ausgegangen, dass das entsprechende Lernprogramm ausgeführt wird. HTM-Hilfedateien befinden sich in diesem übergeordneten \[ Ziel \] Verzeichnis.

Für die Win32-Anwendung "Read tut":

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Für die Win32-exe-Skeleton-Anwendung:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Für das Win32-DLL-Skelett:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

Für die grundlegenden com-Objekt Beispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

Für die grundlegenden Client/Server-Beispiele für die Prozess interne dll-Komponente:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Für die Client-/Serverbeispiele für lizenzierte Komponenten:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

Für die standardmäßigen Marshallingbeispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

Für die Beispiele für den lokalen Client/Server außerhalb des Prozesses:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

Für die Apartment Model-Client/Server-Beispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

Für die DCOM-Client/Server-Beispiele (verteiltes com):

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

Die Beispiele für die kostenlose Threading Client/Server:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Für die Verbindungs fähigen COM-Objekt Client/Server-Beispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Für die strukturierten Speicher Client/Server-Beispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Für die persistenten Objekt Client/Server-Beispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

Für die DCOM-Sicherheits Client/Server-Beispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




