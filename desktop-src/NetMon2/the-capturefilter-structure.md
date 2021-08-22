---
description: In Netzwerkmonitor wird der Erfassungsfilter durch die CAPTUREFILTER-Struktur definiert.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Die CAPTUREFILTER-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5c6d8d8f8baa3710b7dff4e33c98eb8791a65dc76931caa9068bbc1280f33e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339364"
---
# <a name="the-capturefilter-structure"></a>Die CAPTUREFILTER-Struktur

In Netzwerkmonitor wird der [Erfassungsfilter](capture-filters.md) durch die [**CAPTUREFILTER-Struktur**](capturefilter.md) definiert. Das Fehlen oder die Kombination von Flags, Werten und Ausdrücken bestimmt, welche Frames vom Netzwerkmonitor Treiber übergeben oder gelöscht werden. Die folgende Abbildung zeigt die drei Bereiche der Erfassungsfilteranalyse: Etype/SAP, Adresse und Musterabgleich.

![drei Bereiche der Erfassungsfilteranalyse](images/capfilter.png)

In der folgenden Tabelle ist die Funktion der einzelnen Erfassungsfilterelemente aufgeführt.



| Filter-Element                                       | Aktion                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Etype/SAP](writing-etypesap-filter-portion.md)     | Wertet Etype-/SAP-Einstellungen aus. Die Kombination von Flags bestimmt, welche Einstellungstypen oder -werte eingeschlossen oder ausgeschlossen werden.                                                                                    |
| [Adresse](writing-addresstable-filter-portion.md)   | Wertet Quell- und Zieladressen und Adresspaare aus. Unterschiedliche Kombinationen von Flags bestimmen, welche einzelnen Werte oder Kombinationen von Adresspaaren eingeschlossen oder ausgeschlossen werden.                   |
| [Muster übereinstimmung](writing-the-patternmatch-filter.md) | Definiert komplexe Muster übereinstimmungen innerhalb eines Frames. Flags werden für verschiedene Typen und Offsets bereitgestellt. Sie können Muster übereinstimmungen mit logischen AND- oder OR-Operatoranweisungen kombinieren.                              |
| [Freistellen](clipping-a-frame.md)                     | Clipframes in einer Weise, die durch verschiedene Bytewerte angegeben wird. Sie können nur dieses Element verwenden, um alle Frames abzuschneiden oder es mit anderen Erfassungsfilterelementen zu verwenden. beispielsweise, um einen einzelnen Frame zu suchen und dann zu beschneiden. |
| [**Trigger**](trigger.md)                           | Dieses Erfassungsfilterelement ist veraltet. Trigger sind nicht mehr Teil eines Erfassungsfilters. sie sind jetzt in ihren eigenen BLOB-Tags enthalten, die separat angegeben werden.                                     |



 

Ein Frame wird für alle drei Teile des Erfassungsfilters ausgewertet. Daher muss ein erfolgreich übertragener Frame jedes Element übergeben. Beachten Sie, dass der Netzwerkmonitor-Treiber das Fehlen eines der drei Elemente als **TRUE** auswertet. Beispielsweise wertet der Treiber das Fehlen eines Etype/SAP-Abschnitts als "ALLE Frames mit dem WERT ANY Etype/SAP sind gültig" aus.

 

 



