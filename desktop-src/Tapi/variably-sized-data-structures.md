---
description: Wenn Datenstrukturen mit variabler Größen Verwendung zum Übertragen von Informationen zwischen TAPI und der Anwendung verwendet werden, ist die Anwendung dafür verantwortlich, den erforderlichen Arbeitsspeicher zuzuordnen.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Datenstrukturen mit variabler Größenanpassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217751"
---
# <a name="variably-sized-data-structures"></a>Datenstrukturen mit variabler Größenanpassung

Wenn Datenstrukturen mit variabler Größen Verwendung zum Übertragen von Informationen zwischen TAPI und der Anwendung verwendet werden, ist die Anwendung dafür verantwortlich, den erforderlichen Arbeitsspeicher zuzuordnen. Der zugewiesene Arbeitsspeicher muss für den festgelegten Teil der Datenstruktur mindestens groß genug sein, und er wird von der Anwendung im **dwtotalsize** -Member der Datenstruktur festgelegt. Die **dwusedsize** -und **dwneeddsize** -Elemente werden von TAPI ausgefüllt. Wenn **dwtotalsize** kleiner als die Größe des fixierten Teils ist, wird lineerr/phoneerr \_ structureumosmall zurückgegeben. Wenn eine Funktion Erfolg zurückgibt, wurden alle Felder im Fixed-Teil ausgefüllt. Die Member **dwusedsize** und **dwneedebug** können verglichen werden, um zu bestimmen, ob alle Variablen Teile ausgefüllt wurden und wie viel Speicherplatz erforderlich ist, um alle Elemente auszufüllen.

Wenn **dwneeendsize** gleich **dwusedsize** ist, wurden alle fixierten und Variablen Teile ausgefüllt. Wenn **dwneeundsize** größer als **dwusedsize** ist, wurden möglicherweise einige Variablen Teile ausgefüllt, aber genau, welche Felder mit variabler Größe eingegeben wurden, ist nicht definiert. Es wird nie ein Variablen Teil abgeschnitten, und Variablen Teile, die aufgrund von unzureichendem Speicherplatz abgeschnitten wurden, werden angezeigt, wenn beide der entsprechenden Teile "Offset" und "size" auf NULL festgelegt sind. Wenn diese nicht gleich NULL sind (und kein Fehler zurückgegeben wurde), geben Sie den Offset und die Größe gültiger, nicht abgeschnittener Variablen Teil Daten an.

Eine Anwendung kann immer gewährleisten, dass alle Variablen Teile ausgefüllt werden, indem Sie für die Struktur die **dwneededsize** -Bytes zuordnen und angeben und die Get-Funktion erneut aufrufen, bis die Funktion Success zurückgibt und **dwneededsize** gleich **dwusedsize** ist. Dies sollte beim zweiten Versuch vorkommen, außer bei Racebedingungen, die Änderungen an der Größe der Variablen Teile zwischen den Aufrufen bewirken, die selten vorkommen sollten.

> [!Note]  
> Alle Text Zeichenfolgen, unabhängig von der Codierung, in Strukturen mit variabler Größe sollten gemäß den normalen C-Zeichen folgen Behandlungs Konventionen auf **null** enden.

 

 

 



