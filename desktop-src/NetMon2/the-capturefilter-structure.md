---
description: In Netzwerkmonitor wird der Erfassungs Filter durch die capturefilter-Struktur definiert.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Die capturefilter-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959011"
---
# <a name="the-capturefilter-structure"></a>Die capturefilter-Struktur

In Netzwerkmonitor wird der [Erfassungs Filter](capture-filters.md) durch die [**capturefilter**](capturefilter.md) -Struktur definiert. Das Fehlen oder Kombinieren von Flags, Werten und Ausdrücken bestimmt, welche Frames von der Netzwerkmonitor-Treiber weitergegeben oder verworfen werden. Die folgende Abbildung zeigt die drei Bereiche der Erfassungs Filter Analyse: ETYPE/SAP, address und Pattern Match.

![drei Bereiche der Erfassungs Filter Analyse](images/capfilter.png)

In der folgenden Tabelle sind die Funktionen der einzelnen Erfassungs Filterelemente aufgelistet.



| Filter-Element                                       | Aktion                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ETYPE/SAP](writing-etypesap-filter-portion.md)     | Wertet ETYPE/SAP-Einstellungen aus. Die Kombination von Flags bestimmt, welche Einstellungs Typen oder-Werte eingeschlossen oder ausgeschlossen werden.                                                                                    |
| [Adresse](writing-addresstable-filter-portion.md)   | Wertet Quell-und Zieladressen und Adress Paare aus. Verschiedene Kombinationen von Flags bestimmen, welche einzelnen Werte oder Kombinationen von Adress Paaren eingeschlossen oder ausgeschlossen werden.                   |
| [Muster Übereinstimmung](writing-the-patternmatch-filter.md) | Definiert komplexe Muster Übereinstimmungen innerhalb eines Frames. Flags werden für verschiedene Typen und Offsets bereitgestellt. Sie können Muster Übereinstimmungen mit logischen and-oder or-Operator-Anweisungen kombinieren.                              |
| [Freistellen](clipping-a-frame.md)                     | Schneidet Frames auf eine Weise aus, die von verschiedenen Byte Werten angegeben wird. Sie können nur dieses Element verwenden, um alle Frames auszuschneiden oder mit anderen Erfassungs Filterelementen zu verwenden. um z. b. einen einzelnen Frame zu suchen und dann zu schneiden. |
| [**Trigger**](trigger.md)                           | Dieses Erfassungs Filterelement ist veraltet. Trigger sind nicht mehr Teil eines Erfassungs Filters. Sie sind jetzt in ihren eigenen BLOB-Tags enthalten, die separat angegeben werden.                                     |



 

Ein Frame wird gegen alle drei Teile des Erfassungs Filters ausgewertet. Daher muss ein erfolgreich übertragener Frame jedes Element übergeben. Beachten Sie, dass der Netzwerkmonitor Treiber das Fehlen eines der drei Elemente als " **true**" auswertet. Der Treiber wertet z. b. das Fehlen eines ETYPE/SAP-Abschnitts als "alle Frames mit einem beliebigen ETYPE/SAP-Wert sind gültig" aus.

 

 



