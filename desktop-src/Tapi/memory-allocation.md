---
description: Anwendungen müssen für diese Daten Arbeitsspeicher zuweisen. TAPI und der Dienstanbieter stellen die Daten bereit. Wenn der Vorgang asynchron ist, sind die Daten erst verfügbar, wenn die asynchrone Antwortnachricht einen Erfolg angibt.
ms.assetid: 61313fe3-74a1-4195-b5af-37463dad02c1
title: Speicherzuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f192e34fdc652293c480277631c3839ecd2435fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344237"
---
# <a name="memory-allocation"></a>Speicherzuweisung

Anwendungen müssen für diese Daten Arbeitsspeicher zuweisen. TAPI und der Dienstanbieter stellen die Daten bereit. Wenn der Vorgang asynchron ist, sind die Daten erst verfügbar, wenn die asynchrone Antwortnachricht einen Erfolg angibt.

Alle Datenstrukturen, die zum Übergeben von Daten zwischen der Anwendung und der TAPI *verwendet werden, werden vereinfacht.* Das heißt, Datenstrukturen enthalten keine Zeiger auf Unterstrukturen, die Daten Komponenten variabler Größen enthalten. Stattdessen müssen Datenstrukturen, die verwendet werden, um Variable Datenmengen an die Anwendung zurückzugeben, die folgende Metastruktur aufweisen:

``` syntax
  DWORD  dwTotalSize;
  DWORD  dwNeededSize;
  DWORD  dwUsedSize; 
    <fixed size fields> 
  DWORD  dw<VarSizeField1>Size;
  DWORD  dw<VarSizeField1>Offset; 
    <fixed size fields> 
  DWORD  dw<VarSizeField2>Size;
  DWORD  dw<VarSizeField2>Offset; 
    <common extensions> 
    <var sized field1> 
    <var sized field2>
```

Der **dwtotalsize** -Member ist die Größe (in Bytes), die dieser Datenstruktur zugeordnet ist. Sie markiert das Ende der Datenstruktur und wird von der Anwendung festgelegt, bevor die Funktion aufgerufen wird, die diese Datenstruktur verwendet. Die Funktion liest oder schreibt nicht über diese Größe hinaus. Eine Anwendung muss den **dwtotalsize** -Member so festlegen, dass die Gesamtzahl der Bytes angegeben wird, die TAPI für die Rückgabe des Inhalts der Struktur zugeordnet ist.

TAPI füllt den **dwneeddsize** -Member aus. Gibt an, wie viele Bytes erforderlich sind, um alle angeforderten Daten zurückzugeben. Das vorhanden sein von Feldern mit variabler Größe macht es für die Anwendung oft unmöglich, die für die Zuteilung erforderliche Datenstruktur einzuschätzen. Dieses Feld gibt die Anzahl der Bytes zurück, die tatsächlich für die Daten erforderlich sind. Diese Zahl kann kleiner, gleich oder größer als **dwtotalsize** sein, und Sie enthält Platz für den **dwtotalsize** -Member selbst. Wenn der Wert größer ist, wird die zurückgegebene Struktur nur teilweise ausgefüllt. Wenn die von der Anwendung benötigten Felder in der Teilstruktur verfügbar sind, muss nichts anderes ausgeführt werden. Andernfalls sollte die Anwendung eine Struktur mindestens der Größe von **dwneeundsize** zuordnen und die Funktion erneut aufrufen. In der Regel ist ausreichend Speicherplatz verfügbar, um alle Informationen zurückzugeben, obwohl es möglich ist, dass sich die Größe nochmals erhöhen könnte.

TAPI füllt den **dwusedsize** -Member aus, wenn er Daten an die Anwendung zurückgibt, um die tatsächliche Größe (in Bytes) des Teils der Datenstruktur anzugeben, die nützliche Daten enthält. Wenn z. b. eine zugeordnete Struktur zu klein war und das abgeschnittene Feld ein Feld mit variabler Größe ist, ist **dwneededsize** größer als **dwtotalsize**, und das gekürzte Feld bleibt leer. Der **dwusedsize** -Member könnte daher kleiner als **dwtotalsize** sein. Partielle Feldwerte werden nicht zurückgegeben.

Das Befolgen dieses Headers ist der fixierte Teil der Datenstruktur. Sie enthält reguläre Felder und Größe/Offset-Paare, die die eigentlichen Felder mit variabler Größe beschreiben. Das Offset-Feld enthält den Offset des Felds mit variabler Größe vom Anfang des Datensatzes in Byte. Das Größen Feld enthält die Größe des Felds mit variabler Größe in Byte. Wenn ein Feld mit variabler Größe leer ist, ist das Größen Feld NULL, und der Offset wird auf 0 (null) festgelegt. Felder mit variabler Größe, die abgeschnitten werden, wenn die Gesamtstruktur Größe unzureichend ist, werden leer gelassen. Das heißt, das Größen Feld ist auf NULL festgelegt, und der Offset wird auf 0 (null) festgelegt. Die Felder mit variabler Größe folgen den Fixed-Feldern.

Wenn der Dienstanbieter ein Variablenmember ausfüllen muss, initialisiert TAPI die entsprechenden Größen-und Offset Elemente auf 0 (null). Wenn der Dienstanbieter den Variablenmember füllt, muss er die entsprechenden Größen-und Offset Elemente auf entsprechende Werte festlegen, einschließlich **dwusedsize** und **dwneededsize** , wenn Variablen Elemente festgelegt werden. Der Dienstanbieter darf einen Variablen Member nicht abschneiden, damit er in den verfügbaren Speicherplatz passt.

Der Dienstanbieter muss Variablen Elemente unmittelbar nach den fixierten Membern der Struktur starten und zusätzlichen Speicherplatz am Ende des zugeordneten Arbeitsspeichers belassen, damit TAPI ihn für die Member variabler Länge verwenden kann. Die Variablen Elemente können in beliebiger Reihenfolge platziert werden, aber die Elemente müssen zusammenhängend sein.

 

 



