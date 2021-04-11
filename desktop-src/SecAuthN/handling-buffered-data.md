---
description: Einige der Netzwerkanbieter Funktionen übernehmen die Adresse und Größe eines Puffers, in dem die Funktion eine Datenstruktur mit variabler Größe platziert.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Verarbeiten von gepufferten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217335"
---
# <a name="handling-buffered-data"></a>Verarbeiten von gepufferten Daten

Einige der Netzwerkanbieter Funktionen übernehmen die Adresse und Größe eines Puffers, in dem die Funktion eine Datenstruktur mit variabler Größe platziert.

In jedem Fall ist der verwendete Mechanismus identisch. Der Aufrufer ordnet einen Puffer zu und übergibt seine Adresse an die Funktion. Außerdem übergibt Sie die Adresse eines **DWORD** , das die Größe des Puffers angibt, in Bytes.

Die Funktion kopiert dann den Großteil der angeforderten Datenstruktur, wie Sie in den Puffer kopiert werden kann. Wenn alle Daten in den Puffer passen, gibt die Funktion "WN Success" zurück \_ . Wenn die Daten nicht in den Puffer passen, bleiben die Daten möglicherweise unvollständig, und die Funktion legt den Fehler für die WN- \_ Daten mehr fest \_ . In beiden Fällen wird das **DWORD** , das die Größe des Puffers angibt, auf die Anzahl der Bytes festgelegt, die tatsächlich für die Datenstruktur erforderlich sind. Auf diese Weise kann der Aufrufer einen neuen Puffer der erforderlichen Größe zuordnen und die Funktion erneut aufzurufen, wenn der Puffer, der an übergeben wurde, zu klein war und die Funktion fehlgeschlagen ist.

Wenn die zurückgegebenen Datenstrukturen Zeichen folgen variabler Länge enthalten, enthalten die einzelnen Datenstrukturen in der Regel Zeiger auf diese Zeichen folgen. Die Zeichen folgen selbst sollten auch innerhalb des Puffers abgelegt werden. Es ist jedoch wichtig, Sie am Ende des Puffers zu platzieren. Andernfalls wird die Indizierung der Nth-Struktur unmöglich. Anders ausgedrückt: alle Strukturen werden am Anfang des Puffers zusammenhängend angeordnet. Zeiger auf Zeichen folgen oder Variablen mit variabler Länge müssen tatsächliche Zeiger sein, nicht im Puffer Offsets.

Wenn ein Puffer zum übergeben und Zurückgeben von Daten verwendet wird, die nur aus Zeichen folgen bestehen, muss das **DWORD** , das die Größe des Puffers angibt, auf die Gesamtanzahl der Zeichen festgelegt werden, die in diese Zeichen folgen passen, nicht auf die Anzahl der Bytes.

 

 



