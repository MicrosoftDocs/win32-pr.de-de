---
description: Im Abschnitt "SourceDisksNames" einer INF-Datei werden die Datenträger identifiziert, die die zu installierenden Quelldateien enthalten.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: INF SourceDisksNames-und SourceDisksFiles-Abschnitte (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349986"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>INF SourceDisksNames-und SourceDisksFiles-Abschnitte (Beispiel)

Im Abschnitt " **SourceDisksNames** " einer INF-Datei werden die Datenträger identifiziert, die die zu installierenden Quelldateien enthalten. Der Abschnitt **SourceDisksFiles** identifiziert die Quelldateien und die Quell Datenträger, die Sie enthalten. Beachten Sie, dass die Plattformen mips, Alpha und PPC von Windows 2000 oder Windows XP nicht unterstützt werden.

Ab Windows XP kann ein **SourceDisksNames** -Abschnitt ein Tag und eine CAB-Datei angeben. Der folgende **SourceDisksNames** -Abschnitt kann z. b. für Wechsel Datenträger oder ein festes Medium verwendet werden. Wenn Sie Wechselmedien verwenden, überprüft der Beispiel Abschnitt, ob das Medium vorhanden ist, indem zuerst überprüft wird, ob das-Tag vorhanden ist. Wenn Sie ein festes Medium verwenden, überprüft der Beispiel Abschnitt, ob die Medien vorhanden sind, indem zuerst überprüft wird, ob die CAB-Anwendung vorhanden ist. Nachdem das vorhanden sein einer CAB-Datei überprüft wurde, versucht das System, Dateien aus der CAB-Datei zu kopieren, und fordert Sie zur Eingabe von Dateien auf, die nicht kopiert werden konnten.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Weitere Informationen zu **SourceDisksNames** oder **SourceDisksFiles** finden Sie in den Abschnitten "allgemeine Richtlinien für INF-Datei" und "INF-Datei Abschnitte und-Direktiven" des Microsoft Windows 2000 Driver Development Kit.

 

 



