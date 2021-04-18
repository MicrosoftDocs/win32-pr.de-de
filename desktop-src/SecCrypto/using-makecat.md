---
description: Erstellt eine nicht signierte Katalog Datei, in der die Hashwerte eines Satzes von Dateien zusammen mit zugeordneten Attributen der einzelnen Dateien im Satz enthalten sind. Eine Katalog Datei ermöglicht dem Benutzer, eine Datei (den Katalog) zu signieren, anstatt zahlreiche einzelne Dateien zu signieren.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Verwenden von MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345180"
---
# <a name="using-makecat"></a>Verwenden von MakeCat

Das [MakeCat](makecat.md) -Tool erstellt eine nicht signierte Katalog Datei, die [*die Hashwerte eines Satzes*](../secgloss/h-gly.md) von Dateien zusammen mit zugeordneten Attributen der einzelnen Dateien in der Gruppe enthält. Eine Katalog Datei ermöglicht dem Benutzer, eine Datei (den Katalog) zu signieren, anstatt zahlreiche einzelne Dateien zu signieren.

Nachdem die nicht signierte Katalog Datei signiert und übertragen wurde, kann der Empfänger die Hashwerte der ursprünglichen Dateien mit den Hashes in der Katalog Datei vergleichen und sicherstellen, dass die Dateien nicht manipuliert sind.

Vor der Verwendung des [MakeCat](makecat.md) -Tools muss der Benutzer eine Katalog Definitionsdatei (. CDF) mithilfe eines beliebigen Text-Editors vorbereiten. Die CDF-Datei enthält die Liste der Dateien und die Attribute der zu katalogigenden Dateien (die Spezifikationen sind unten aufgeführt). Das MakeCat-Tool scannt die CDF-Datei, überprüft die Liste der Attribute der einzelnen aufgelisteten Dateien, fügt die aufgelisteten Attribute dem Katalog selbst hinzu, erstellt Hashwerte für jede der aufgelisteten Dateien und speichert die Hashes der einzelnen Dateien in der Katalog Datei. Jede Datei enthält den Hash und die Attribute, die separat im Katalog gespeichert werden. Diese Katalog Datei kann dann signiert und übertragen werden. Der Empfänger kann anschließend den Hash der einzelnen Dateien im Katalog mit dem Hash der ursprünglichen Dateien vergleichen, um zu beweisen, dass der ursprüngliche Inhalt nicht manipuliert werden kann. MakeCat ändert die CDF-Datei nicht.

In den folgenden Beispielen werden [MakeCat](makecat.md) -Befehle verwendet.

-   Generieren Sie eine Katalog Datei aus der Datei Good. CDF.

    **MakeCat-v Good. CDF**

Eine Datei, "Good. CDF", erzeugt eine Katalog Datei (Good.cat), indem Sie die Dateien UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, unsigned. Class und SignedPE.exe. Die analysierten Dateien, zusammen mit "Good. CDF" und der neu generierten Good.cat, befinden sich alle im selben Verzeichnis.

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> Der letzte Eintrag in der CDF-Datei muss immer über ein explizites Zeilen Trennzeichen am Ende der Zeile verfügen.

 

 

 
