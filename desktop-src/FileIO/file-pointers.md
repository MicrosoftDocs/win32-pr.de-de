---
description: Ein Dateizeiger ist ein 64-Bit-Offset Wert, der das nächste Byte angibt, das gelesen werden soll, oder der Speicherort, an dem das nächste geschriebene Byte empfangen werden soll.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Dateizeiger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215380"
---
# <a name="file-pointers"></a>Dateizeiger

Wenn eine Datei geöffnet wird, ordnet Windows einen *Dateizeiger* dem Standardstream zu. Dieser Dateizeiger ist ein 64-Bit-Offset Wert, der das nächste Byte angibt, das gelesen werden soll, oder der Speicherort, an dem das nächste geschriebene Byte empfangen werden soll. Jedes Mal, wenn eine Datei geöffnet wird, platziert das System den Dateizeiger am Anfang der Datei, der Offset 0 (null) ist. Jeder Lese-und Schreibvorgang verschiebt den Dateizeiger um die Anzahl der gelesenen und geschriebenen Bytes. Wenn sich der Dateizeiger z. b. am Anfang der Datei befindet und ein Lesevorgang von 5 Bytes angefordert wird, befindet sich der Dateizeiger unmittelbar nach dem Lesevorgang am Offset 5. Wenn jedes Byte gelesen oder geschrieben wird, verschiebt das System den Dateizeiger. Der Dateizeiger kann auch durch Aufrufen der [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) -Funktion neu positioniert werden.

Wenn der Dateizeiger das Ende einer Datei erreicht und die Anwendung versucht, aus der Datei zu lesen, tritt kein Fehler auf, aber es werden keine Bytes gelesen. Daher bedeutet das Lesen von 0 Bytes ohne Fehler, dass die Anwendung das Ende der Datei erreicht hat. Das Schreiben von 0 Bytes bewirkt nichts.

Eine Anwendung kann eine Datei mithilfe der [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) -Funktion abschneiden oder erweitern. Diese Funktion legt das Ende der Datei auf die aktuelle Position des Dateizeigers fest.

 

 



