---
title: Abstrakte Datenmodelle
description: Jede Anwendung und jedes Betriebssystem verfügt über ein abstraktes Datenmodell.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- abstrakte Datenmodelle mit 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ad383e52c49997e43aa90301e7e417ef8cfeb089c9f6da151542b193b25071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121860"
---
# <a name="abstract-data-models"></a>Abstrakte Datenmodelle

Jede Anwendung und jedes Betriebssystem verfügt über ein abstraktes Datenmodell. Viele Anwendungen machen dieses Datenmodell nicht explizit verfügbar, aber das Modell steuert die Art und Weise, in der der Code der Anwendung geschrieben wird. Im 32-Bit-Programmiermodell (als ILP32-Modell bezeichnet) sind die Datentypen integer, long und pointer 32 Bits lang. Die meisten Entwickler haben dieses Modell ohne Merken verwendet. Für den Verlauf der Win32-API war dies eine gültige (aber nicht notwendigerweise sichere) Annahme, die getroffen werden muss.

In 64-BitWindows ist diese Annahme der Parität in Datentypgrößen ungültig. Wenn alle Datentypen 64 Bit lang sind, würde Speicherplatz verschwendet, da die meisten Anwendungen die höhere Größe nicht benötigen. Anwendungen benötigen jedoch Zeiger auf 64-Bit-Daten, und sie benötigen die Möglichkeit, in ausgewählten Fällen 64-Bit-Datentypen zu verwenden. Diese Überlegungen führten zur Auswahl eines abstrakten Datenmodells namens LLP64 (oder P64). Im LLP64-Datenmodell werden nur Zeiger auf 64 Bits erweitert. alle anderen grundlegenden Datentypen (integer und long) bleiben 32 Bits lang.

Anfänglich wurden die meisten Anwendungen, die auf 64-Bit-Windows ausgeführt werden, von 32-Bit-Windows portiert. Es ist ein Ziel, dass dieselbe sorgfältig geschriebene Quelle sowohl auf 32- als auch auf 64-Bit-Windows ausgeführt wird. Das Definieren des Datenmodells erleichtert diese Aufgabe nicht. Es ist jedoch der erste Schritt, sicherzustellen, dass sich das Datenmodell nur auf Zeigerdatentypen auswirkt. Der zweite Schritt besteht darin, eine Reihe neuer Datentypen zu definieren, mit denen Entwickler ihre zeigerbezogenen Daten automatisch dimensionieren können. Dadurch können Daten, die Zeigern zugeordnet sind, die Größe ändern, wenn sich die Zeigergröße von 32 Bits in 64 Bits ändert. Grundlegende Datentypen bleiben 32 Bits lang, sodass sich die Größe der Daten auf dem Datenträger, der über ein Netzwerk freigegebenen Daten oder der daten, die über speicherzuordnungsbasierte Dateien freigegeben werden, nicht ändert. Dies erleichtert Entwicklern den Großteil des Aufwands beim Portieren von 32-Bit-Code in 64-Bit-Windows.

Diese neuen Datentypen wurden den Windows-API-Headerdateien hinzugefügt. Daher können Sie jetzt mit der Verwendung der neuen Typen beginnen. Weitere Informationen finden Sie unter [The New Data Types](the-new-data-types.md).

 

 




