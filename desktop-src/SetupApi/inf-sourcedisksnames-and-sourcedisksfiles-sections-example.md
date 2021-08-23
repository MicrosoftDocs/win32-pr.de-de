---
description: Im Abschnitt SourceDisksNames einer INF-Datei werden die Datenträger identifiziert, die die installierten Quelldateien enthalten.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: INF SourceDisksNames and SourceDisksFiles Sections Example
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00eb8241b8e290f5460cc41b233d3b199df35e709d6e32f2c5a39925a79f851d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739410"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>INF SourceDisksNames and SourceDisksFiles Sections Example

Im Abschnitt **SourceDisksNames** einer INF-Datei werden die Datenträger identifiziert, die die installierten Quelldateien enthalten. Im Abschnitt **SourceDisksFiles** werden die Quelldateien und die Quelldatenträger identifiziert, die sie enthalten. Beachten Sie, dass MIPS-, Alpha- und PPC-Plattformen von Windows 2000 oder Windows XP nicht unterstützt werden.

Ab Windows XP können im Abschnitt **SourceDisksNames** ein Tag und eine Cab-Datei angegeben werden. Beispielsweise kann der folgende **SourceDisksNames-Abschnitt** mit Wechselmedien oder festen Medien verwendet werden. Bei Verwendung von Wechselmedien überprüft der Beispielabschnitt das Vorhandensein der Medien, indem zuerst überprüft wird, ob das Tag vorhanden ist. Bei Verwendung fester Medien überprüft der Beispielabschnitt das Vorhandensein der Medien, indem zuerst überprüft wird, ob das Gehäuse vorhanden ist. Nachdem das Vorhandensein eines Schränks überprüft wurde, versucht das System, Dateien aus dem Gehäuse zu kopieren, und fordert alle Dateien auf, die nicht kopiert werden konnten.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Weitere Informationen zu **SourceDisksNames** oder **SourceDisksFiles** finden Sie im Microsoft Windows 2000 Driver Development Kit in den Abschnitten "Allgemeine Richtlinien für INF-Dateien" und "INF-Dateiabschnitte und -Direktiven".

 

 



