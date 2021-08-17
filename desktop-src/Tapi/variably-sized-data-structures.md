---
description: Wenn Datenstrukturen mit unterschiedlicher Größe zum Übertragen von Informationen zwischen TAPI und der Anwendung verwendet werden, ist die Anwendung für die Zuweisung des erforderlichen Arbeitsspeichers verantwortlich.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Variabel dimensionierte Datenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182e349079abbce93f533b1b6cd299ab7e0e883d71e9b845dfdaf52bf0275ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760195"
---
# <a name="variably-sized-data-structures"></a>Variabel dimensionierte Datenstrukturen

Wenn Datenstrukturen mit unterschiedlicher Größe zum Übertragen von Informationen zwischen TAPI und der Anwendung verwendet werden, ist die Anwendung für die Zuweisung des erforderlichen Arbeitsspeichers verantwortlich. Der zugeordnete Arbeitsspeicher muss mindestens groß genug für den festen Teil der Datenstruktur sein und wird von der Anwendung im **dwTotalSize-Element** der Datenstruktur festgelegt. Die Elemente **dwUsedSize** und **dwNeededSize** werden von TAPI ausgefüllt. Wenn **dwTotalSize** kleiner als die Größe des festen Teils ist, wird LINEERR/PHONEERR \_ STRUCTURETOOSMALL zurückgegeben. Wenn eine Funktion erfolgreich zurückgegeben wird, wurden alle Felder im festen Teil ausgefüllt. Die Member **dwUsedSize** und **dwNeededSize** können verglichen werden, um zu bestimmen, ob alle Variablenteile ausgefüllt wurden und wie viel Speicherplatz erforderlich wäre, um sie alle aufzufüllen.

Wenn **dwNeededSize** gleich **dwUsedSize** ist, wurden alle festen und variablen Teile ausgefüllt. Wenn **dwNeededSize** größer als **dwUsedSize** ist, wurden möglicherweise einige variable Teile ausgefüllt, aber genau die Felder mit unterschiedlicher Größe sind nicht definiert. Es wird kein variabler Teil abgeschnitten, und variablen Teile, die aufgrund von unzureichendem Speicherplatz abgeschnitten worden wären, werden angezeigt, wenn beide entsprechenden Teile "Offset" und "Size" auf 0 (null) festgelegt sind. Wenn diese nicht beide null sind (und kein Fehler zurückgegeben wurde), geben sie den Offset und die Größe gültiger, nicht erfasster Variablenteildaten an.

Eine Anwendung kann immer garantieren, dass alle Variablenteile ausgefüllt werden, indem **dwNeededSize-Bytes** für die Struktur zugewiesen und angegeben werden und die Get-Funktion erneut aufgerufen wird, bis die Funktion erfolgreich zurückgegeben wird und **dwNeededSize** gleich **dwUsedSize** ist. Dies sollte beim zweiten Versuch geschehen, mit Ausnahme von Racebedingungen, die Änderungen an der Größe variabler Teile zwischen Aufrufen verursachen, die selten vorkommen sollten.

> [!Note]  
> Alle Textzeichenfolgen sollten unabhängig von der Codierung in Strukturen mit variabler Größe **NULL** sein und gemäß den normalen C-Konventionen zur Behandlung von Zeichenfolgen enden.

 

 

 



