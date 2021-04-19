---
title: Abstrakte Datenmodelle
description: Jede Anwendung und jedes Betriebssystem verfügen über ein abstraktes Datenmodell.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- abstrakte Datenmodelle 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bfb116d5afccba1b1ce3438f8b7135d01bc1b7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337175"
---
# <a name="abstract-data-models"></a>Abstrakte Datenmodelle

Jede Anwendung und jedes Betriebssystem verfügen über ein abstraktes Datenmodell. Viele Anwendungen machen dieses Datenmodell nicht explizit verfügbar, aber das Modell steuert die Art und Weise, in der der Anwendungscode geschrieben wird. Im 32-Bit-Programmiermodell (bekannt als ILP32 Model) sind die Datentypen integer, Long und Pointer 32 Bit lang. Die meisten Entwickler haben dieses Modell verwendet, ohne es zu erkennen. Für den Verlauf der Win32-API war dies eine gültige (obwohl nicht notwendigerweise sichere) Annahme.

In 64-bitwindows ist diese Annahme der Parität in den Datentyp Größen ungültig. Wenn alle Datentypen 64 Bits in der Länge liegen, wird Speicherplatz verschwendet, da die meisten Anwendungen die größere Größe nicht benötigen. Anwendungen benötigen jedoch Zeiger auf 64-Bit-Daten, und Sie benötigen die Möglichkeit, in den ausgewählten Fällen 64-Bit-Datentypen zu verwenden. Diese Überlegungen führten zur Auswahl eines abstrakten Datenmodells mit dem Namen LLP64 (oder P64). Im Datenmodell LLP64 werden nur Zeiger auf 64 Bits erweitert. alle anderen grundlegenden Datentypen (Integer und Long) verbleiben 32 Bits.

Anfänglich wurden die meisten Anwendungen, die auf 64-Bit-Windows ausgeführt werden, von 32-Bit-Windows portiert. Es ist ein Ziel, dass dieselbe Quelle, die sorgfältig geschrieben wurde, sowohl unter 32-als auch 64-Bit-Windows ausgeführt werden sollte. Die Definition des Datenmodells macht diese Aufgabe nicht einfacher. Es ist jedoch der erste Schritt, sicherzustellen, dass sich das Datenmodell nur auf Zeiger Datentypen auswirkt. Der zweite Schritt besteht darin, eine Reihe neuer Datentypen zu definieren, die es Entwicklern ermöglichen, ihre Zeiger bezogenen Daten automatisch zu verkleinern. Dadurch können Daten, die Zeigern zugeordnet sind, die Größe ändern, wenn die Zeiger Größe von 32 Bits in 64 Bits geändert wird. Grundlegende Datentypen verbleiben 32 Bits, sodass die Größe der Daten auf dem Datenträger nicht geändert werden kann, die Daten, die über ein Netzwerk freigegeben werden, oder Daten, die durch Speicher Abbild Dateien freigegeben werden. Dadurch wird Entwicklern der Aufwand bei der Portierung von 32-Bit-Code auf 64-Bit-Windows erleichtert.

Diese neuen Datentypen wurden den Windows-API-Header Dateien hinzugefügt. Daher können Sie jetzt mit der Verwendung der neuen Typen beginnen. Weitere Informationen finden Sie [unter den neuen Datentypen](the-new-data-types.md).

 

 




