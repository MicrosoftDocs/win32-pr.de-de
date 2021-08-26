---
title: Extrahieren der Codebeispiele
description: Obwohl die Codebeispiele in eine Reihe von Tutorial-Lektionen unterteilt sind, können die entsprechenden Beispielgruppierungen problemlos aus der Sammlung extrahiert werden.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67093f4cfbbfab2a3c1681462627f02b504124ed15d1483b9f9d91ec5551d0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034950"
---
# <a name="extracting-the-code-samples"></a>Extrahieren der Codebeispiele

Obwohl die Codebeispiele in eine Reihe von Tutorial-Lektionen unterteilt sind, können die entsprechenden Beispielgruppierungen problemlos aus der Sammlung extrahiert werden. Die meisten der einzelnen Beispielverzeichnisse sind für die Zusammenarbeit mit mindestens einem anderen Beispielverzeichnis vorgesehen. Die komponentenbezogenen Beispiele bestehen aus einem Client- und einem Serverpaar, wobei der Server die Verwendung des REGISTER-Beispielhilfsprogramms erfordert. Hier finden Sie eine Zusammenfassung der Beispielgruppierungen und wie jede Gruppe als bearbeitbare Einheit extrahiert wird. Kopieren Sie für jede Beispielgruppierung den Inhalt der angezeigten Verzeichnisse. Das \[ angezeigte übergeordnete \] Zielverzeichnis erfordert keinen Inhalt aus dem Branch samples. Bei den Hilfemenüs in den ausgeführten Beispielen wird jedoch davon ausgegangen, dass sich das entsprechende Tutorial .HTM Hilfedateien in diesem übergeordneten \[ \] Zielverzeichnis befindet.

Für die Win32 READTUT-Anwendung:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Für die Win32 EXE-Skeleton-Anwendung:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Für das Win32-DLL-Gerüst:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

Für die grundlegenden COM-Objektbeispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

Für die grundlegenden In-Process-DLL-Komponentenclient-/Serverbeispiele:

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

Für die Out-of-Process-Beispiele für lokale Clients/Server:

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

Für die Apartmentmodell-Client-/Serverbeispiele:

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

Für die DCOM-Client-/Serverbeispiele (Distributed COM):

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

Für die Kostenlosen Threading-Client-/Serverbeispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Für die Client-/Serverbeispiele für ein verbindungsfähiges COM-Objekt:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Für die Strukturierte Speicherclient-/Serverbeispiele:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Für die Client-/Serverbeispiele für persistente Objekte:

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

Für die DCOM-Sicherheitsclient-/Serverbeispiele:

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

 

 




